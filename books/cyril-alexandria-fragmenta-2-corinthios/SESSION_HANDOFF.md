# Session handoff: Cyril of Alexandria, Fragments on 2 Corinthians

## 2026-10-23 (wave A assembly, Claude; not committed)

What changed
- Placeholder rows filled with the reviewed translations from
  `websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-fragmenta-2-corinthios/tr0.json`:
  u02-rem-close, u04-rem-mid, u05-open (and u05-rem-early, see below). Each row kept its
  book fields; title, english and translator_notes now come from the translation (the old
  worksheet notes were dropped).
- Reviewer fixes rv0-rv5 applied (english, plus title where the reviewer gave one) to
  u01-open, u01-rem-early/mid/close, u02-open, u02-rem-early/mid, u03-open,
  u03-rem-early/mid/close, u04-open, u04-rem-early/close. Most are full retranslations from
  the PG 74 Greek; the reasons are in each rv file's `why`.
- New justifications: `reviews/justifications/u02_rem_close.json`, `u04_rem_mid.json`,
  `u05_open.json` (pass_a_gloss, lemmas, choices, bible_refs, review_notes). Greek lemma tags
  sit in `lemmas[]`, so the gloss reads as English.
- All `*_meta.json`: status "available"; blurb, first_english_note and text_history.method
  rewritten in plain English ("fresh English translation"; the "SERIES CLOSEOUT"/"OET" worksheet
  wording is gone). No scope: the five units cover all of the PG 74 fragments.

Reviewer hold resolved (u05 duplicate)
- `f2c_u05_rem_source.json` held exactly the Greek of `f2c_u05_open_source.json`, re-split
  into three rows (and the split broke one clause across two rows). Kept u05-open, the
  whole unit in one section. The u05-rem trio (english with u05-rem-early filled and
  rv5 fixes, meta, source) and its justifications were moved to
  `outputs/waveA-20261023/cyril-alexandria-fragmenta-2-corinthios/backup/parked_u05_rem/`.
  The site now loads 17 sections, u01-open through u05-open, once each.

Checks
- `python3 -m pipeline.check_pass_ab reviews/justifications`: ok=18 fail=0 in total
  (17 in the book, plus the parked u05_rem_early).
- `--tip-ready`: ok on all nine pairs (and on the parked u05-rem pair).
- No "Lemma-led open", "Rem early:", "Rem mid:", "Rem closeout:", "Rem CLOSEOUT" or
  "lemma and argument toward the thesis" left in `translations/*_english.json`; no worksheet
  words in titles or metas.
- `build_site.load_cyril_works()` on this book alone: one work, status available, 17
  sections in order.

Left open
- Older justifications for the rv-fixed rows still carry the old pass_b_english and gloss;
  they pass check_pass_ab but no longer match the English. Refresh them when this book next
  gets a review packet.
- translator_notes on the rv-fixed rows are the old machine notes, written for the old
  English. Some (for example u01-open on Matthew 10:20) no longer describe the new text.
- book.yml still says `status: series-closeout` and has a worksheet `scope`; the site reads
  the metas, not book.yml, for this book.
- Backups of every changed file: `outputs/waveA-20261023/cyril-alexandria-fragmenta-2-corinthios/backup/`.

## 2026-10-24 (follow-up cleanup, Claude; not committed)

Closes the three "Left open" items above. No external model or API was called.

What changed
- intro.md: this book has none. The site's "About this text" for `cyril-fragmenta-2-corinthios`
  comes from the metas (blurb, first_english_note, text_history), which already agree with the
  English. Nothing to fix; no intro.md was created.
- translator_notes rewritten on all 17 rows. The old machine notes are gone (generic "may be
  fragmented" lines, the Matthew 10:20 note, the "341"/"347"/"350" notes, the "δυνά 360 μει is OCR
  corruption" note, the "much-god delusion" and "his face Christ" notes, the "guarantee" note).
  Kept or written: Septuagint numbering (Psalms, Isaiah 9:2, Jeremiah 31, Malachi 4:2, Job 4:19,
  Hosea), doubtful readings (εἱρκότων for εἰρηκότων, ἐν ἕξει μικρῷ, causal εἰ, ἀνυπόστατος,
  διὸ οὐ λέγει τοῦτό ἐστιν), section joins, print headings, Migne column numbers. Notes say
  "previous/next section", never section ids; u05-open no longer mentions the parked u05-rem rows.
- reviews/justifications: on the 14 rv-fixed rows, pass_b_english now equals the English, and
  pass_a_gloss was rewritten from the PG 74 Greek as a clause-by-clause gloss with lemma tags that
  matches the reviewed English; lemmas[] rebuilt from those tags; choices rewritten from the rv
  `why` notes (old wrong renderings listed as rejected); bible_refs rebuilt from the inline
  citations. u02_rem_close, u04_rem_mid, u05_open already matched; u05_open review_notes now say
  the u05-rem hold is resolved. A `revisions` entry was added to each changed file. confidence and
  reviewer fields were not touched (still the old machine values on the 14 rows).
- English: the only change is the structural fix work_lint asked for, "Wisdom" written "Wisdom of
  Solomon" in three citations (u03-rem-early, u03-rem-mid, u04-open).
- book.yml: status `available`; reader scope line; description in "fresh English translation"
  wording; worksheet notes replaced by a copy-text line. Note: scripts/build_corpus_catalog.py
  counts only series-closeout/done/verified as complete, so this book now shows as `available`
  there.

Checks
- `python3 -m pipeline.check_pass_ab reviews/justifications`: ok=17 fail=0.
- `--tip-ready`: ok on all nine pairs.
- `python3 -m pipeline.work_lint --slug cyril-alexandria-fragmenta-2-corinthios`: findings=0
  (was 3 glossary errors).
- No workroom words (OET, SERIES CLOSEOUT, Melito, densify, tip, Pass A/B, lane, section ids) in
  English titles, notes or book.yml. `build_site.load_cyril_works()` on this book: status
  available, 17 sections.

Backups and inputs
- Every file changed here, before the change: `outputs/waveA-20261023/cyril-alexandria-fragmenta-2-corinthios/backup-cleanup/`
  (with sha256_before.txt). The patch files and scripts used: `backup-cleanup/cleanup-inputs/`.

Still open
- The 14 refreshed justifications keep confidence `machine_draft` and their old reviewer stamps;
  they need a fresh review receipt before anyone marks them reviewed.
