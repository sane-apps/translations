# Session handoff: Cyril of Alexandria, Fragments on Kings

## 2026-10-24 (follow-up cleanup, Claude; not committed)

What changed (no English text or title changed)
- intro.md: this book has none, so there was nothing to correct and none was created.
  The site's "About this text" for this work comes from the metas, which already say
  "fresh English translation".
- translator_notes, all 12 rows:
  - Book Three: the old machine notes are gone. b03-open uses the rv0 notes, with one fix
    (the "Book Three." heading is rendered, so the note no longer says the book heading is
    not rendered; columns 688–689). b03-rem-early/mid/close have new notes taken from the
    rv1 `why` fields and the Greek: Ezekiel attribution (words of LXX Obadiah 15, Ezekiel 16:59
    nearest parallel), "calves" for δαμάλεις, bracketed edition readings (πρόξενον, Θεός,
    ἀμελ[λ]ητί), Greek chapter order of 1 Kings 20/21, the Hezekiah comment that fits Uzziah
    (2 Chronicles 26:16–21), Psalm 30:11 = LXX 29:12 (χορόν vs Cyril's χαράν), and the
    page, column and running-header items left out.
  - Books One and Two: notes that described replaced wording were corrected: b01-open
    "made Christ mediator" is now "took Christ as his mediator"; b01-rem-close "'David's' is
    supplied for 'his' twice" now says David is supplied where the Greek has no name or
    pronoun; b02-rem-mid "to wish to be enlisted" is now the current "a wish to be taken into
    Absalom's service", with the point that the feigning covers both infinitives. The
    "checked against the Greek on 2026-10-23" process clauses were dropped (b01-rem-mid,
    b02-rem-mid). Section ids in the notes (b01-rem-mid and so on) are now "the previous
    section" / "the next section".
- Justifications:
  - `b03_open.json`, `b03_rem_early.json`, `b03_rem_mid.json`, `b03_rem_close.json` were
    rebuilt for the reviewed English. pass_b_english is now the current English; the new
    pass_a_gloss is a clause-by-clause gloss from the PG 69 Greek. The update also covers
    lemmas, choices (each choice's English appears in the current text), and bible_refs
    (they match the inline citations exactly). Also updated: review_notes, edition sha256,
    reviewer, and a new revisions entry pointing to rv0/rv1. The stale ai_crosscheck stamps
    for the old English were removed.
  - Books One and Two: review_notes were brought in line with the corrected notes.
    pass_b_english already matched the English, and every choice is present in it.
- book.yml: status available. The worksheet scope and notes are gone. The description now
  matches the meta blurb ("fresh English translation"). Author and edition are unchanged; the
  metas give no other author.

Checks
- `python3 -m pipeline.check_pass_ab books/cyril-alexandria-fragmenta-regum/reviews/justifications`: ok=12 fail=0.
- `--tip-ready`: ok on all six english/source pairs.
- `python3 -m pipeline.work_lint --slug cyril-alexandria-fragmenta-regum`: findings=0.
- No worksheet words in titles, english or translator_notes. The only hits are the internal
  `claim` ids (`cyril-fr-…-oet`), which were not changed because receipts key on them.
- `build_site.load_cyril_works()` on this book alone: six packs, status available.

Left open
- Book One says "heifers" for δαμάλεις (b01-rem-early); Book Three says "calves"
  (b03-rem-early). Each row's note is true for that row, but the next review should pick one
  word.
- The Book Three English writes verse ranges with a hyphen (Deuteronomy 7:3-4, 1 Kings 20:35-36,
  2 Kings 17:25-26), while Books One and Two use an en dash. This is style only and was left
  alone because the English was not to be changed.
- Backups of every file changed today, and their sha256 before the change:
  `websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-fragmenta-regum/backup-cleanup/`.

## 2026-10-23 (wave A assembly, Claude; not committed)

What changed
- Placeholder rows filled with the reviewed translations from
  `websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-fragmenta-regum/tr0.json`:
  b01-open, b01-rem-early/mid/close, b02-open, b02-rem-early/mid/close (Books One and Two).
  Each row kept its book fields; title, english and translator_notes now come from the
  translation (the old worksheet notes were dropped). Two notes that said "reviewer should
  check" now record that the reading was checked against the Greek and kept.
- The staged rv0 fixes for b01-open, b01-rem-close, b02-open, b02-rem-early and b02-rem-mid
  were already in tr0; they were applied again and changed nothing.
- Reviewer fixes applied to the Book Three rows (english and title only): b03-open (rv0),
  b03-rem-early/mid/close (rv1). All four are full retranslations from the PG 69 Greek; the
  reasons are in each rv row's `why`.
- Justifications rewritten for the eight new sections: `reviews/justifications/b01_open.json`,
  `b01_rem_early.json`, `b01_rem_mid.json`, `b01_rem_close.json`, `b02_open.json`,
  `b02_rem_early.json`, `b02_rem_mid.json`, `b02_rem_close.json` (pass_a_gloss, Greek lemma
  tags in `lemmas[]`, choices, bible_refs, review_notes, source sha256). The old files held
  only the placeholder text.
- All six `*_meta.json`: status "available"; blurb, first_english_note and
  text_history.method rewritten in plain English ("fresh English translation"; the
  "SERIES CLOSEOUT"/"OET" worksheet wording is gone). No scope: the six units hold the
  whole PG 69 text of the fragments (only the printed heading is outside them).

Checks
- `python3 -m pipeline.check_pass_ab reviews/justifications`: ok=12 fail=0.
- `--tip-ready`: ok on all six english/source pairs.
- No "Lemma-led open", "Rem early:", "Rem mid:", "Rem closeout:", "Rem CLOSEOUT" or
  "lemma and argument toward the thesis" left in `translations/*_english.json`; no worksheet
  words in titles or metas.
- `build_site.load_cyril_works()` on this book alone: six packs under slug
  cyril-fragmenta-regum, status available, 12 sections b01-open through b03-rem-close.

Left open
- The four Book Three justifications (`b03_*.json`) still carry the old machine pass_b_english
  and gloss; they pass check_pass_ab but no longer match the reviewed English. Refresh them
  when this book next gets a review packet.
- translator_notes on the Book Three rows are the old machine notes, written for the old
  English; some are wrong (b03-open says the text begins mid-sentence). rv0 holds corrected
  notes for b03-open.
- Book One renders δαμάλεις as "heifers" (b01-rem-early, with a note); the Book Three
  retranslation says "calves" for the same calves of Jeroboam. Pick one in the next review.
- book.yml still says `status: series-closeout` and has a worksheet `scope`; the site reads
  the metas, not book.yml, for this book.
- Backups of every changed file and sha256 before the change:
  `outputs/waveA-20261023/cyril-alexandria-fragmenta-regum/backup/`.
