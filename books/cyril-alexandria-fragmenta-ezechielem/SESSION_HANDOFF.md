# Session handoff: cyril-alexandria-fragmenta-ezechielem

## 2026-10-24: Wave A assembly (Claude)

### Done

- Three scaffold rows replaced with the reviewed translation from
  `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-fragmenta-ezechielem/tr0.json`
  (rv0 fixes already staged in tr0): frag-open "The Powers Above and Three Righteous Men",
  frag-rem-early "Noah, Daniel, Job, and the Cedar", frag-rem-mid "Ordinances That Were Not
  Good, and Greedy Shepherds". Title and English set; pass_a_gloss, bible_refs and the review
  fields kept out of the rows.
- frag-rem-close (a real row, unreviewed machine draft) given the rv0 English. The old draft
  reversed the litotes οὐκ ἀνικάνως ("not unconquerably"), dropped the teaching (διδασκαλίαν),
  misread the sheep-and-rams clause and ἀταλαίπωρον, and lost "the Father". Ezekiel 34:18 and
  34:23 now cited inline. Title unchanged ("The Shepherd and the Water").
- translator_notes replaced on all four rows. The scaffold rows carried workroom lines (OET,
  Melito, densify, Pusey), and rv0 called the frag-rem-close note worksheet debris with a wrong
  gloss. New notes come from the tr0 notes and the rv0 `why` text.
- Justifications rewritten for all four sections (frag_open, frag_rem_early, frag_rem_mid,
  frag_rem_close; file names follow the book's existing names, section with dashes as
  underscores). Each has an English Pass A with a few key Greek terms, Greek lemma tags in
  lemmas[], bible_refs, choices, review_notes, source sha256, source_text copied exactly from
  the source file, and pass_b_english equal to the live English. frag_rem_close keeps its draft
  history in revisions[] and corrects the old lemma tags (παιδεία, ποδηγεώ, νόμη).
- Both `*_meta.json`: blurb rewritten in plain English with "fresh English translation" wording;
  the SERIES CLOSEOUT / OET first_english_note removed; first_english set to false (it was
  claimed only from absence in ANF/NPNF, as in the other Cyril books this wave);
  text_history.method rewritten. Status stays "available". No scope line: the four sections
  cover the whole of the fragments as printed in PG 70.
- Checks: `check_pass_ab` on reviews/justifications ok=4 fail=0; `--tip-ready` ok on both pairs;
  `work_lint --slug cyril-alexandria-fragmenta-ezechielem` findings=0; no placeholder or workroom
  strings in translations/*_english.json, *_meta.json or the justifications (the only "oet" hits
  are the `claim` ids); titles clean.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-fragmenta-ezechielem/backup/`.
- No reviewer holds. Not committed.

### Open

- `book.yml` still says `status: series-closeout` with a workroom `scope` ("SERIES CLOSEOUT
  9c8ad8f2 footer-safe; true OET.") and `notes` (OET, Melito, Pusey). Outside this task's file
  list; bring it in line with the meta files.
- Source row titles in `translations/*_source.json` are still scaffold labels ("Fragments rem
  early"); the English titles are the reader-facing ones.
- The printed text names Daniel twice in the list of the dead (frag-open). Kept as printed and
  explained in a translator note; check the catena edition if one becomes available.

## 2026-10-24 (1:35 AM ET): follow-up cleanup (Claude)

### Done

- intro.md: this book has none, so the site shows no "About this text" block and nothing
  could contradict the rows. Not written here (the task was to correct, not to add); see Open.
- translator_notes: checked every note on all four rows against the current English and rv0.
  No note describes replaced wording or a fixed error, and none carries workroom words. Six
  notes named sections by their internal ids (frag-open, frag-rem-early, frag-rem-mid,
  frag-rem-close); those now say "the previous section" / "the next section" (the frag-open
  note names the next section by its title). Meaning unchanged.
- Justifications: pass_b_english already equals the live English on all four sections;
  choices and glosses agree with it. No change.
- book.yml: status series-closeout to available (matches both metas); title now the English
  "Fragments on Ezekiel" with original_title "Fragmenta in Ezechielem", as in the metas;
  workroom scope replaced with "All the Ezekiel fragments printed in PG 70, in four sections.";
  description added in "fresh English translation" wording; workroom notes replaced with the
  copy-text line and a note that catena folio and PG column references are left out of the
  reading text. Author (Cyril of Alexandria) and edition (PG 70) kept; the metas agree.
- No English text changed.
- Checks: check_pass_ab on reviews/justifications ok=4 fail=0; --tip-ready ok on both pairs;
  work_lint --slug cyril-alexandria-fragmenta-ezechielem findings=0.
- Backups: ~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-fragmenta-ezechielem/backup-cleanup/
  (book.yml, SESSION_HANDOFF.md, both *_english.json). Not committed.

### Open

- No intro.md. Sibling Cyril fragment books have a three-paragraph intro (the Logos builder
  requires one). Write one if this book is to show "About this text" or go into a DOCX.
- The `claim` ids in the rows and metas end in "-oet". They are internal keys and not shown;
  left alone.
- Source row titles in translations/*_source.json are still scaffold labels (unchanged).
