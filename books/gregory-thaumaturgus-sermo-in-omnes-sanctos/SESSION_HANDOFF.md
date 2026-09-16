# Gregory Thaumaturgus: Sermo in omnes sanctos — production ledger

Canonical path: `~/SaneApps/clients/translations/books/gregory-thaumaturgus-sermo-in-omnes-sanctos/`

## Charter

- Title: Gregory Thaumaturgus: Sermo in omnes sanctos
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

- **tip-ready:** PASS for opening (blessing through Hades despoiled / sting of death).
- **Source locked:** MGR Greek extract (TLG 2063.010 / Documenta Catholica Omnia); PG 10.1200–1201 cues.
- **Pass A≠B:** justification `reviews/justifications/omnes_1.json` OK.
- **DOCX:** `gregory-thaumaturgus-sermo-in-omnes-sanctos.docx`; verify_docx OK; Headword TN; inline Bible (1 Cor 15:55); no footnotes.xml.
- **Live:** https://fathers.saneapps.com/works/gregory-thaumaturgus-sermo-in-omnes-sanctos/ (200); `/1/` (200). Deploy `6dba211d.fathers-site.pages.dev`. live_works=40.
- **Claim:** remains **prepped**.
- **Logos:** compile pending on Air.
- **Next densify:** greg-thaum-panegyricus — current english is scaffold summary; needs real Latin lock Pass A≠B before ship.

## 2026-09-15 (CoS / Grok Bot — TN ops-leak cleanup)

- Stripped ops/process theater from `translator_notes` / `notes_covered` (Pass A≠B stamps, Tip densify / scaffold-discarded chatter). Kept scholarly notes (lemma/OCR/scope).
- Cleaned meta blurb/edition/method phrasing of densify/scaffold ops leak; fixed copy-paste panegyricus Title/H1/author hardcodes in `build_book.py` where present.
- Rebuilt DOCX; `pipeline.verify_docx` OK; spot-check: no Pass A / Tip densify / scaffold strings in english JSON or DOCX body.
- TNs: 5→4.
- **Logos gate: CLEAR for Air Personal Book backlog** after this strip (private study).
- **Site:** KEEP live tip (Pass B already ok). Section HTML does not embed Headword TNs; no re-ship this turn (About/meta on live may still show older densify wording until a later packet rebuild).
