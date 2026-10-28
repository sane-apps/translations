# Session handoff: Letter to Calosyrius (cyril-alexandria-ad-calosyrium)

## 2026-10-24 (Wave A assembly, Claude)

- All four sections are now real English: ep-open, ep-rem-early, ep-rem-mid, ep-rem-close.
- Replaced the three scaffold rows in `translations/ac_ep_rem_english.json` with the reviewed
  translations from Wave A `tr0.json`: ep-rem-early "God Has No Body or Shape", ep-rem-mid "What
  the Image of God Means", ep-rem-close "The Image Is Not the Body's Shape". The staged rows in
  `rv0.json` (early, mid) match `tr0.json` word for word; the script asserted this before writing.
- Applied the reviewer retranslation from `rv0.json` to ep-open (english and title): superscription
  restored, "out of ignorance" and "not embodied" restored, "was made" (past), "the utmost
  impiety", the subject of the spread talk corrected, Genesis 1:27 and John 4:24 cited inline,
  "Calamon" for the mountain. New title "Monks Who Say God Has Human Form".
- translator_notes replaced on all four rows. The scaffold rows carried workroom lines (OET,
  Melito, densify, Pusey); the old ep-open notes contradicted the Greek ("last age of apostasy",
  "ends mid-sentence"), and rv0 asked for them to be dropped. New notes come from the tr0 notes
  and the rv0 `why` text, with "row" wording changed to "section".
- Justifications rewritten for all four sections (ep_open, ep_rem_early, ep_rem_mid,
  ep_rem_close; file names follow the book adapter: section with dashes as underscores). Each has
  an English Pass A with a few key Greek terms, Greek lemma tags in lemmas[], bible_refs, choices,
  review_notes, source sha256, source_text copied exactly from the source file, and
  pass_b_english equal to the live English. ep_open was rewritten too, because its pass_b_english
  no longer matched the corrected English and its lemma tags had errors (ἐφίκνομαι, ἀσύνητος,
  ἄσωμος).
- Both `*_meta.json`: blurb rewritten in plain English with "fresh English translation" wording;
  the SERIES CLOSEOUT / OET first_english_note removed; first_english set to false (it was
  claimed only from absence in ANF/NPNF); text_history.method rewritten; scope added (first part
  of the letter, on the image of God; the rest is not yet translated). Status stays "available".
- Checks: `check_pass_ab` on reviews/justifications ok=4 fail=0; `--tip-ready` ok on both pairs;
  `work_lint --slug cyril-alexandria-ad-calosyrium` findings=0; no placeholder or workroom strings
  in translations/*_english.json, *_meta.json or the justifications; titles clean.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-ad-calosyrium/backup/`.
- No reviewer holds. Not committed.

### Open

- The letter is incomplete on the site. The locked sections stop at "They are mad to say this"
  (the Greek goes on with οὐ γὰρ). The rest of the letter is already in
  `sources/ad_calosyrium_pg.txt`: the reserved Eucharist ("Christ is not altered"), monks who
  refuse to work, the Melitians, the order to read the letter in the monasteries, and the closing
  greeting. Lock it as new sections in `ac_ep_rem_source.json` (or a new pair) and translate it,
  then drop the "not yet translated" line from `scope`.
- `book.yml` still says `status: series-closeout` with a workroom `scope` ("SERIES CLOSEOUT
  e47599be; true OET.") and `notes` (OET, Melito, Pusey). Outside this task's file list; bring it
  in line with the meta files.
- The page numbers 604-607 inside the Greek look like the Pusey edition's pages, not PG columns;
  the scope does not cite column numbers for that reason. Check against the Khazarzar PDF before
  adding a column range.
- Topics in the meta files (christology, hermeneutics-types, ...) were kept as they were; the
  letter is mainly about the image of God and God's bodiless nature.

## 2026-10-24 1:30 AM ET (follow-up cleanup, Claude)

- intro.md: this book has none, so nothing to correct. The site's About this text for
  `cyril-ad-calosyrium` comes from the meta blurb, scope and text history, which already match the
  English. No intro.md was added: the site maps intros by site slug, so one here would not show.
- translator_notes: section ids (ep-open, ep-rem-early, ep-rem-mid, ep-rem-close) inside the notes
  replaced with plain words ("the previous section", "the next section", "the opening section"),
  since notes reach the downloads. Nine notes changed; no note described replaced wording or
  carried workroom words. English text unchanged.
- Justifications: pass_b_english already equals the current English in all four files; glosses
  and choices do not contradict it. Not changed.
- book.yml: status `available`; workroom scope and notes (SERIES CLOSEOUT, OET, Melito, Pusey)
  replaced with a reader-facing scope matching the metas and a one-line copy-text note; English
  title "Letter to Calosyrius" with original_title "Ad Calosyrium"; description added in "fresh
  English translation" wording. Author (Cyril) and edition (PG 76; CPG 5230) kept.
- Checks: check_pass_ab ok=4 fail=0; --tip-ready ok on both pairs; work_lint findings=0;
  library_sync gate 0 of 7 files with worksheet notes.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-ad-calosyrium/backup-cleanup/`.
- Not committed.

### Still open

- The rest of the letter (reserved Eucharist, idle monks, Melitians, closing greeting) is not yet
  translated; see the entry above.
- The English rows and metas carry `claim` ids ending in `-oet` (an internal id, not shown to
  readers). Left as is so the claim ledger still matches.
