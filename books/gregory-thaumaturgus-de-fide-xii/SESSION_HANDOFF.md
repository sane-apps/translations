# Gregory Thaumaturgus: De fide XII — production ledger

Canonical path: `~/SaneApps/clients/translations/books/gregory-thaumaturgus-de-fide-xii/`

## Charter

- Title: Gregory Thaumaturgus: De fide XII
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

## 2026-09-15 (ChiefOfStaff / Grok Bot — tip-ready + ship path)

- **tip-ready:** PASS for Capita I–II.
- **Source locked:** Vossius 1684 Latin column (Greek column OCR damaged; disclosed). Scholia stripped.
- **Pass B densified:** new English, not ANF Crombie; Pass A≠B; John 20 / Phil 2 inline.
- **DOCX:** `gregory-thaumaturgus-de-fide-xii.docx`; verify_docx OK; no footnotes.xml; Headword TN; no logosres:.
- **Claim:** remains **prepped** (ai_promote Jeremiah-only).
- **Logos Personal Book:** compile pending on Air.
- **Next:** live ship after visual review of dry-run artifact.


## 2026-09-15 (ChiefOfStaff / Grok Bot — live ship)

- **Live:** https://fathers.saneapps.com/works/gregory-thaumaturgus-de-fide-xii/ (200); `/1/` and `/2/` (200). Deploy `faac724c.fathers-site.pages.dev`. live_works=37.
- **Visual review:** artifact `07c93cb76e5cdbd10dce629107311ddb948d0787745286644f47fbfabb39ae29` passed image-inspection (32 shots).
- **Claim:** remains **prepped**.
- **Logos Personal Book:** compile pending on Air. DOCX at `gregory-thaumaturgus-de-fide-xii.docx`.
- **Next densify:** greg-thaum-ad-tatianum (CLAIMS order).

## 2026-09-15 (CoS / Grok Bot — TN ops-leak cleanup)

- Stripped ops/process theater from `translator_notes` / `notes_covered` (Pass A≠B stamps, Tip densify / scaffold-discarded chatter). Kept scholarly notes (lemma/OCR/scope).
- Cleaned meta blurb/edition/method phrasing of densify/scaffold ops leak; fixed copy-paste panegyricus Title/H1/author hardcodes in `build_book.py` where present.
- Rebuilt DOCX; `pipeline.verify_docx` OK; spot-check: no Pass A / Tip densify / scaffold strings in english JSON or DOCX body.
- TNs: 6→4.
- **Logos gate: CLEAR for Air Personal Book backlog** after this strip (private study).
- **Site:** KEEP live tip (Pass B already ok). Section HTML does not embed Headword TNs; no re-ship this turn (About/meta on live may still show older densify wording until a later packet rebuild).
