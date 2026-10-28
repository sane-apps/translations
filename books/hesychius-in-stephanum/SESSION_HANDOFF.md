# Hesychius of Jerusalem, In sanctum Stephanum — production ledger

Canonical path: `~/SaneApps/clients/translations/books/hesychius-in-stephanum/`

## 2026-10-23 — Wave A assembly (Claude, Mini)

- Whole homily (§§1-28, opening to doxology) is now real English in all 8 sections.
- Replaced the three scaffold rows with reviewed translations from Wave A `tr0.json`:
  u02-open "The Lamb Slain Outside the City", u02-rem-mid "The Judge Who Weighs Our Deeds",
  u02-rem-close "Blood Poured Out in Confession". Their translator notes replace the old
  workroom notes (Melito/SERIES CLOSEOUT lines are gone).
- Applied reviewer retranslations (english and title only) from `rv0`-`rv2`: u01-open
  (title kept, "Praise of Stephen"), u01-rem-early "Prophecy, Not Blasphemy", u01-rem-mid
  "The Day That Was Neither Day nor Night", u01-rem-close "The Heavens Opened",
  u02-rem-early "A Prayer for Safe Passage and for the Jews".
- Boundary: the sentence σφενδόναι λίθων … ἐπηκολούθουν δόγμασιν is rendered whole at the
  end of u01-rem-close; u02-open starts at Ὅπλων ἀποροῦντες.
- One punctuation fix outside the review files: u01-rem-early ended on ";" (work_lint
  boundary error); now ends "Christ…", since the sentence runs on into u01-rem-mid.
- Justifications rewritten for u02_open, u02_rem_mid, u02_rem_close (English Pass A, Greek
  lemma tags, bible_refs, choices, review_notes).
- All four `*_meta.json`: blurb and first_english_note rewritten in plain English with
  "fresh English translation" wording; status stays "available". No scope set (whole work).
- Checks: `check_pass_ab` ok=8 fail=0; `--tip-ready` ok on all four pairs;
  `work_lint --slug hesychius-in-stephanum` findings=0; no placeholder strings left.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/hesychius-in-stephanum/backup/`.
- Not committed.

### Open

- Old machine-draft translator notes still sit on u01-rem-early, u01-rem-mid, u01-rem-close
  and u02-rem-early. Some no longer match the new English (u01-rem-close describes the old
  "sling-stones" rendering; u02-rem-early calls the text a fragment). Replace them with
  notes drawn from the reviewer `why` text.
- Justifications for the five reviewed real rows still hold the old pass_b_english.
- `book.yml` still has `status: series-closeout` and a workroom `scope` line.

## 2026-10-24 — follow-up cleanup (Claude, Mini)

All three open items above are closed. English text unchanged (checked field by field
against the backups).

- `intro.md` did not exist; wrote one (3 short paragraphs, as `book_frontmatter` requires):
  Hesychius and Jerusalem's claim on Stephen; the charge of Acts 6:13-14 answered from
  Micah, Isaiah, David, Moses (Leviticus 26, Deuteronomy 28) and Zechariah 14; the vision,
  stoning and two prayers (Acts 7:56, 7:59-60). Every sentence checked against the English.
- translator_notes, all 8 sections: old machine notes removed (the "sling-stones" note,
  the "fragment" notes, the bogus grammar notes on u01-rem-mid). rv*.json give no
  replacement notes for these sections, so new notes were written from the reviewer `why`
  text: LXX Psalm numbering, LXX wording of Leviticus 26:21 and Zechariah 14, the editor's
  supplement in Matthew 28:4, Hesychius's σκληροκάρδιοι in Acts 7:51, φύραμα, the sentence
  that runs across the u01/u02 break. u02-rem-mid note now quotes the current "Do not lift
  it onto the scale". Section ids and the page-number note taken out of the notes readers see.
- Justifications u01_open, u01_rem_early, u01_rem_mid, u01_rem_close, u02_rem_early:
  pass_b_english = current English; new Pass A sense glosses from the Greek (old ones
  carried the wrong senses the review fixed); lemmas rebuilt with forms copied from
  source_text (edition accents); choices and bible_refs replaced to match the English
  (inline citations and bible_refs agree); anf_compare no_pd_reference; old AI crosscheck
  stamps cleared; review_notes = translator notes. u02_rem_mid: review note fixed and a
  choice added for "lift it onto the scale". u02_open, u02_rem_close: review_notes aligned.
- `book.yml`: status available; workroom scope and notes removed; description in "fresh
  English translation" wording; author and edition kept.
- Checks: `check_pass_ab` ok=8 fail=0; `--tip-ready` ok on all four pairs;
  `work_lint --slug hesychius-in-stephanum` findings=0; `load_frontmatter` reads 3 paragraphs.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/hesychius-in-stephanum/backup-cleanup/`.
- Not committed.

### Open

- Edition label: the source PDF is headed "In sanctum Stephanum (homilia 9)" and prints
  editorial supplements in <…>, which looks like a modern critical text (Aubineau's
  numbering) rather than Migne. Not checked against PG 93 itself; edition label left as is.
