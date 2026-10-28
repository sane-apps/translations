# Hesychius, In sanctum Andream — session handoff

## 2026-10-23 (Wave A assembly, Claude)

Done (not committed):
- Filled the two placeholder rows in `translations/hia_u02_rem_english.json`
  (u02-rem-early "Raised Above Kings and Stars", u02-rem-close "Fish for the
  Master's Table") from the reviewed Wave A translation (`tr0.json`). Old
  scaffold translator notes replaced with the translation's notes.
- Applied reviewer fixes (english + title only) to u01-open (`rv0.json`) and
  u01-rem-early, u01-rem-mid, u01-rem-close, u02-open, u02-rem-mid (`rv1.json`).
  The old rows dropped large parts of the Greek, cited wrong verses and spelled
  Andrew "Andreas". u01-open pronouns set to lowercase he/him/his for Christ to
  match the other seven sections (no change of meaning).
- Rewrote `reviews/justifications/u02_rem_early.json` and `u02_rem_close.json`
  (English Pass A, Greek lemmas, choices, bible_refs, review notes).
- Meta blurb and first_english_note (all four `*_meta.json`) cleaned of
  "SERIES CLOSEOUT" and lane notes; blurb now uses "fresh English translation".
  Status was already "available". No `scope` set: the source is the whole homily.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/hesychius-in-andream/backup/`.

Checks: `check_pass_ab` on all 8 justifications ok=8 fail=0; `--tip-ready` ok on
all four english/source pairs; `work_lint --slug hesychius-in-andream` 0
findings; no placeholder strings in `translations/*_english.json`.

Left open (files outside this task's write list):
- `translator_notes` on the six reviewer-fixed rows still describe the old
  renderings (e.g. u01-open says τὴν λίμνην was rendered "the net"; u01-rem-close
  says sentences "may have been rephrased"). Replace or trim them.
- Justifications for those six rows still hold the old Pass B text.
- `intro.md` still says "Andreas tells Peter" and "David sought God"; both are
  now wrong (Andrew; David "took pride in seeking").
- `book.yml` has `status: series-closeout`, `scope: "SERIES CLOSEOUT 978834f3;
  true OET."` and "New English" in `description`.
- `hia_u02_rem_source.json` section titles are still "Unit 2 rem early/mid/close".

## 2026-10-24 (follow-up cleanup, Claude)

Done (not committed; English text unchanged, checked against the backup):
- `intro.md`: rewritten in three short paragraphs to match the current English:
  Andrew (not "Andreas"); David "took pride in seeking" God; Hosea's two days and
  third day; Romans 9:16 wording dropped; the close is the prayer that the
  apostles' light shine into our minds and that we become fish in their heavenly
  net for the Master's table (not "the light of heaven").
- `translator_notes` on all eight English rows replaced. Gone: notes on old
  renderings ("the net" for λίμνη, "may have been rephrased", "of the heavens
  is", "disciplining"), OCR split-word notes, and section ids. Kept or added only
  reader notes: heading lines, Greek Psalter numbering, Greek Old Testament forms
  (Isaiah 21:12, Proverbs 17:17, "paradise of delight"), Hosea 6:3 quoted with
  both εὑρήκαμεν and εὑρήσομεν, χοῦν "dust" rendered "chaff" after Hosea 13:3,
  John 14:6 in Hesychius's order, εὐγνωμοσύνη "good judgment" (or "gratitude"),
  doubtful readings, possible echoes not cited inline, and section joins.
- Justifications u01_open, u01_rem_early, u01_rem_mid, u01_rem_close, u02_open,
  u02_rem_mid rebuilt: pass_b_english = current English; new clause-by-clause
  English Pass A; lemmas spelled as printed (oxia accents) and all found in the
  source; choices and bible_refs match the inline citations (old wrong refs such
  as Joel 2:23, Isaiah 7:14, Matthew 16:18 gone); old machine-draft stamps
  removed, with a `history` line pointing to the backup.
- `book.yml`: status available; scope "The whole homily, as printed in PG 93."
  (the eight source sections cover the whole PG text, checked by Greek letter
  count); notes and description in plain words with "fresh English translation".
  Author and edition unchanged.
- All four metas: `text_history.method` no longer says "OET".

Checks: `check_pass_ab` on reviews/justifications ok=8 fail=0; `--tip-ready` ok
on all four pairs; `work_lint --slug hesychius-in-andream` findings=0; workroom
word scan of intro, book.yml, titles, notes and metas clean.

Backups and the script used: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/hesychius-in-andream/backup-cleanup/`.

Still open:
- `hia_u02_rem_source.json` and the other source files keep titles like
  "Unit 2 rem early". Not changed: editing a source file changes the sha256 that
  every justification records.
- `confidence: source_verified` on the six rebuilt justifications rests on a
  same-model-family check (the reviewer who retranslated and this pass are both
  Claude). No independent model has checked this work.
