# Ad episcopos Libyae et Pentapoleos (Cyril of Alexandria) — production ledger

Canonical path: `~/SaneApps/clients/translations/books/cyril-alexandria-ad-episcopos-libyae/`

## 2026-10-24 — Wave A assembly (Claude, Mini)

- All four sections are now real English, covering the whole letter as printed in PG 77
  (preface, headings (α)-(γ), the heading printed "Ε", and the closing greeting).
- Replaced the three scaffold rows with reviewed translations from Wave A `tr0.json`:
  ep-open "What the Monks of the Thebaid Reported", ep-rem-early "Hasty Ordinations and Expelled
  Monks", ep-rem-mid "Examining Candidates Before Ordination". The staged rows in `rv0.json` match
  `tr0.json` exactly.
- Applied the reviewer retranslation (english and title) from `rv0.json` to ep-rem-close, now
  "Catechumens and Penitents Near Death". The old machine draft (2026-09-30) dropped the separation
  clause, mistranslated πταισμάτων and κατηχούμενοι ὄντες, turned a command into a purpose clause,
  and closed with a wrong greeting carrying an invented 1 Corinthians 1:10 citation.
- translator_notes replaced on all four rows: the scaffold rows carried workroom lines (Melito /
  densify / Pusey / OET), and the old ep-rem-close notes were false ("σεπτήν rendered as rotten").
  New notes come from the tr0 notes and the rv0 `why` text.
- Scripture: Leviticus 15:31 quoted in ep-open, checked against the LXX, cited inline. A possible
  echo of 1 Timothy 3:10 in ep-rem-mid is uncertain and left uncited (noted).
- Justifications rewritten for all four sections (ep_open, ep_rem_early, ep_rem_mid,
  ep_rem_close): English Pass A, Greek lemma tags in lemmas[], choices, bible_refs, review_notes,
  source text and sha256 from the locked source files.
- Both `*_meta.json`: blurb rewritten in plain English with "fresh English translation" wording;
  text_history method rewritten; the old first_english_note (SERIES CLOSEOUT / OET wording)
  removed; first_english set to false, since this canonical letter is likely already in English
  (Cyril's Letters in the Fathers of the Church series; the canons in The Rudder). Not checked
  online, so the site no longer claims a first. Status stays "available". No scope line: the letter
  is complete.
- Checks: `check_pass_ab` on reviews/justifications ok=4 fail=0; `--tip-ready` ok on both pairs;
  `work_lint --slug cyril-alexandria-ad-episcopos-libyae` findings=0; no placeholder strings left
  in translations/*_english.json; titles are plain English.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-ad-episcopos-libyae/backup/`.
- Not committed.

### Open

- `book.yml` still says `status: series-closeout` and `scope: "SERIES CLOSEOUT 2eb0d458; true OET."`
  with workroom notes. Not in this task's file list; clean it in a later pass.
- Meta topics (christology, father-son-spirit, hermeneutics-types) do not fit a letter on
  ordination and the dying; church-life fits. Left as is.

## 2026-10-24 — Follow-up cleanup (Claude, Mini)

- intro.md: this book has none, and the site work slug (`cyril-ad-episcopos-libyae`) has no
  intro mapping in build_site.py, so "About this text" comes from the metas. Nothing to correct;
  none created.
- translator_notes: the four copy-text lines named the scan site and PDF file name, and the
  ep-open one said "The Latin file label at the top of the source block is not translated".
  Each is now "Copy-text: the Greek text printed in PG 77." plus its page-marker note where it had
  one. All other notes checked against the current English and kept: they are true and useful
  (headings, Leviticus 15:31 LXX wording, the uncertain 1 Timothy 3:10 echo, grammar choices).
- Justifications: no English changed in this pass. pass_b_english already equals the current
  English in all four files; every choice's English appears in it; lemmas and glosses agree.
  No edits.
- book.yml: title now the English title the metas use, with `original_title`; description added
  in "fresh English translation" wording; `status: available`; scope removed (the letter is
  complete); workroom notes replaced by the copy-text line and the letter's contents.
  Author and edition kept (Cyril of Alexandria; PG 77).
- English text unchanged. The internal `claim` ids (`cyril-ael-ep-*-oet`) are left as keys;
  readers do not see them.
- Checks: `check_pass_ab` on reviews/justifications ok=4 fail=0; `--tip-ready` ok on both pairs;
  `work_lint --slug cyril-alexandria-ad-episcopos-libyae` findings=0.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-ad-episcopos-libyae/backup-cleanup/`.
- Not committed.

### Still open

- Meta topics (christology, father-son-spirit, hermeneutics-types) still do not fit this letter;
  church-life fits. Metas were outside this pass's file list.
