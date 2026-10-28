# Session handoff: Dialogue with Nestorius (cyril-alexandria-dialogus-nestorio)

## 2026-10-24 (Wave A assembly, Claude)

- All four sections are now real English (PG 76, cols. 249-253).
- Replaced the two scaffold rows with reviewed translations from Wave A `tr0.json`:
  dial-rem-early "The Child Born of the Virgin Is God", dial-rem-mid "One Son, of One Substance
  with His Mother". The staged rows in `rv0.json` match `tr0.json`.
- Applied reviewer retranslations (english) from `rv0.json` to dial-open and dial-rem-close:
  dropped "or of his death" restored, "as he breathed" corrected to "just as he said", the added
  "Mother of God" gloss removed, the dropped Nestorius/Cyril speaker labels in dial-rem-close
  restored, citations added (Galatians 4:4, Psalm 82:6, Hebrews 9:28, 1 Peter 2:22, John 6:56-57,
  John 6:50-51; 8:52). Titles unchanged.
- One change of my own after checking the Greek: dial-rem-mid ἀχώριστος now "inseparable" (was
  "not separated"), in the English and the justification.
- translator_notes replaced on all four rows: the scaffold rows carried workroom lines (OET /
  Melito / densify / Pusey), and the old dial-open and dial-rem-close notes contradicted the
  corrected English (rv0 asked for the dial-open note to be corrected). New notes come from the
  tr0 notes and the rv0 `why` text.
- Justifications rewritten for dial_rem_early and dial_rem_mid (English Pass A with a few key
  Greek terms, Greek lemma tags in lemmas[], bible_refs, choices, review_notes, source sha256,
  source_text copied exactly from the source file).
- Both `*_meta.json`: blurb and text_history rewritten in plain English with "fresh English
  translation" wording; scope added (PG 76 cols. 249-253, breaks off mid-sentence); the old
  first_english_note (SERIES CLOSEOUT / OET wording) removed; first_english set to false, since
  "first English" was claimed only from absence in ANF/NPNF, which the QA rules forbid. Status
  stays "available".
- Checks: `check_pass_ab` on reviews/justifications ok=4 fail=0; `--tip-ready` ok on both pairs;
  `work_lint --slug cyril-alexandria-dialogus-nestorio` findings=0; no placeholder strings left in
  translations/*_english.json; titles clean.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-dialogus-nestorio/backup/`.
- Not committed.

### Open

- Justifications dial_open and dial_rem_close still hold the old machine-draft pass_b_english,
  choices and bible_refs (dial_rem_close has a "Full Book chapter:verse" template ref; dial_open
  keeps "in womb"). Rewrite them from the rv0 English.
- `book.yml` still says `status: series-closeout` with a workroom `scope` and `notes` (OET,
  Melito, Pusey) and a description saying "New English"; `intro.md` still quotes the old Isaiah
  wording ("shall conceive"). Bring them in line with the meta files.
- The locked text stops at PG 76 col. 253 mid-sentence; the end of the dialogue is not in the
  locked file. Check the Khazarzar PDF for the remaining lines.
- Authorship: the dialogue is printed among Cyril's works; whether CPG lists it among the
  genuine works or the spuria was not checked this session.

## 2026-10-24 (follow-up cleanup, Claude)

- intro.md rewritten to match the English rows and metas: "printed among the works of Cyril"
  (as the metas say), PG 76 cols. 249-253, the whole run of exchanges (not "two exchanges in this
  file"), Isaiah quoted as in the English ("will conceive ... they will call"), Cyril's reply as
  "the life-giving flesh of the life-giving Word" and "never taste death", and a line that the
  text breaks off in Cyril's reply.
- translator_notes: section-ID cross-references (dial-open, dial-rem-early, ...) changed to
  "the previous/next section"; "where the locked text ends" now "where the text translated here
  ends"; the dial-rem-close speaker-label note reworded so it describes the print, not the fix.
  No other note content changed; English and titles unchanged (checked by script).
- Justifications dial_open and dial_rem_close rebuilt on the rv0 English: pass_b_english equals
  the current English; choices, lemmas and bible_refs rewritten (removed "Mother of God", "in
  womb", the "Full Book chapter:verse" template ref, John 6:51/6:54-56; fixed invalid lemmas
  προσενέχω, θεότητα, ἀνθρωπότητα); Pass A rewritten as a literal English sense gloss; anf_compare
  set to no_pd_reference_used, matching the meta text_history. source_text and sha256 untouched.
  dial_rem_early and dial_rem_mid already matched the English; not changed.
- book.yml: status available; scope taken from the metas; notes reduced to the copy-text line
  (workroom lines removed); description in "fresh English translation" wording from the meta blurb.
  Author and edition kept.
- Checks: check_pass_ab ok=4 fail=0; --tip-ready ok on both pairs; work_lint findings=0.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-dialogus-nestorio/backup-cleanup/`.
- Not committed.

### Still open

- `cyril-alexandria-dialogus-nestorio.docx` (Oct 5) still holds the old machine-draft English and
  old intro; rebuild it before the next Logos upload.
- The end of the dialogue past PG 76 col. 253 is not in the source file; check the Khazarzar PDF.
- Authorship (CPG genuine or spurious) still unchecked; intro and book.yml say only "printed
  among the works of Cyril", as the metas do.
