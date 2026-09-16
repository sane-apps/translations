# Gregory Thaumaturgus: Panegyricus — production ledger

Canonical path: `~/SaneApps/clients/translations/books/gregory-thaumaturgus-panegyricus/`

## Charter

- Title: Gregory Thaumaturgus: Panegyricus
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

## 2026-09-15 (ChiefOfStaff / Grok Bot — tip-ready + live ship)

- **tip-ready:** PASS for opening (silence / eight years without oratory / fear before Origen).
- **Source locked:** Vossius 1684 Latin column (PDF pp. ~72-74); Greek OCR damaged; Argumentum/scholia stripped; scaffold summary discarded.
- **Pass A≠B:** justification `reviews/justifications/paneg_1.json` OK.
- **DOCX:** `gregory-thaumaturgus-panegyricus.docx`; verify_docx OK; Headword TN; inline/editorial Bible Genesis 48:15; no footnotes.xml.
- **Live:** https://fathers.saneapps.com/works/gregory-thaumaturgus-panegyricus/ (200); `/1/` (200). Deploy `a1a8a899.fathers-site.pages.dev`. live_works=41.
- **Claim:** remains **prepped**.
- **Logos:** compile pending on Air.
- **Next densify:** greg-thaum-eccl-metaphrase (CLAIMS order); skip origen-numbers, cosmas, paulus-silentarius-*, photius.

## 2026-09-15 (CoS / Grok Bot — TN ops-leak cleanup)

- Stripped ops/process theater from `translator_notes` / `notes_covered` (Pass A≠B stamps, Tip densify / scaffold-discarded chatter). Kept scholarly notes (lemma/OCR/scope).
- Cleaned meta blurb/edition/method phrasing of densify/scaffold ops leak; fixed copy-paste panegyricus Title/H1/author hardcodes in `build_book.py` where present.
- Rebuilt DOCX; `pipeline.verify_docx` OK; spot-check: no Pass A / Tip densify / scaffold strings in english JSON or DOCX body.
- TNs: 4→3.
- **Logos gate: CLEAR for Air Personal Book backlog** after this strip (private study).
- **Site:** KEEP live tip (Pass B already ok). Section HTML does not embed Headword TNs; no re-ship this turn (About/meta on live may still show older densify wording until a later packet rebuild).
