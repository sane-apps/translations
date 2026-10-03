# Via Patrum spend plan, Oct 3

**Bottom line:** Oct 3 cost $598–633, depending on the time window. Only about **$79/day of ongoing waste** is proven, plus **about $58 of one-off waste**. That is roughly 13% of the day. Most of the money bought work we keep but cannot count yet. Large books saved passed sections but certified nothing. Aura spent $140 re-voicing works in the narrator you chose. Translation lanes certified 18,068 source words, all from small books, at **$33 per 1,000 certified words all-in**.

## 1. Where the ~$598 went

The account total was $605–633 on Oct 3 (UTC day). Your $598 uses a different window. The other jobs (about $47) are already counted inside the model rows below.

| Source | $/day | What it produced |
|---|---|---|
| Kimi K2.6 + GLM-5.2 (checkers, judges, readers) | $234 | The checks behind about 1,200 passed sections. Also beliefs grading (3,925 grades, about $17 with GPT-OSS), which is kept. |
| DeepSeek V4 Pro (drafts, repairs, polish) | $148 | 1,196 sections passed. Only about 4,400 of 18,750 billed calls ended in the attempts that passed. |
| Aura-2 narration | $140 | About 90 h of orion audio, nearly all re-reading works that already had audio. 0 new audiobooks. Kept, and done by your rule of one narrator per work. |
| GLM-5.3 (checker in 1 of 3 lane pairs since 13:43, plus a bench) | $80–85 | At least 668 billed calls (27%) returned no answer. Your own defect-bench had rejected it at 01:27 that morning. |
| GPT-OSS-120b | $26–29 | Checker in every lane pair, plus beliefs grading. |
| Small models (old overnight runner, Nemotron-120, Qwen, clef) | about $10 | The old runner shipped 4 claims out of 1,277 attempts. The clef pass verified 175 citations. |

Translation lanes by outcome (21 h window, $473.7):

| Outcome | $ | Notes |
|---|---|---|
| Certified | $24.4 | 51 works, 19,374 words, all under 2,039 words each |
| Held | $202 | Most retries later pass: 68–86% of retried "confirmed after repairs" holds |
| Killed | $215.5 | Passed sections are kept. About $40 was really lost. |
| Still running | $31.7 | |

The 2k–20k and over-20k books (lane groups B, D and E) spent $226.6 and certified nothing. But D and E saved about 272 passed sections that will count later.

## 2. Proven waste, ranked by corrected $/day

| # | Item | $ | Fix | Accuracy risk | How to prove it |
|---|---|---|---|---|---|
| 1 | GLM-5.3 as a lane checker (confirmed) | **$70/day**, could reach about $116/day at the 6-lane pace. At least $40–50/day is calls that return nothing. | Take glm-5.3 out of PAIRS in run-recert-lanes.sh:46 and go back to the pairs the bench chose. When it fails as a checker, the check silently moves to qwen3.8-27b, which was never benched. When it fails as a judge, the finding counts as confirmed (work_pipeline.py:777), which buys paid repairs or a hold. | Low. The claim said medium; a skeptic argued low because the swap restores the benched pairs. | Daily count of `glm-5.3 failed` lines in lane*.out (fixed-string grep) goes to 0. GLM-5.3 neurons in GraphQL go to about 0. Hold and pass rates match the other pairs. |
| 2 | Quotation-voice backlog, not spent yet (confirmed) | **$52.85 one-off.** It would re-read 2,336 passages to change about 3% of their text. | In `_quote_voice_item`, set quote_voice to arcas with no TTS when a passage has no quotation. For the rest, re-speak only the sentences with quotations, through the reuse_plan path. All 2,336 old mp3s still exist. | None (audio only). Small seams in the joined audio are possible. | That drain run bills about 96k characters, not 1.86M. |
| 3 | Rejected read-fix calls (**contested**) | $6.1/day | Do **not** filter reader findings; that drops real fidelity repairs. If anything, bench a less noisy acceptance test: reject only when a new confirmed finding falls in the edited span, deletions and source quotes included. | Medium to high as proposed. These rejections are partly the accuracy gate working. | Bench about 20 works. Final confirmed problems must not rise. |
| 4 | Defect-bench GLM-5.3 arm ran 90 min (confirmed) | $5.19 one-off | Add a roughly 10-call smoke gate on speed and $/call before a full bench arm. Never reject on recall from 10 calls. | None | The next failed arm costs under $0.50 in GraphQL hourly rows. |
| 5 | Polish on low-score sections (confirmed) | $4.7/day | Remove the fallback that polishes every section when readers flagged none. Skip polish when the reader mean is below 3.0. **Keep** polish at 3.0–3.49, where 7 of 8 crossings happened. **Keep** round 1, where 4 of 8 crossings happened. The proposed fix had both backwards. | None to low | Polish calls drop by about 2/3. Works passing readability per day stay the same. |
| 6 | Old overnight-quota runner retries the same held claims (confirmed) | $4.3/day while on. $0 now (it died at 19:16Z). | Keep it off. overnight_catchup.sh will restart it at Oct 5 09:10, or on any reboot after Oct 4 15:16Z, so disable that path. If it ever runs again, fix record_claim_fail so an empty defect_key parks the claim. | None. It actually removes a weaker check path. | No more `*-dual.json` receipts. The four small models' daily spend goes from $4.3 to $0. |
| 7 | Re-voicing apollo/odysseus works (**contested**) | $1.5 one-off. $15 is left in total. | Your call: it is part of the voice switch. | None | — |
| 8 | Read-fix/polish rejected on finding count (**contested**) | **$0 saving.** The fix still runs every check. | Not a cost item. | Medium | — |

Total confirmed: **about $79/day ongoing** (items 1, 5, 6) and **about $58 one-off** (items 2, 4).

## 3. Change now vs your decision

**Now (safe):**
1. Swap GLM-5.3 out of the lane pairs, then restart gracefully by touching `outputs/work-pipeline/lanes.restart`. Nine processes still run the GLM-5.3 pair. The same restart also replaces the stale origen-jeremiah-samuel process (PID 54938), which still runs code from before the 16:06 fix and keeps throwing false "soul"/"Church" gate holds.
2. Apply the corrected polish gate from item 5.
3. Stop overnight_catchup.sh from restarting the old runner before Oct 5 09:10.
4. Apply the quotation-voice fix before the drain reaches that backlog. It is still re-voicing bm_daniel works now.
5. Add the bench smoke gate.

**Needs a person (accuracy harm found):** repairs in origen-jeremiah-samuel replaced a correct "soul" (Greek psychē) with "Jerusalem". Counts differ: 7 live edits in one count, 9 in another (sections 13.2, 14, 23, 25, 34). Section 14.json is already marked passing and reads "Jerusalem's watchful and contemplative power". Revert these before that work is published, then run regate_held.py after the restart.

**Your decision:**
- **Pace of the voice switch.** Moving every older-voice work to orion plus arcas is a one-time cost of about $360, or about $307 after the quotation fix. Under current code it all runs within about 2–3 days. It is not waste. A daily cap (for example `REVOICE_USD_PER_DAY`), with certified works first, would spread it out.
- **Flash for repair and polish.** The flash-polish-repair bench says to adopt it in stages. It cuts 2/3 to 3/4 of Pro editing calls. Pro editing was about 6,900 calls (about $52 over 22.9 h), so the saving is roughly $30–40/day at 15 lanes. This changes the lanes, so roll it out in stages as the bench says.
- **Read-fix acceptance rule** (item 3): bench it or leave it alone.

**Not waste, or already fixed. Don't chase these:**
- About 41,000 GLM rate-limit rejections and 13,329 failed DeepSeek calls cost $0.
- Kill churn lost about $40 on Oct 3. Graceful restarts landed at 15:52 and no kill has happened since 17:34.
- Held-section redrafts: 68–86% of retried "confirmed after repairs" holds later pass. A cheap upgrade is to pass the old findings into the redraft.
- Reads on held books are mostly fixed since 15:52.
- Flat read rounds: the defensible saving is about $2/day.
- Large books save their passed sections, so kills do not wipe them.

## 4. The daily metric: cost per certified 1,000 source words

- **Today: $33.10 all-in** ($598 / 18,068 words). Lanes only: **$24.5** ($473.7 / 19,374 words in the 21 h window).
- **After the confirmed fixes, at today's output:** about $28.7 all-in ($519 / 18,068) and about $21 lanes only. Cuts alone move this metric only a little.
- **Target: $13 lanes only.** Small books already hit $12.8 today ($9.2 for live books under 2k words, $15.9 for unpublished books under 20k). Getting there takes more certified words, not just fewer dollars: point lane hours at books that can certify, and let the large books' saved sections cash out. Large books certify in bursts, so report a 7-day rolling figure next to the daily one.
- **Credit runway (rough).** The balance is **not in the inputs**. Memory notes say a $10k CF grant, which I did not check. Oct 1–3 spent $712, which leaves about $9,288 if that grant is the whole pool.
  - At $598/day: about 15 days.
  - At the 6-lane pace ($317–396/day for lanes, a skeptic's estimate), plus about $135/day of Aura for 2–3 days, minus the GLM-5.3 swap: about **4–5 weeks**.
  - Pull the real balance from CF billing before relying on this.

**Still open (hooks blocked these counts):**
- What kind of failure each of GLM-5.3's 334 failure lines is.
- Unparseable failures per model under the current code.
- Check rounds per held attempt.
- Why two lanes ran barnabas-epistle at the same time (18:04), and why didache started three times at once. This may be a race in the check for a book that is already running.
