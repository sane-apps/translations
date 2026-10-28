# Cyril of Alexandria, Fragments on the Song of Songs — production ledger

Canonical path: `~/SaneApps/clients/translations/books/cyril-alexandria-fragmenta-canticum/`

## 2026-10-23 (Claude, wave A assembly; not committed)

- Copy-text: PG 69, Fragmenta in Canticum canticorum (Khazarzar transcription); the three units cover the whole PG text (Song of Songs 1:3 to 8:14), so no part-only scope was set.
- u03 placeholder rows replaced with the reviewed translation (`outputs/waveA-20261023/cyril-alexandria-fragmenta-canticum/tr0.json` in the fathers site repo): u03-open, u03-rem-early, u03-rem-mid, u03-rem-close. Titles, English and translator notes now match the reviewed text; scaffold notes ("Melito skipped", "SERIES CLOSEOUT") are gone from those rows.
- Reviewer fixes applied (rv0, rv1): u01-open, u01-rem-early, u01-rem-mid, u01-rem-close, u02-open, u02-rem-early, u02-rem-mid, u02-rem-close (English and title). Translator notes on those rows were replaced too, because the old notes described the old draft and the reviewer named several as wrong (Εὐώνυμος "right-handed", προσκεῖσθαι "OCR error", "Locked Greek"). rv1 supplied full notes for u02-rem-*; u01-* and u02-open notes were rebuilt from the reviewer's own "why" text.
- Sentence splits across rows: u02-rem-close now finishes the Song of Songs 5:15 sentence, so u03-open starts at "The pillars of the Church". u03-open finishes the sentence whose last words sit at the head of u03-rem-early.
- New justifications: `reviews/justifications/u03_open.json`, `u03_rem_early.json`, `u03_rem_mid.json`, `u03_rem_close.json` (Pass A English gloss, lemmas with source spelling, bible_refs, choices, review notes).
- Meta (all six `*_meta.json`): status stays "available"; blurb, first_english_note and text_history.method rewritten in plain English ("fresh English translation"), dropping "SERIES CLOSEOUT" / "OET".
- Checks: `python3 -m pipeline.check_pass_ab reviews/justifications/` ok=12 fail=0; `--tip-ready` ok on all six english/source pairs; `python3 -m pipeline.work_lint --slug cyril-alexandria-fragmenta-canticum` findings=0; no placeholder strings left in `translations/*_english.json`.
- Backups of every changed file: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-fragmenta-canticum/backup/`.

### Open

- The u01/u02 justification files still hold the old machine-draft Pass B and old lemmas/choices (e.g. "Logos", "knees", "apathy"). They pass the structural gate, but they no longer describe the published English. Refresh them from rv0/rv1 in a later pass.
- `book.yml` `scope` still reads "SERIES CLOSEOUT 4e4f96f3 footer-safe; true OET." and `notes` carry worksheet text. The site reads scope from meta, not book.yml, but Logos `pb_sync` may read book.yml. Clean it before the next Logos build.
- Source files keep scaffold titles ("Unit 3 rem early"); the reader uses the English titles.
- `first_english: true` is unchanged and was not re-verified; the site shows a first-English note only for slugs on its curated list.

## 2026-10-24 (Claude, follow-up cleanup; not committed)

- English text unchanged (checked field by field against the backup). No external model was called.
- intro.md: this book has none, and never had one in git. The site's "About this text" for `cyril-fragmenta-canticum` is built from the metas (blurb, first_english_note, text_history), which already match the English. Nothing to correct. A Logos build that wants an intro will find none; write a 3-paragraph intro.md only if the owner wants one.
- translator_notes (all 12 rows): row labels ("u01-rem-early", "row break", "source row") replaced with "previous/next section"; copy-text lines no longer carry unit labels; the u02-open note about having no opening ellipsis dropped; the u02-rem-early note now quotes the current u02-open wording ("which casts the shadow of the things to come"); the παράκλησις note reworded so it states the sense instead of correcting the old draft; notes added for the stray print numbers '1' (u01-rem-early) and '2' (u01-rem-close). rv1 notes for u02-rem-* kept, with labels changed only.
- Justifications u01_open, u01_rem_early/mid/close, u02_open, u02_rem_early/mid/close: pass_b_english now equals the published English; Pass A rewritten as a literal gloss of the Greek; lemmas (every form checked as a substring of source_text), choices and bible_refs rebuilt to match the English (old "consolation", "knees", "apathy", "Logos", "right-handed", "Full Book chapter:verse" entries gone); confidence "reviewed", anf_compare not_applicable, review block added. u03 files untouched.
- book.yml: status available; scope "All the fragments printed in PG 69, from Song of Songs 1:3 to 8:14."; description added (fresh English translation wording, same as the meta blurb); worksheet notes replaced by one plain line. Author and edition unchanged.
- Checks: `check_pass_ab reviews/justifications/` ok=12 fail=0; `--tip-ready` ok on all six pairs; `work_lint --slug cyril-alexandria-fragmenta-canticum` findings=0.
- Backups: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-fragmenta-canticum/backup-cleanup/`.

### Still open

- `claim` and `baehrens` fields in the English rows still carry unit labels ("cyril-fc-u01-open-oet", "... u01 open"); they are not shown to readers but were left for the claim tooling.
- Source titles still read "Unit N ..." (reader uses English titles).
