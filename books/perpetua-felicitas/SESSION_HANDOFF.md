# Passion of Perpetua and Felicitas — production ledger

Canonical path: `~/SaneApps/clients/translations/books/perpetua-felicitas/`

## Charter

- Title: Passion of Perpetua and Felicitas
- Author: Perpetua, Saturus, and the Redactor (Carthage, 203, Severan)
- Scope: the complete Passio as printed by Gebhardt VII (21 sections), in nightly queue order.
- Why this work: highest demand — Perpetua's own prison diary, the most-read martyr text after the New Testament.
- Legal: private study; new English from the Latin only. No modern copyrighted English used.
- Sources: Gebhardt 1902 (archive.org actamartyrumsel00gebhgoog), Latin copy-text throughout; facing Greek is a version, cited only secondarily. The Greek heading's Valerian-and-Gallienus date is not imported.

## State (2026-10-19 night, Spark) — book COMPLETE 21/21

- All 21 sections drafted, critic-passed, gate-clean, promoted with justifications and filed receipts (`reviews/audit/perpetua_1..21.review.json`, all verdict pass, validate zero errors against current book text).
- Notable lane events: §1's first draft skimped the gloss (retry passed); §3 took three draft attempts on cut-offs; §5's two passing drafts failed the shared gate on bare "scaffold" — narrowed PLACEHOLDER to operational compounds + regression test (29/29 green); §§10 and 20 needed retries on long-section cut-offs; the §§9-10 catch-up caught a missing-research filing gap; the critic rightly failed an untranslated §16 holding row once (no rubber-stamp).
- Staleness rule applied throughout: promote → rebuild packet → review on promoted text; every book-file move re-stales all packets.
- DOCX/Logos/site: not started.

## Next

1. Conon the Gardener (scaffolded, §§1-4 locked) — queue next.
2. Pionius (23 chapters, long) — after Conon.
