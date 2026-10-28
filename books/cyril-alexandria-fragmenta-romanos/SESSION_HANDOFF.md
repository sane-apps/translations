# Fragmenta in epistulam ad Romanos (Cyril of Alexandria, PG 74) — production ledger

Canonical path: `~/SaneApps/clients/translations/books/cyril-alexandria-fragmenta-romanos/`

## 2026-10-24, 1:45 AM ET — follow-up cleanup (Claude, Mini)

- English text unchanged in every row; only translator_notes, justifications and book.yml changed.
- intro.md: this book has none, so the site shows no "About this text" for
  `cyril-fragmenta-romanos` (build_site falls back to `books/<site slug>/intro.md`, and no
  WORK_BOOK_INTRO entry maps it). Nothing to correct; none was written.
- translator_notes (18 rows): workroom lines gone ("Translated by Claude…", "source row …",
  "Check against the printed PG 74 page before certifying", "the review keeps", "US spelling
  follows the other rows", "Unit 5", "now reads", "the bible_refs note"); u04-rem-* take the
  standard copy-text line. Notes that no longer matched the English were corrected: u05-rem-close,
  u06-open and u06-rem-early Spirit/spirit notes now describe only what each row contains;
  u06-rem-mid (Romans 8:10 is quoted only as "the spirit is life"); u06-rem-close ("the things he
  has promised"); u07-open (Psalm 49:12 wording); u08-open (dropped the replaced-wording clause);
  u08-rem-early (the ὡς is not rendered "as in faith"); u09-open and u11-rem-mid ("words of economy"
  / "as elsewhere" no longer true after the u10-open fix); u11-rem-close (there is no next unit).
  A script check confirms every "rendered '…'" claim in the notes appears in its row's English.
- Justifications: the 12 stale files (u01_*, u02_open, u02_rem_early, u02_rem_mid, u10_*,
  u11_rem_early) are rebuilt. pass_b_english = current English; fresh Pass A glosses written from
  the PG 74 Greek in source order (Pass A/B similarity 0.52-0.68); lemmas with corrected headwords,
  every form checked against the section's Greek; choices checked against the English;
  bible_refs read from the English citations; stale ai_crosscheck fields removed. The 18 other
  files carry the same note fixes in choices/review_notes. All 44 now have pass_b_english equal
  to the English.
- book.yml: status available; scope and description now match the metas ("fresh English
  translation"); workroom scope and notes removed; author and edition kept.
- Checks: check_pass_ab ok=44 fail=0; --tip-ready ok on all 22 pairs; work_lint 0 errors,
  2 deliberate warnings ([died], [without toil]).
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-fragmenta-romanos/backup-cleanup/`.
  Scripts and specs: `…/cyril-alexandria-fragmenta-romanos/cleanup/` (build_just.py, fix_notes.py, specs/).
- Still open: first_english unchecked; u09-rem-mid and u11-rem-mid spot check against the Greek;
  the new Pass A glosses are Claude's own and have had no second reader. Not committed.

## 2026-10-24 — Wave A assembly (Claude, Mini)

- All 44 sections (u01-u11, Romans 1 to 15) now carry real English. No placeholder rows remain.
- Replaced 32 scaffold rows with the reviewed Wave A translations from `tr0.json`-`tr9.json`
  (u02-rem-close; all of u03-u09; u11-open, u11-rem-mid, u11-rem-close). The staged rows in
  `rv1.json`-`rv9.json` match the `tr` files word for word. The reviewer left no holds.
- Applied the reviewer retranslations (english and title) to the 12 rows that were already real:
  u01-open, u01-rem-early, u01-rem-mid, u01-rem-close, u02-open, u02-rem-early, u02-rem-mid,
  u10-open, u10-rem-early, u10-rem-mid, u10-rem-close, u11-rem-early. The old drafts had wrong
  senses, reversed agency and whole missing halves (see the `why` text in each `rv` file).
- Seam fix u02-open / u02-rem-early, which rv0 asked for: u02-open already ends "…had brought to
  completion the…", so u02-rem-early now opens "…mystery of the dispensation in the flesh." The
  doubled verb "and had carried through" is gone. The Greek seam is καὶ τῆς | μετὰ σαρκὸς
  οἰκονομίας διαπεράναντος τὸ μυστήριον.
- translator_notes: on the 32 new rows they now come from the `tr` notes, without workroom lines
  (spelling or pronoun conventions, "Review fix:", "flagged for review", the scaffold-title
  remarks). On the 12 fixed rows the old notes described the discarded drafts ("guardrails",
  "equal refuse", "inclusive language"), and the reviewers said to drop them. New short notes
  come from the reviewers' `why` text: seams, readings, omitted page numbers.
- House glossary: "Wisdom 9:15" became "Wisdom of Solomon 9:15" in u07-open (english, note and
  bible_refs).
- Justifications: rewrote the 32 scaffold files in `reviews/justifications/` (u02_rem_close,
  u03_*-u09_*, u11_open, u11_rem_mid, u11_rem_close). Each has an English Pass A, Greek lemma tags
  in lemmas[] (608 tags in all, each form checked against the section's source Greek), bible_refs
  from the translator, choices taken from the translator notes (each rendering checked against the
  English), review notes, and the source file sha256. Structural repairs to Pass A, meaning
  unchanged, are recorded in each file's review_notes. Word-join hyphens in 6 glosses became
  spaces. Greek tags were trimmed in 2 glosses. In u05-rem-early and u05-rem-mid the Greek words
  left in the gloss are now given in English, in the same clause order.
- All 22 `*_meta.json`: the blurb said "SERIES CLOSEOUT on this page". It now reads as plain
  English with "fresh English translation" wording. The first_english_note and
  text_history.method lost the OET, Greystone/Pusey and SERIES CLOSEOUT wording. A new reader
  `scope` reads: "The surviving fragments of Cyril's commentary on Romans, as printed in PG 74,
  on Romans 1 to 15. Many fragments begin or end mid-sentence." Status stays "available".
- Checks (Mini): `python3 -m pipeline.check_pass_ab books/cyril-alexandria-fragmenta-romanos/reviews/justifications`
  gives ok=44 fail=0. `--tip-ready` passes on all 22 english/source pairs. A grep for "Lemma-led
  open", "Rem early:", "Rem mid:", "Rem closeout:" (any case) and "lemma and argument toward the
  thesis" finds nothing in translations/*_english.json. No workroom text in titles, english or
  translator_notes. `pipeline.work_lint --slug cyril-alexandria-fragmenta-romanos` leaves 2 warnings,
  both deliberate: "[died]" in u03-rem-early carries over ἀπέθανε from the end of u03-open, and
  "[without toil]" in u06-rem-close is PG's own editorial restoration.
- Backups of every changed file:
  `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-fragmenta-romanos/backup/`.
  Assembly script and inputs (re-runnable):
  `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-fragmenta-romanos/assembly/`.
- Not committed.

### Open

- The justifications for the 12 fixed rows (u01_*, u02_open, u02_rem_early, u02_rem_mid, u10_*,
  u11_rem_early) still hold the old machine-draft Pass A, Pass B, lemmas and choices. They pass
  the gate but no longer match the English. Rewrite them from the rv English.
- `first_english` is still true in every meta file. It has not been checked. English excerpts of
  Cyril on Romans may exist in an anthology (for example the Ancient Christian Commentary on
  Scripture volume on Romans). Check two sources before keeping the flag.
- `book.yml` still says `status: series-closeout`, with a workroom `scope` ("SERIES CLOSEOUT
  4a392d80 footer-safe; true OET.") and workroom notes. That file was outside this task.
- The source files' section titles ("Unit 3 rem early") are workroom labels. They are not
  reader text, and they were left alone.
- The u09-rem-mid and u11-rem-mid translations had no separate reviewer entry in the `rv` files.
  They passed all the gates and the reviewer raised no hold, but a spot check against the Greek
  would help.
