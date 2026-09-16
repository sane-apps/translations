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
