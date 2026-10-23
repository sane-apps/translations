# Gregory Thaumaturgus: Ecclesiastes metaphrase — production ledger

Canonical path: `~/SaneApps/clients/translations/books/gregory-thaumaturgus-ecclesiastes-metaphrase/`

## Charter

- Title: Gregory Thaumaturgus: Ecclesiastes metaphrase
- Author: Gregory Thaumaturgus
- Scope: (fill)
- Legal: private study; new English from allowed sources; no modern copyrighted English copy.

## State

- Sources: not started
- Translations: not started
- DOCX: not built
- Logos Build: not compiled
- Bible-link verify: not done

## Next

Follow `docs/SOP.md`.

## 2026-09-15 (Grok Bot — tip-ready + live ship)

- **tip-ready:** PASS for Cap. I opening (Solomon to the Church through Jerusalem consideration).
- **Source locked:** MGR Greek extract (TLG 2063.006 / Documenta Catholica Omnia); PG 10.987–989 cues. Vossius Latin DjVu OCR damaged — check only.
- **Pass A≠B:** justification `reviews/justifications/eccl_1.json` OK (lemmas+choices).
- **DOCX:** `gregory-thaumaturgus-ecclesiastes-metaphrase.docx`; verify_docx OK; Headword TN; inline Bible (Ecclesiastes 1:1-11); no footnotes.xml. Scaffold English.docx discarded.
- **Live:** https://fathers.saneapps.com/works/gregory-thaumaturgus-ecclesiastes-metaphrase/ (200); `/1/` (200). Deploy `1b34f63e.fathers-site.pages.dev`. live_works=42.
- **Claim:** remains **prepped**.
- **Logos:** compile pending on Air.

## 2026-09-15 (CoS / Grok Bot — TN ops-leak cleanup)

- Stripped ops/process theater from `translator_notes` / `notes_covered` (Pass A≠B stamps, Tip densify / scaffold-discarded chatter). Kept scholarly notes (lemma/OCR/scope).
- Cleaned meta blurb/edition/method phrasing of densify/scaffold ops leak; fixed copy-paste panegyricus Title/H1/author hardcodes in `build_book.py` where present.
- Rebuilt DOCX; `pipeline.verify_docx` OK; spot-check: no Pass A / Tip densify / scaffold strings in english JSON or DOCX body.
- TNs: 3→2.
- **Logos gate: CLEAR for Air Personal Book backlog** after this strip (private study).
- **Site:** KEEP live tip (Pass B already ok). Section HTML does not embed Headword TNs; no re-ship this turn (About/meta on live may still show older densify wording until a later packet rebuild).

## 2026-10-23 (Claude — rest of the work translated; whole paraphrase now in English)

- **Translated:** the rest of the work, Ecclesiastes 1:13 to 12:14, as 26 new sections (`1.2`, `2.1`, `2.2`, `3.1` … `11.2`, `12.1`, `12.2`), appended after section `1` in reading order. Section `1` is unchanged. The book now covers the whole paraphrase (chapters 1-12, ending at ΤΕΛΟΣ). Claude drafted from the Greek (Cloudflare AI is off; no outside model or API was called).
- **Pages read:** copy-text is `sources/metaphrasis_MGR_concord.pdf` (MGR / Documenta Catholica Omnia, TLG 2063.006 = PG 10), read from the page images, PDF pages 1-11 of 36, records [00022]-[00363]; PG 10 col. 992-1017. Check witness: `sources/gregory_thaumaturgus_opera_omnia.pdf`, Greek and Latin columns, PDF leaves 103-120 (printed pp. 79-96). The title page (PDF p. 7) reads Paris: Sonnius, Morel and Cramoisy, MDCXXII. So it is the **1622 Paris** print, not "Vossius 1684"; meta `text_history` is corrected. Each source row's `notes` names its records, columns and corrections.
- **Files:** `translations/eccl_metaphrase_source.json` (+26 rows), `translations/eccl_metaphrase_english.json` (+26 rows: title, english, added_allusions, translator_notes, source_ref, orientation, confidence), `reviews/justifications/<section>.json` ×26 (Pass A, lemmas, choices, bible_refs, Pass B, notes, review object, source/English hashes). In the justifications, Pass A has its inline Greek lemma tags moved into `lemmas`. The English gloss is unchanged.
- **Meta / book.yml:** status stays `available`, with no `scope` field because the work is complete. Title is now "Paraphrase of Ecclesiastes" (dropped "(Cap. I tip)"). Blurb, era note, first-English note and edition line are refreshed, and `text_history` has its witnesses, coverage and joins. In book.yml the description now says "the whole paraphrase, Chapters 1-12" and "Fresh English translation"; the edition and copyright lines are updated the same way.
- **Reviewer verdicts:** all 26 sections passed, every clause checked against the Greek, and each `review.changes` lists its edits. The reviewer was a separate Claude pass, so this is the same model family, not a second one.
- **Gates (Mini):** `python3 -m pipeline.check_pass_ab reviews/justifications/` gives ok on all 26 new files. The 2 fails are the old legacy files `eccl_1.json` (hyphen gloss) and `eccl_metaphrase_1.json` (catalogue stub); both are untouched. `--tip-ready` on the english/source pair is ok. A `pipeline.verify_translation_qa` structural packet run (written to scratch, not saved to the repo) gave 0 structural errors and 27/27 coverage.
- **Open doubts (kept in the translator notes):**
  - 3.1: ᾯ τινι οὖν, ἀλλ᾽ ἔστιν may be corrupt (same words in the 1622 print); it is taken as the dative of ὁστισοῦν.
  - 2.2: τέλος is read as the noun "end", not the adverb; 1622 may read εὗρον ὥσπερ οὐδέν, with the same sense.
  - 6.1: τοῦ ὀφθῆναι is read as passive; the 1622 Latin has "videndi".
  - 7.2: ἣ is read for ἢ συγγινώσκει, after the 1622 Latin relative.
  - 7.3: γῆν τινα ("a kind of earth") is in both prints and in the Latin.
  - 8.1: Ἐφίστασθαι … λόγῳ πονηρῷ is obscure; "when wisdom is tested" is kept for ἐξεταζομένη.
  - 10.3: "the only King, rich and great" is capitalized as God, which is an interpretive choice.
  - 12.1: παυσαμένης is taken with περιδρομῆς, and the passage stays obscure.
  - 12.2: τὰ περὶ τὸ προσῆκον is kept as printed, against the 1622 Latin, which implies παρά.
- **Still to do (not done here):**
  - Rebuild the DOCX (`build_book.py` + `verify_docx`); this was not run.
  - Add a site publication-review packet and receipt for sections 1.2-12.2. `publication-review.json` binds only the old tip packet.
  - `intro.md` and `research.json` ("SCOPE: opening of Chapter I") still describe only the opening.
  - Section 1 has no inline Ecclesiastes citations, and its notes say "ANF 4 Crombie", although the prior English is ANF 6.
  - Commit; that is left to the parent.

## 2026-10-23 (Claude, Mini) — stale scope wording fixed

- Row 1 translator note 'Tip covers Cap. A opening only ...' now says the paraphrase continues in sections 1.2-12.2. intro.md, research.json (SCOPE) and work_brief.json (argument + outline) now describe Ecclesiastes 1:1-12:14. Checks: --tip-ready ok, work_lint 0 (legacy eccl_1.json / eccl_metaphrase_1.json fail check_pass_ab, as before).
