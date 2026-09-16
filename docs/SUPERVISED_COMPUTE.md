# Supervised Compute — free AI lanes on the Mini and Air

This is the operating system for getting real translation work out of free
model access. It exists because unsupervised runs drift: vague briefs with no
checking produced a 500-file uncommitted pile and padded Bible links. Every
lane below is cheap, and every lane is supervised. No lane writes to the tree
without passing the gates, and no lane commits.

## Hosts and roles

- The Mini is the worker. Repo inspection, builds, tests, model runs, and
  verification all happen there. The translation repo lives at
  `~/SaneApps/clients/translations` on both machines.
- The Air is the controller. The supervisor (Muse) dispatches tasks from the
  Air over ssh, verifies results, and reports. The Air also owns the one job
  that can only happen there: Logos Personal Book compile in the owner's
  Logos library (see `docs/LOGOS_PERSONAL_BOOK_BACKLOG.md`).

## Lanes

| Lane | Host | What it costs | Best use | Limits |
|---|---|---|---|---|
| opencode free models (e.g. nemotron-3-ultra-free) | Mini, headless `opencode run` | Nothing; rate limits are the budget | Bounded agent tasks: rebuild a book, fix a named defect, run a gate sweep | Flaky upstream (502/504 storms); needs small tasks and retries; never unsupervised overnight |
| Cloudflare Workers AI draft/checker lanes | Mini, `scripts/llm_bakeoff.py` + lane config | Nothing; quota-capped | Draft translation passes and mechanical checker votes | Quota windows; check `outputs/overnight-quota/` before large runs |
| NVIDIA NIM draft/checker lanes | Mini, same bakeoff path | Nothing; quota-capped | Same as above, different model family for second opinions | Same quota discipline |
| Gemini prep/QA lane | Mini, `scripts/gemini_prep_lane.py` | Nothing; free tier | Prep work and third-opinion QA only; never promotes alone (`auto_promote` is false, keep it that way) | Enable with `docs/LLM_LANE_CONFIG.json` gemini flag or `FATHERS_ENABLE_GEMINI`; key is on the Mini |
| TypeSafe Jev reviewer | Air (controller side) | Metered tokens, roughly 500 in / 50 out per judgment, under a second | Independent second opinions on judgments the gates cannot make: allusion certainty, ops-chatter vs scholarship, review-need triage | Typed output guarantees the interface, not the truth; flags mismatches for a stronger reviewer, never decides alone |

The TypeSafe key lives at `~/.config/typesafe/env` (mode 600) on both
hosts, so review can run wherever the data is. The key never appears in
typed commands, shell history, logs, or committed files: load it from the
env file (`set -a && . ~/.config/typesafe/env && set +a`).

## The loop

Every unit of work goes through these steps in order. A unit is one book or
one named defect. Nothing larger.

1. **Brief.** The supervisor writes a task brief (template below): scope
   files, exact acceptance checks with the literal commands, and an explicit
   stop. One unit per dispatch, fresh session per task. Never append a second
   job onto a running session; long accumulations (millions of input tokens)
   are where context rots and padding creeps in.
2. **Dispatch.** opencode lane: `opencode run --session <id> --fork` for
   follow-ups, or a fresh `opencode run --dir <repo> -m <provider/model>`
   for new units. Bakeoff lanes: claim a row first (`scripts/claims.py`),
   then run the lane script. Record the dispatch (lane, model, session) in
   the report.
3. **Verify.** Mechanical gates first: `assert_tip_ready.py` on the pair,
   `verify_docx` on the rebuilt book, `check_pbb_guards`. Then the Jev
   cross-check on every added allusion (`scripts/jev_review.py`): any
   mismatch between the filed certainty and Jev goes to a stronger reviewer,
   and padding fails the unit outright. Then a human-grade spot check of the
   actual diff: read the English against the source for at least one section.
4. **Land.** Passing work lands in the working tree only. Workers never
   commit. Keep units small enough that each one is reviewable on its own.
5. **Report.** One short digest per unit: what was tasked, what changed
   (files + line counts), gate results word for word, Jev verdicts, and what
   is still open. The owner commits when ready.

## Brief template

```
Task: <one book or defect>
Scope files: <exact paths; nothing outside them>
Do first: read <the 2-3 docs/sections that govern this task>.
Do: <numbered steps, each verifiable>
Acceptance (run literally):
  - <command 1, must exit 0 / print OK>
  - <command 2>
Stop conditions: change no files outside scope. Commit nothing. Claim nothing
new. If a gate fails for a reason outside your scope, stop and report it
instead of working around it. End with a short report and wait for orders.
```

## Locks and schedule

- The overnight burn owns the Mini from 21:10 local under flock
  (`scripts/run-overnight-quota.sh`, `scripts/fathers_run_lock.py`).
  Supervised runs check the locks first and never start a second burn while
  global or claim locks are held. Daytime supervised work and the nighttime
  burn never overlap by design, not by luck.
- On 502/504/429 or empty responses: back off, retry the single failed call
  at most twice, then report the lane as degraded and move the unit to
  another lane. Never hammer a failing free endpoint.
- A run doing only tiny read-only tool calls for many minutes with nothing
  landing is stuck, not working. Stop it and re-brief smaller.

## Standing prohibitions

These restate project rules where free-compute agents keep tripping:

- No padded Bible links. A link asserts the author invokes the passage
  (`docs/LOGOS_MARKUP.md`). The Jev cross-check exists to catch exactly this.
- No new Rank-1 claims while the quality pause holds; no invented claims at
  all (`docs/CLAIMS.md` + `scripts/claims.py` are the only queue).
- No stubs presented as completed work: empty sections, scaffold English,
  and unbuilt DOCXs fail the unit.
- Keep the working docs lean (pointer lines in each file say how). Log
  entries are short and factual.
