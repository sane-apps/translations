# Serapion of Antioch: Fragmenta — production ledger

Canonical path: `~/SaneApps/clients/translations/books/serapion-antioch-fragmenta/`

## Charter

- Title: Serapion of Antioch: Fragmenta
- Author: Serapion of Antioch
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

- **tip-ready:** PASS for Gospel of Peter fragment (Rhossus).
- **Source locked:** Routh Reliquiae Sacrae + Eusebius HE 6.12; scaffold English discarded.
- **Pass A≠B:** `reviews/justifications/serapion_1.json` OK.
- **DOCX:** `serapion-antioch-fragmenta.docx`; verify_docx OK; inline Gal 4:14.
- **Claim:** remains **prepped**.
- **Logos:** compile pending on Air.

## 2026-09-15 (CoS / Grok Bot — TN ops-leak cleanup)

- Stripped ops/process theater from `translator_notes` / `notes_covered` (Pass A≠B stamps, Tip densify / scaffold-discarded chatter). Kept scholarly notes (lemma/OCR/scope).
- Cleaned meta blurb/edition/method phrasing of densify/scaffold ops leak; fixed copy-paste panegyricus Title/H1/author hardcodes in `build_book.py` where present.
- Rebuilt DOCX; `pipeline.verify_docx` OK; spot-check: no Pass A / Tip densify / scaffold strings in english JSON or DOCX body.
- TNs: 3→2.
- **Logos gate: CLEAR for Air Personal Book backlog** after this strip (private study).
- **Site:** KEEP live tip (Pass B already ok). Section HTML does not embed Headword TNs; no re-ship this turn (About/meta on live may still show older densify wording until a later packet rebuild).

## 2026-09-17 (SerapionRe — stale-packet re-review, Mini)

- **Cause:** English re-saved post-review (translator_notes cleanup); all 5 English paras + Greek byte-identical, row/file digests moved. Old packet f6abc79d stale.
- **Review:** clause-by-clause vs locked Routh/HE 6.12 Greek; DjVu OCR + Eusebius HE 6.12 TEI cross-checked; Pass A!=B; Gal 4:14 filed clear upheld (Jev advisory possible@0.53 overruled by wording parallel; DOCX injects cite inline).
- **Artifacts:** regenerated reviews/audit/serapion_fragmenta_tip.packet.json (e158eda9, lane tool only — no hand-edited hashes) + fresh serapion_fragmenta_tip.review.json.
- **Gate:** validate_audit_receipt == [] (direct + CLI --receipt, exit 0); assert_tip_ready exit 0.
- **Coordination gap:** serapion-fragmenta-densify is prepped (Owner); no free serapion slice exists, so no board take/mark was made rather than squat an unrelated free slice.
- **Not touched:** _register_payload.json digests still reference old packet (no lane script owns that file); DOCX/Logos rebuild left for Air lane.
