# Hesychius of Jerusalem, Homily II on the Holy Pascha — production ledger

Canonical path: `~/SaneApps/clients/translations/books/hesychius-homilia-ii-pascha/`

## 2026-10-23 — Wave A assembly (Claude, Mini)

- Whole homily (opening trumpet to doxology, one unit, four sections) is now real English.
- Replaced the scaffold row u01-rem-close ("Rem CLOSEOUT ...") with the reviewed translation
  from Wave A `tr0.json`: "Now I Will Arise" (Isaiah 33:9–11, Philippians 2:7 cited inline).
  Its translator notes replace the old workroom notes (Melito/SERIES CLOSEOUT lines are gone).
- Applied reviewer retranslations (english and title only) from `rv0.json`:
  u01-open "The Trumpet and the Tomb", u01-rem-early "One Word Made Flesh" (Job 38:17 added),
  u01-rem-mid "The Angel and the Prophets" (Mark 16:6; Matthew 28:6; Hosea 6:1–2; Isaiah 33:9).
- One clarity edit beyond the reviewer text, meaning unchanged: u01-rem-early "appear to the
  women in white" became "appear in white to the women" (λευχείμονες describes the angels).
- Justification `reviews/justifications/u01_rem_close.json` rewritten (English Pass A, Greek
  lemma tags, bible_refs, choices, review_notes).
- Both `*_meta.json`: blurb, first_english_note and text_history.method rewritten in plain
  English with "fresh English translation" wording; status stays "available". No scope set
  (whole work).
- Checks: `check_pass_ab` ok=4 fail=0; `--tip-ready` ok on both pairs;
  `work_lint --slug hesychius-homilia-ii-pascha` findings=0; no placeholder strings left.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/hesychius-homilia-ii-pascha/backup/`.
- Not committed.

### Open

- Old machine-draft translator notes still sit on u01-open, u01-rem-early and u01-rem-mid, and
  some contradict the new English (u01-open claims an OCR "mu nu" error and renders πρόξενον
  "herald"; the others call the text a "literal rendering" of a fragment). The reviewer
  `rv0.json` carries replacement notes for all three; apply them.
- Justifications for the three reviewed rows (u01_open, u01_rem_early, u01_rem_mid) still hold
  the old pass_b_english and machine-draft choices (u01_open glosses σφῦρα as "anvil").
- `book.yml` still has `status: series-closeout`, a workroom `scope` line and workroom `notes`.
- The `.docx` predates this English and needs a rebuild.

## 2026-10-24 — follow-up cleanup (Claude, Mini)

- English text unchanged. No check forced a structural fix.
- Translator notes: all four rows now carry only notes true of the current English. u01-open,
  u01-rem-early and u01-rem-mid use the `rv0.json` replacement notes, reworded so they name
  "the previous / next section" instead of row ids and no longer describe the replaced wording
  (the "not 'flint'" aside is gone). u01-rem-close lost two notes: the soft-hyphen and page-number
  note (kept in the justification's `source_normalizations`) and the "capitalised as divine names"
  line; its first note no longer names u01-rem-mid.
- Justifications u01_open, u01_rem_early, u01_rem_mid: `pass_b_english` set to the current
  English; Pass A glosses, lemmas, choices and bible_refs rewritten from the Greek `source_text`
  (σφῦρα 'hammer', ἄκμων 'anvil', ἐπύρωσεν 'tempered in fire'; ὡς θεὸς 'as God'; ἐκυλίσαμεν
  'we rolled away'; Mark 16:6, Matthew 28:6, Hosea 6:1–2, Isaiah 33:9, Job 38:17 refs).
  `anf_compare` set to no_pd_reference, reviewer and a revisions entry point to the Wave A
  review (`rv0.json`), `lemma_constraint` pass. u01_rem_close was already current; not changed.
- `intro.md` rewritten to match the English: "tempered in fire" (not "ignited"), the bridal
  chamber where the bridegroom slept three days (not "buried"), "the Word made flesh" (not
  "Logos"), and the Isaiah close and doxology added; the "not Homily I" line removed.
- `book.yml`: status available (matches the metas), scope "The whole homily, from the opening to
  the closing doxology.", workroom notes replaced with a plain source note, description in
  "fresh English translation" wording. Author and edition kept as in the metas.
- Checks: `check_pass_ab` ok=4 fail=0; `--tip-ready` ok on both pairs;
  `work_lint --slug hesychius-homilia-ii-pascha` findings=0.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/hesychius-homilia-ii-pascha/backup-cleanup/`.
- Not committed.

### Open

- The `.docx` still predates this English and needs a rebuild.
- The source header reads "Homilia ii in sanctum pascha (homilia 4) (e cod. Sinaitico gr. 492)".
  The "PG 93" edition label in book.yml and the metas was kept as found and was not checked
  against a PG 93 page tonight.
