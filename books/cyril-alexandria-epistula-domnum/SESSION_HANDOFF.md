# Cyril of Alexandria, Epistula canonica ad Domnum — session handoff

## 2026-10-23 (Wave A assembly, Claude)

Done (not committed):
- Filled the two placeholder rows from the reviewed Wave A translation (`tr0.json`):
  ep-open "Canonical Order and the Case of Peter" (`translations/ed_ep_open_english.json`)
  and ep-rem-close "Peter's Money Must Be Returned" (`translations/ed_ep_rem_english.json`).
  Old scaffold translator notes ("SERIES CLOSEOUT", lane notes) replaced with the
  translation's notes. Romans 14:12 cited inline in ep-rem-close.
- Applied reviewer fixes (english + title only, `rv0.json`) to ep-rem-early
  "Peter Was Given No Hearing" and ep-rem-mid "A Fair Trial Before the Bishops".
  The old rows called Peter "the presbyter" (τὸν πρεσβύτην is "the old man"),
  read στη|σάτω (split by column 279) as "shed a tear ... at the 279th" instead of
  "stop the old man's tears", made Peter "she", and garbled the last clause.
- Rewrote `reviews/justifications/ep_open.json` and `ep_rem_close.json` (English
  Pass A, Greek lemmas found in the source, choices, bible_refs, source
  normalizations for column numbers 277 and 280, review notes, current source hashes).
- Both `*_meta.json`: blurb and first_english_note cleaned of "SERIES CLOSEOUT" /
  "OET" lane wording and now say "fresh English translation"; text_history.method
  likewise. Status was already "available". Added `scope`: "Canon 1 and the opening
  of canon 2" (the copy-text breaks off at ταῖς inside canon 2).
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-epistula-domnum/backup/`.

Checks: `check_pass_ab` on all 4 justifications ok=4 fail=0; `--tip-ready` ok on
both english/source pairs; `work_lint --slug cyril-alexandria-epistula-domnum`
0 findings; no placeholder strings in `translations/*_english.json`.

Left open (files or fields outside this task's write list):
- `translator_notes` on ep-rem-mid still describe the old wrong readings
  ("shed the tear of the presbyter at the 279th", "unless she refuses some as
  suspects", "under her hand"). They print in the Logos edition notes. Replace them
  with notes matching the new English (see `rv0.json` "why").
- `reviews/justifications/ep_rem_early.json` and `ep_rem_mid.json` still hold the old
  Pass A/Pass B text, wrong lemma glosses ("presbyter") and, for ep-rem-mid, three
  1 Timothy 3 bible_refs that do not fit the passage.
- `book.yml` still has `status: series-closeout` and `scope: "SERIES CLOSEOUT
  e24ae197; true OET."`.
- `ed_ep_rem_source.json` section titles are still "Epistle rem early/mid/close";
  `ed_ep_open_source.json` title is "Epistle".
- Meta `edition` keeps "CPG 5378?" with a question mark; meta `topics` list
  christology / father-son-spirit / hermeneutics-types, which this disciplinary
  letter does not treat.

## 2026-10-24 (follow-up cleanup, Claude)

Done (not committed). No English reading text changed.
- `intro.md`: this book has none, so there was nothing to correct. The site's
  "About this text" comes from the meta blurb and text_history, already clean.
  Logos builds warn "no intro.md" (front matter needs 3 paragraphs); not written.
- `translator_notes` rewritten on all four sections. ep-rem-mid's old notes
  ("279th", "she", "under her hand") and ep-rem-early's "begins mid-sentence"
  note are gone; the new notes follow `rv0.json` (old man, not presbyter;
  στη|σάτω split by column 279; Peter is the subject; αὐτῆς = your piety) and
  name the PG column numbers 278/279/280. "Pass B", "row" and "this row only"
  wording removed from ep-open and ep-rem-close; the ep-rem-close join quote now
  matches the English ("some who are under suspicion").
- `reviews/justifications/ep_rem_early.json`, `ep_rem_mid.json` rebuilt:
  pass_b_english = current English; new Pass A sense gloss of every clause;
  lemmas corrected (πρεσβύτης "old man", συνίστημι, ὑπόμνημα, ἄθεσμος,
  προσεπάγω) with forms in the source's exact spelling; choices record the
  corrected readings; the three 1 Timothy 3 bible_refs removed; column-number
  source_normalizations; review block; old machine-draft stamps dropped (copies
  in the backup).
- `book.yml`: status available; scope "Canon 1 and the opening of canon 2"
  (same as the metas); new `description` in "fresh English translation"
  wording; workroom notes replaced by the copy-text line. Edition unchanged.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-epistula-domnum/backup-cleanup/`.

Checks: `check_pass_ab` ok=4 fail=0; `--tip-ready` ok on both pairs;
`work_lint --slug cyril-alexandria-epistula-domnum` 0 findings.

Still open (outside this task):
- Source section titles "Epistle" / "Epistle rem early/mid/close" (changing the
  source file changes its hash in all four justifications).
- `baehrens` fields end "ep open" / "ep rem early" etc.; `claim` ids end "-oet"
  (internal keys, left alone).
- Meta `edition` "CPG 5378?" question mark and the meta topics list.
