# Ad Optimum episcopum (Basil, Letter 260, in PG 77 among Cyril's letters) — production ledger

Canonical path: `~/SaneApps/clients/translations/books/cyril-alexandria-ad-optimum/`

## 2026-10-23 — Wave A assembly (Claude, Mini)

- Author settled: this text is Basil of Caesarea's Letter 260, to Bishop Optimus, on Genesis 4:15.
  PG 77 prints it among Cyril of Alexandria's letters as Letter 80. Checked three ways: the Wave A
  translator and reviewer both matched the Greek to Basil's Letter 260; the NPNF Series 2 vol. 8
  English of Basil's Letter 260 (newadvent.org/fathers/3202260.htm) follows our Greek clause by
  clause through section 3; the source PDF sits in the Khazarzar PG 68-77 Cyril folder. The work
  stays on the site; both `*_meta.json` now say plainly that it is Basil's letter carried under
  Cyril's name.
- All four sections are now real English (PG cols. 365-368 = Basil, Letter 260, sections 1-3).
- Replaced the two scaffold rows with reviewed translations from Wave A `tr0.json`:
  ep-open "Thanks for the Letter and Its Question", ep-rem-mid "The First Sense and a Deeper
  Question". The staged rows in `rv0.json` match `tr0.json` exactly.
- Applied reviewer retranslations (english and title) from `rv0.json`: ep-rem-early "Roused in Old
  Age, and the Plain Sense", ep-rem-close "The Number Seven in the Law and This Age".
- translator_notes replaced on all four rows: the scaffold rows carried workroom lines (Melito /
  densify / Pusey), and the old ep-rem-early and ep-rem-close notes were wrong (rv0 asked for this:
  "perfect middle", "believers' state", "fragment cut at the beginning"). New notes come from the
  tr0 notes and the rv0 `why` text.
- Copy-text readings taken by sense, now supported by the NPNF English of Letter 260: ἀποίκιλον
  read as καὶ ποικίλον ("a more varied explanation"); ἢ μέλλει read as a condition ("if he is to be
  made better").
- Justifications rewritten for ep_open and ep_rem_mid (English Pass A, Greek lemma tags in
  lemmas[], bible_refs, choices, review_notes, source sha256).
- Both `*_meta.json`: title "Letter to Optatus" corrected to "Letter to Bishop Optimus" (the
  heading names Optimus); period "c. 412–444" (Cyril) corrected to "c. 377" (Basil); blurb and
  text_history rewritten in plain English with "fresh English translation" wording; scope added
  (opening of the letter only, sections 1-3; breaks off mid-sentence); first_english set to false,
  since an NPNF English of Basil's Letter 260 exists; the old first_english_note (SERIES CLOSEOUT /
  OET wording) removed. Status stays "available".
- Checks: `check_pass_ab` on reviews/justifications ok=4 fail=0; `--tip-ready` ok on both pairs;
  `work_lint --slug cyril-alexandria-ad-optimum` findings=0; no placeholder strings left in
  translations/*_english.json.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-ad-optimum/backup/`.
- Not committed.

### Open

- Justifications ep_rem_early and ep_rem_close still hold the old machine-draft pass_b_english,
  lemmas and choices (for example "arranged", "elders", Leviticus 25:8-55). Rewrite them from the
  rv0 English.
- `book.yml` still says `author: Cyril of Alexandria`, `status: series-closeout`, a workroom
  `scope` line and "CPG 5379?". Decide whether the site lists this under Basil or keeps it under
  Cyril with the attribution note.
- Meta `edition` string still reads "PG 77; CPG 5379? / Ep. 80 Ad Optimum (Cain)"; the CPG number
  is unverified. Meta topics (christology, father-son-spirit) do not fit a letter on Cain's
  punishment and forgiveness.
- Only sections 1-3 of Letter 260 are in the locked PG text. Sections 4-9 (Cain's seven sins,
  Lamech, Simeon's sword) are not translated.

## 2026-10-24 — follow-up cleanup (Claude, Mini)

- intro.md: none exists for this book, so the site's About this text comes from the metas. Nothing
  to correct there except the edition line (below). No intro.md was created.
- Metas: `edition` now "PG 77, cols. 365-368 (Letter 80 among the letters of Cyril of Alexandria;
  Basil of Caesarea, Letter 260)". The unverified "CPG 5379?" is gone. Site check: About shows the
  full line, the mast label is "PG 77".
- translator_notes: ep-open author note shortened to the attribution facts (process text about how
  identity was checked removed). ep-rem-early reading note no longer claims the Greek of Basil's
  Letter 260 has καὶ ποικίλον; it now says the standard English of Letter 260 takes it the same way
  (what was actually checked). Other notes were already true of the current English.
- Justifications ep_rem_early and ep_rem_close rewritten: pass_b_english = current English; new
  Pass A sense glosses of every clause; lemmas re-tagged with forms copied from the copy-text's own
  code points (the PG text uses U+1F73-style oxia and ∆ U+2206 in ∆εσπότου); choices from the rv0
  fixes; bible_refs Romans 12:11 + Genesis 4:15 (early), Exodus 21:2 + Leviticus 25:8-10 (close);
  old machine-draft reviewer stamps and ai_crosscheck fields dropped. ep_open Pass A: τέως μέν
  glossed "first of all" to match the English and its choice.
- book.yml: title "Letter to Bishop Optimus", original_title "Ad Optimum episcopum", author Basil of
  Caesarea (agrees with the metas), status available, reader scope line, description in "fresh
  English translation" wording, edition as in the metas, workroom notes replaced. The metas carry no
  author field, so the site's author listing is unchanged by this.
- English text and titles unchanged (checked against the backup).
- Checks: check_pass_ab ok=4 fail=0; --tip-ready ok on both pairs; work_lint findings=0.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-ad-optimum/backup-cleanup/`.
- Not committed.

### Still open

- Meta topics (christology, father-son-spirit) still do not fit a letter on Cain's punishment and
  forgiveness; not changed here (catalogue-level choice).
- English rows' internal `baehrens` field still carries the old "CPG 5379?" string; no site or
  build code reads it.
- Sections 4-9 of Letter 260 are not in the locked PG text and are not translated.
