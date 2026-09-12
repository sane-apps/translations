# Translations — session handoff

## 2026-09-12 (Air — pulcheria-rf-a11 Pulcheria §§41–44)

- Claim `pulcheria-rf-a11`: receives all authority in emptying measures; emptied Word exalted to what he was; Father raises yet Son raises own temple; baptized into one death—Word suffered in flesh; Spirit of Jesus; crucified from weakness / lives by God’s power. Pass A ≠ B; Greek locked `greek_clean_a11`.
- `jer-h20b` intact. No site CSS. Melito skipped.

## 2026-09-12 (Air — pulcheria-rf-a10 Pulcheria §§37–40)

- Claim `pulcheria-rf-a10`: one offering of own body; weak in flesh / beyond weakness as God; sits at right yet ministers; own blood once; appears not as naked Word; crucified Lord of glory receives glory economically. Pass A ≠ B; Greek locked `greek_clean_a10`.
- `jer-h20b` intact. No site CSS. Melito skipped.

## 2026-09-12 (Air — pulcheria-rf-a9 Pulcheria §§33–36)

- Claim `pulcheria-rf-a9`: post-baptism temptation type; Word as high priest and lamb; passes heavens bodily and divinely; Heb 5 call/obedience; we pray in him as second firstfruit; neither bare man nor fleshless Word—impassible in own flesh. Pass A ≠ B; Greek locked `greek_clean_a9`.
- `jer-h20b` intact. No site CSS. Melito skipped.

## 2026-09-11 (overnight hang watch)

- Live Mini burn is **HEALTHY** (jer-h8 → done, jer-h5a NVIDIA promote in flight). Do not bootout.
- Hang hole closed: `run_bounded` kills draft/promote process groups after `claim_wall_s` (exit 4). `draft_claim.py` has the same wall. Health: `python3 scripts/fathers_overnight_health.py` (`--kill` only if the log is silent). Grok scheduler every 30m.

## 2026-09-11 (Homilies 3–4 shipped; CF drafts held)

- Combined the earlier choice: fill the 3–4 gap at the Homily 1–2 bar; do **not** upload CF 6–7, 9–10 until a literary pass. Homily 8 still running on Mini NVIDIA — leave it.
- Site `publish_homilies: [1, 2, 3, 4]`. Checker 8/8 for 3–4. Machine drafts stay in JSON off the public reader.

## 2026-09-11 (EOD wrap — flock overnight + jer-h8)

- **Shipped:** dual-lane Mini overnight is calendar-only (21:10 local, no KeepAlive). Concurrency is kernel `fcntl.flock` (`scripts/fathers_run_lock.py`): global burn + per-claim locks. Promote exits: `0` done, `1` content, `2` API, `3` lock busy, `4` claim wall. Docs: `docs/AI_CROSSCHECK.md`. Install: `scripts/install-mini-overnight-quota.sh`. Regression: `python3 scripts/test_fathers_run_lock.py`.
- **Live on Mini (leave alone):** `jer-h8` claimed by `overnight-mini-nv`; one promote may still be running under the LaunchAgent job. Do **not** free/re-claim, second-burn, or `bootout`/`kickstart` while locks/`ai_promote` are live. When idle: sync Mini → Air `docs/CLAIMS.md` + Jeremiah `jeremiah_english.json` + `reviews/justifications/jeremiah_8_*.json`, then confirm claim `done` or leave `claimed` for next calendar burn.
- CF lane near reserve today (~9.7k+/10k used earlier); NV lane independent. Logos still Air-only.
- SaneProcess `scripts/automation/recurring-jobs.md` updated to match (no KeepAlive).

## 2026-09-11 (Help us + one-command start)

- Site nav **Help** → `/contribute/`: donate (GitHub Sponsors), buy a Mac app (saneapps.com, one-time, no prices), point an AI (`claims.py start`), spot-check Greek/Latin (GitHub issue).
- Contributors: copy `docs/START_HERE.md` into the AI (site Help has a Copy prompt button). GitHub README: four one-click links.
- Visual: `websites/fathers.saneapps.com/outputs/visual-audit-2026-09-11-help/`.

## 2026-09-11 (reader witness disclosure)

- Public works: collapsed **About this text** names copy-text, checked prints, and real joins (`text_history`). Reading column stays clean. Italic cue only for a stretch supplied from another witness (none live yet).
- Jeremiah pattern: GCS 1901 copy-text; TEI/DjVu checks of the same print; joins at Hom. 1.1, 1.5, 1.11. `publish_homilies: [1, 2]` so later JSON drafts do not ship. No PG 13 / Jerome claim yet.
- Same About block on the other live works, honest to what is actually locked. Site `/about/` states the method.

## 2026-09-11 (two-pass pipeline on live works)

`python3 -m pipeline.check_pass_ab` (Pass A gloss ≠ B, lemmas, choices, real source_text):

| Work | Receipts | Checker |
|------|----------|---------|
| On Prayer (Gebet) | 34 | ok |
| Martyrdom | 52 | ok (some Greek slices overlap chapters; A follows locked block) |
| Heraclides | 28 | ok (was Greek dumped as A; now English gloss) |
| Pascha | 149 | ok |
| Cyril Adoration 1 | 39 | ok (was 36× A==B) |
| Jeremiah Homilies 1–2 | 19 | ok |
| Julian To Florus 1 | 141 | ok |
| Julian rest | in flight | Books 2–6 + fragments |

Jeremiah 3–7 stub files exist without English; not live; not `source_verified` in the two-pass sense.

## 2026-09-11 (reader SOP + two-pass bar)

- Works reader SOP is live (`websites/fathers.saneapps.com/AGENTS.md`). Mini visual: `outputs/visual-audit-2026-09-11-reader-sop/`. Rail, thought-chunks, text-first at 375, cite “Read continuously.”
- Two-pass translation is now pointed from `clients/translations/AGENTS.md` and `docs/SOP.md` → `TRANSLATION_QA.md`. Pass A ≠ Pass B.
- **Jeremiah Homilies 1–2:** real Pass A glosses + lemmas written (19 receipts). Earlier receipts had copied B into A; those are replaced.
- **Still not through real Pass A:** Julian (no justifications). Cyril Adoration 1 (36/39 A copies B). Martyrdom (empty lemmas). Many Pascha/Heraclides receipts lack lemmas/choices. Do not call those `source_verified` in the two-pass sense until A is a gloss.

## 2026-09-11 (keep going — rest of Origen and Cyril)

- Owner: keep going on the rest of Origen and Cyril; do not wait for a reminder. Logos still deferred.
- **Origen Jeremiah:** Homilies 1–2 on the site. DOCX 19 / 111 links / 7 TN. Homilies 3–20 still to translate.
- **Cyril Adoration Book 2:** PG 68 Greek ingested, 26 columns (`adoration2_source.json`). English 1–8 drafted in `scripts/english_adoration2_part1.py`. Not shipped until Book 2 is complete.
- **Cyril court treatises:** Pusey 1877 PDF + OCR locked in `cyril-alexandria-recta-fide-court/sources/`. Not yet sectioned or translated. Skip *ad Theodosium* (King FC 129).
- Work sessions still on. Do not run `work_session_off`.

## 2026-09-11 (evening keep-awake)

- Work-session guards renewed on Air and Mini; caffeinate through **2026-09-12T01:21:24Z** (Air) / **2026-09-12T01:21:35Z** (Mini). Do not run `work_session_off` while this scheduler still needs both hosts.
- Pascha English literary pass shipped (149/149). Fixed 1.63 (disciples vs crowds) and bare `lacuna` in 1.63/1.75. Heraclides + Cyril Book 1 light prose pass (author voice kept). No Logos compile.
- Site rebuilt and deployed: https://fathers.saneapps.com — 10 works / 1466 sections. No “First English” button. Heading remains “Treatises with no earlier English.”
- Mini now has the Origen Book 2, Cyril Book 1, Prayer/Martyrdom, and fathers site trees (they were missing).
- Next: Cyril court treatises (`cyril-alexandria-recta-fide-court`) or human review of Pascha lacuna justifications. Optional Air Logos Build.

## 2026-09-11 (overnight)

- Work-session guards renewed on Air and Mini; caffeinate through **2026-09-11T17:20:14Z** (1:20 PM EDT). Scheduler renews both every 8 hours. Do not run `work_session_off` until this run ends.
- Site labels: no “First English” button. Heading is “Treatises with no earlier English.”
- Pascha Greek is locked (149 §§). English in progress. Heraclides + Cyril Book 1 prose polish in progress.

## 2026-09-11 (no-earlier-English marking)

- Treatises with no earlier complete public-domain English are grouped on home and `/works/#no-earlier-english`, and noted on each work intro. Not a slogan button.
- Listed: On Prayer, Exhortation to Martyrdom, Dialogue with Heraclides, Cyril *De adoratione* Book 1. On Pascha when English ships.
- Julian is not in that list (Victorian English of some of his words already exists inside Augustine).

## 2026-09-10 (website fill + Cyril + Origen remainder)

- **Site live:** topic pages print `topics.yml` notes, author groups, Nicene+ banner. Explore: 47 topics / 373 points. 9 works / 1317 sections. Visual: `websites/fathers.saneapps.com/outputs/visual-audit-2026-09-10-fill/`.
- **Cyril:** inventory at `books/ante-nicene-topics/outputs/cyril_alexandria_untranslated_inventory.md`. *De adoratione* Book 1 English + DOCX (`verify_docx` OK) + https://fathers.saneapps.com/works/cyril-adoration-1/ — Book 1 of 17, post-Nicene banner. Logos PBB not compiled (ready to attach).
- **Origen Heraclides:** 28 Scherer sections, DOCX 138 Bible links / 94 TN, live at `/works/origen-dialogue-heraclides/`. Pascha still needs Witte page-image transcription. Remainder: `docs/ORIGEN_CORPUS.md`.

## 2026-09-10 (Gifts + works queue)

- `docs/WORKS_QUEUE.md` added (Tier A: Origen Heraclides/Pascha → Melito → Irenaeus *Demonstration*).
- **Gifts and Order** (`gifts-and-order`): replaced 17 weak ANF seeds with 11 new-English excerpts from locked Didache, Hermas Mand. 11, Justin 1Apol 6, Irenaeus AH 2.32.4 / 3.11.9 / 4.26.5 / 5.6.1 / 5.8.1, Tertullian Marc 5.8.
- Explore: claims + stances + rupture for `gifts-and-order`. Deployed to https://fathers.saneapps.com/topics/gifts-and-order/ and `/explore/?topic=gifts-and-order`.
- Origen Book 2 scaffolded: `books/origen-heraclides-pascha/` — charter + Greek locks (Heraclides DCO; Pascha Witte OCR).
## 2026-09-10 (Explore)

- Public `/explore/` topic-river timeline: stance lanes × time; century aggregation; compare ≤3 authors.
- Seed: 5 topics, editorial stances, Augustine contrast cards, rupture captions.
- Data: `websites/fathers.saneapps.com/data/explore/`; schema in `docs/SCHEMAS.md`.
- Live: https://fathers.saneapps.com/explore/?topic=free-will

## 2026-09-10

- **PBB anti-pattern locked:** Word footnotes banned; clear Scripture as inline `[[… >> Bible:…]]`; TN = Headword marks. Caption dumps labeled `Scripture connection:` banned.
- Enforcement: `pipeline.verify_docx` (also runs `check_pbb_guards`), Cursor hook `pbb_pre_tool_use` → `sane_pbb_guard.rb`.
- Julian DOCX rebuilt: `Cf.` / `Possible allusion` captions; Wisdom-of-Solomon index heading fixed. Verify green. Re-Build in Logos on Air if you want the library copy updated.
- Origen DOCX already green (TN + inline).
- Public site: https://fathers.saneapps.com — Origen On Prayer + Martyrdom complete; Julian To Florus + four fragment works; topic↔work cross-refs (`WORK_TOPICS`).

## 2026-09-09

- Created `~/SaneApps/clients/translations` (Logos Personal Book pipeline).
- Migrated Julian from Documents into `books/julian-of-eclanum/`.
- Shared `pipeline/` extracted from Julian builder (Bible links, DOCX helpers, verify).
- Documents old path is a pointer only (Air).
- Logos GUI remains Air-only.

## Next

- **Works queue:** `docs/WORKS_QUEUE.md` — Heraclides, Pascha, and Cyril Adoration Book 1 are on the public site. Next: Cyril court treatises / Trinity Dialogue 1, then Melito *On Pascha* or Origen Rank 1 in `docs/ORIGEN_CORPUS.md`.
- **Pascha:** English 149/149 live. Greek still first-pass (`pascha_source.json`, not all `source_verified`). `sources/pascha_ocr_status.md`.
- **Gifts of the Spirit:** `gifts-and-order` refreshed 2026-09-10 (11 `source_draft` excerpts from locked Greek/Latin; Explore claims/stances added).
- Optional: Logos re-Build for Julian English DOCX on Air.
- Optional: `git init` for `websites/fathers.saneapps.com` so formal `capture-web-screenshot.sh` gates work.

## Gifts 0–800 wave (2026-09-10)

38 `gifts-and-order` excerpts; Explore claims include `signs-then-not-now`. See `books/ante-nicene-topics/outputs/gifts_coverage_receipt.md`.
