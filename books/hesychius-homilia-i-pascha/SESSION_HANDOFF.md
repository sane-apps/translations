# Hesychius of Jerusalem, Homily I on the Holy Pascha — production ledger

Canonical path: `~/SaneApps/clients/translations/books/hesychius-homilia-i-pascha/`

## 2026-10-24 — Wave A assembly (Claude, Mini)

- Whole homily (superscription to doxology, one unit, four sections) is now real English.
- Replaced the three scaffold rows in `hhip_u01_rem_english.json` ("Rem early:", "Rem mid:",
  "Rem CLOSEOUT") with the reviewed translations from Wave A `tr0.json`:
  u01-rem-early "The Wood of the Cross" (1 Corinthians 1:23, Exodus 14:23–28, Genesis 3:6,
  Luke 23:43), u01-rem-mid "Remember Me in Your Kingdom" (Luke 23:42–43, Psalm 24:7 from
  LXX 23:7), u01-rem-close "The Lord Risen and Enthroned" (Isaiah 35:10, Romans 11:34 with
  Isaiah 40:13, Hebrews 2:13 with Isaiah 8:18, Psalm 110:1 from LXX 109:1). Their translator
  notes replace the old workroom notes (Melito / densify / CLOSEOUT lines are gone).
- Applied the reviewer retranslation from `rv0.json` to u01-open, now "The Night of Victory":
  superscription translated, Malachi 4:2 cited, torchlight, "win" for ἀπενεγκώμεθα, the
  lampstand clause restored, and the row now ends "then across the world's…" to join
  u01-rem-early. The reviewer said the old translator note on this row was wrong (it claimed
  the row begins mid-sentence); it was replaced with the reviewer's corrected note.
  The reviewer's fixes to u01-rem-early and u01-rem-close were already made in `tr0.json`.
- Justifications `reviews/justifications/u01_rem_early.json`, `u01_rem_mid.json`,
  `u01_rem_close.json` rewritten in the sibling (Homily II) shape: English Pass A gloss (Greek
  lemma tags moved into `lemmas[]`), choices, bible_refs, source sha256, review_notes.
- Both `*_meta.json`: blurb, first_english_note and text_history.method rewritten in plain
  English with "fresh English translation" wording; status stays "available". No scope set
  (whole work).
- Checks: `check_pass_ab` on the justifications ok=4 fail=0; `--tip-ready` ok on both pairs;
  `work_lint --slug hesychius-homilia-i-pascha` findings=0; no placeholder strings left in
  `translations/*_english.json`; titles carry no worksheet text.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/hesychius-homilia-i-pascha/backup/`.
- Not committed.

### Open

- `reviews/justifications/u01_open.json` still holds the old machine draft (pass_b_english,
  a muddled pass_a_gloss, no Malachi 4:2 in bible_refs). It passes `check_pass_ab` but no
  longer matches the English; rewrite it from the new u01-open row.
- `book.yml` still has `status: series-closeout`, a workroom `scope` line, workroom `notes`
  and a description saying "New English for private study".
- The `.docx` predates this English and needs a rebuild.

## 2026-10-24 — follow-up cleanup (Claude, Mini)

- `reviews/justifications/u01_open.json` rewritten from the current u01-open row: pass_b_english
  now equals the English; new English sense gloss of the whole Greek block (superscription to
  τότε τῷ τῆς οἰκουμένης); bible_refs John 16:33, Malachi 4:2 (LXX 3:20), Matthew 5:15; choices
  for τὰ σύμπαντα, ἄστροις καταυγάζεται, ἀπενεγκώμεθα 'win', δᾳδουχίαις 'torchlight', the second
  dative with προσκυνείτω, λυχνία 'lampstand'; 38 lemmas, every form found in the source block
  (fixed φαῖδρος → φαιδρός and the form ἡλίος → ἥλιος). The old machine-draft provenance
  (draft model chain, ai_crosscheck stamps) was dropped because it described the replaced English.
- `intro.md` rewritten: "our God and Savior" (one person, not "God and the Savior"), the John 16:33
  quotation in the row's wording, Hesychius as presbyter "active c. 412–450", and a short line on
  the rest of the homily (the wood of the cross, Rome and Paul, Moses' rod, the thief's prayer from
  Luke 23:42, the day's speech, the Lord seated at the Father's right hand).
- `book.yml`: status `available` (matches both metas); workroom `scope` removed (whole work);
  `notes` now plain copy-text facts; description in "fresh English translation" wording.
- Translator notes on all four English rows re-read against the current English: all are true of
  it and carry no workroom words, so none were changed. English text not changed.
- Checks: `check_pass_ab` ok=4 fail=0; `--tip-ready` ok on both pairs; `work_lint --slug
  hesychius-homilia-i-pascha` findings=0.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/hesychius-homilia-i-pascha/backup-cleanup/`.
- Not committed.

### Open

- The `.docx` still predates this English and needs a rebuild.
- The internal `claim` ids on the rows and metas end in `-oet`; they are keys, not reader text, and
  were left as they are.
