# Synodical Letter — production ledger

Canonical path: `~/SaneApps/clients/translations/books/sophronius-jerusalem-synodical-letter/`

## Charter

- Title: Synodical Letter (Epistola Synodica ad Sergium, 634)
- Author: Sophronius of Jerusalem (c. 560–638)
- Scope (Wave 3): translate the core sections only — the address/opening and the two-wills / two-energies confession (PG cols ~3160–3180), plus the closing reception of the five councils and anathema list (cols 3187–3192) if time allows. Remainder is checkpointed here for the book-production lane as a whole-work completion.
- Source: Migne, Patrologia Graeca 87.3 (public domain), via archive.org item `pg-87-3`. Djvu text locked in `sources/pg-87-3_djvu.txt` (sha256 in `sources/manifest.json`); page-image PDF `sources/pg-87-3.pdf`.
- Letter location in the volume text: djvu bytes ≈986,500–1,135,000; title block at ≈988,036 ("EPISTOLA SYNODICA AD SERGIUM PATRIARCHAM CONSTANTINOPOLITANUM. (Mansi, Concil. general. Coll. XI, p. 461.)").
- OCR warning: the archive.org Greek OCR of PG 87.3 is rough — finding aid only. All translated sections must be transcribed from the PDF page images (pdftoppm) and verified against them; never translate from the raw OCR alone.
- Legal: private study; new English translation from the public-domain Migne Greek; no modern copyrighted edition or translation used.

## State

- Sources: LOCKED 2026-10-20 — djvu text + page-image PDF (sha256 in sources/manifest.json). Letter located: cols 3149-3192 = PDF pp. ~191-213; title block at djvu char ~970,127.
- Translations: CORE SECTIONS DONE 2026-10-20 (Wave 3) — section 1 (cols 3152B-3152D: why he writes + the Trinity confession) and section 2 (cols 3171B-3172D: two natures, two natural operations), Greek transcribed from the page images (PDF pp. 191, 201), Pass A/B + justification receipts in reviews/justifications/ (check_pass_ab ok=2 fail=0), QA packet reviews/audit/sophronius.packet.json (packet 2b581acb039e, structural OK). Remaining sections + independent certification review + DOCX/Logos packaging: production lane.
- DOCX: not built
- Logos Build: not compiled
- Bible-link verify: not done

## Next

Follow `docs/SOP.md`: render core pages from the PDF, transcribe, translate core sections, QA, then checkpoint the remainder for the production lane.
