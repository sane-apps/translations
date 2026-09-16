# Gregory Thaumaturgus: Epistula canonica — production ledger

Canonical path: `~/SaneApps/clients/translations/books/gregory-thaumaturgus-epistula-canonica/`

## Charter

- Title: Gregory Thaumaturgus: Epistula canonica
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

## 2026-09-15 (Grok Bot — tip-ready)

- **tip-ready:** PASS for Canon I (captives / captive women).
- **Source locked:** Documenta Catholica Omnia Canones GR; scaffold English discarded.
- **Pass A≠B:** `reviews/justifications/epistula_1.json` OK.
- **DOCX:** `gregory-thaumaturgus-epistula-canonica.docx`; verify_docx OK; inline Bible (1 Cor 6:13, Matt 15:11, Deut 22:25-27).
- **Live:** https://fathers.saneapps.com/works/gregory-thaumaturgus-epistula-canonica/ (200); `/1/` (200). Deploy `5590190c.fathers-site.pages.dev`. live_works=43.
- **Claim:** remains **prepped**.
- **Logos:** compile pending on Air.

## 2026-09-15 (CoS / Grok Bot — TN ops-leak cleanup)

- Stripped ops/process theater from `translator_notes` / `notes_covered` (Pass A≠B stamps, Tip densify / scaffold-discarded chatter). Kept scholarly notes (lemma/OCR/scope).
- Cleaned meta blurb/edition/method phrasing of densify/scaffold ops leak; fixed copy-paste panegyricus Title/H1/author hardcodes in `build_book.py` where present.
- Rebuilt DOCX; `pipeline.verify_docx` OK; spot-check: no Pass A / Tip densify / scaffold strings in english JSON or DOCX body.
- TNs: 3→2.
- **Logos gate: CLEAR for Air Personal Book backlog** after this strip (private study).
- **Site:** KEEP live tip (Pass B already ok). Section HTML does not embed Headword TNs; no re-ship this turn (About/meta on live may still show older densify wording until a later packet rebuild).
