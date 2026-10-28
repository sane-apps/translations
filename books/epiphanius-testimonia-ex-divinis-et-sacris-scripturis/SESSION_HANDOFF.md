# Session handoff: Epiphanius, Testimonia ex divinis et sacris scripturis

## 2026-10-24, 1:20 AM ET (follow-up cleanup, Claude)

What changed (not committed; no English text changed):

- `intro.md`: none exists for this book, so nothing to correct. "About this text"
  comes from the metas (`text_history`, `first_english_note`), which already use
  "fresh English translation".
- translator_notes on all 12 English rows rewritten. rv1's notes used for the three
  u01-rem rows, minus the process note ("No external model or API used…") and the
  bits about the earlier English. The other eight rows got short notes taken from the
  rv2-rv4 source notes and checked against the current English (Psalm numbering,
  edition slips, attributions kept with true citations, section breaks). u01-open notes
  reworded: no row IDs, no "extraction"/"pin.1.1" wording, no ".t" labels.
- 11 justifications rebuilt (all but u01_open, done earlier): `pass_b_english` = current
  English; a new full Pass A gloss of every clause in the locked Greek; lemmas with forms
  as spelled in the source (all checked present); choices and variants that match the
  English; bible_refs taken from the inline citations; confidence `source_verified`,
  with the reviewer named as one model family and no human review. Old machine-draft
  history moved under `superseded_draft`.
- `book.yml`: status `available`; scope set to a short reader line (complete, 102
  chapters); description in "fresh English translation" wording; workroom notes
  replaced; author and edition kept as the metas give them.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/epiphanius-testimonia-ex-divinis-et-sacris-scripturis/backup-cleanup/`.

Checks: `check_pass_ab` on the justifications ok=12 fail=0; `--tip-ready` ok on all six
pairs; `work_lint --slug epiphanius-testimonia-ex-divinis-et-sacris-scripturis` findings=0;
every justification's source sha256 matches its source file.

Still open:

- Psalm numbers in the running text are still mixed: u01 rows keep Epiphanius's Greek
  numbers; u02 and u03 rows give the English numbers. Each row's notes now say which
  rule it uses, so nothing is false, but one rule for the whole book would be better.
  That means an English edit, so it was left alone.
- Authorship and "first English", unverified, from memory only: modern scholarship
  usually treats this work as pseudo-Epiphanius, and I recall a published Greek-English
  edition (R. V. Hotchkiss, *A Pseudo-Epiphanius Testimony Book*, Scholars Press, 1974).
  If that holds, the metas' `first_english: true` is wrong and the author line needs a
  "Pseudo-" or attributed-to wording. Check two sources before changing anything.
- Source rows still have titles like "Unit 1"; meta `claim` IDs still end in "-oet"
  (internal only).

## 2026-10-24 (Wave A assembly, Claude)

What changed (not committed):

- `epi24_u01_open_english.json` u01-open: the placeholder row ("Lemma-led open" plus
  raw Greek) was replaced with the reviewed translation of the title and chapter
  headings 1-94 (`tr0.json`, reviewed in `rv0.json`). Title "Title and Chapter List".
  The old workroom translator_notes were replaced with the reviewed notes. Two were
  trimmed: the "No external model or API was used" note (process detail), and the
  sentence saying u01-rem-early did not yet join cleanly, because the rv1 fix of
  u01-rem-early now opens "…world, and that judgment will be given to Him".
- Reviewer fixes (english and title only) applied to the other 11 rows:
  u01-rem-early/mid/close (`rv1.json`), u02-open (`rv2.json`),
  u02-rem-early/mid/close (`rv3.json`), u03-open, u03-rem-early/mid/close (`rv4.json`).
  All were full retranslations of loose machine paraphrases with wrong verse numbers.
- `reviews/justifications/u01_open.json` rewritten: English Pass A, 48 Greek lemmas
  (forms spelled as in the locked source), 15 choices, bible_refs, variants, review notes.
- All six `*_meta.json`: blurb, first_english_note and text_history.method cleaned of
  "SERIES CLOSEOUT" / "OET" lane wording; blurb now uses "fresh English translation".
  Status was already "available". No `scope` set: the source runs to heading 102, the
  end of the work.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/epiphanius-testimonia-ex-divinis-et-sacris-scripturis/backup/`.

Checks: `check_pass_ab` on all 12 justifications ok=12 fail=0; `--tip-ready` ok on all
six english/source pairs; `work_lint --slug epiphanius-testimonia-ex-divinis-et-sacris-scripturis`
findings=0; no placeholder strings in `translations/*_english.json`; no workroom words
in titles or meta.

Left open (outside this task's write list):

- Psalm numbers in the running text are not uniform. u01-rem-early and u01-rem-close
  keep Epiphanius's Greek (LXX) numbers ("in Psalm 109 … (Psalm 110:3)"); u02 and u03
  rows give the Hebrew number in the text too ("in the 82nd Psalm" where the Greek
  has πα', 81). The parenthetical citations are right in both. Pick one rule and
  apply it across the book.
- translator_notes on the 11 reviewer-fixed rows still describe the old renderings
  and some now contradict the English (u01-rem-early says Habakkuk 3:3 "was removed",
  which rv1 restored; u02-rem-close says "Some biblical references may be
  mistranslated"). rv1 supplied replacement notes for its three rows; the other rows
  need notes trimmed or rewritten.
- Justifications for those 11 rows still hold the old machine-draft pass_b_english,
  lemmas and choices (confidence "machine_draft"). Rebuild them from the new English.
- `book.yml` still has `status: series-closeout`, `scope: "SERIES CLOSEOUT 5152ad11;
  true OET."` and workroom notes.
- Source rows still carry titles like "Unit 1".
