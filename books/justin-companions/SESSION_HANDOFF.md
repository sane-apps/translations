# Martyrdom of Justin and Companions — production ledger

Canonical path: `~/SaneApps/clients/translations/books/justin-companions/`

## Charter

- Title: Martyrdom of Justin, Chariton, Charito, Evelpistus, Hierax, Paeon and Liberian
- Author: Acts of the Martyrs (Rome, ~165, trial before Rusticus)
- Scope: the complete martyrdom as printed by Gebhardt III, in nightly queue order.
- Why this work: very high demand — Justin Martyr's trial and death; the named lodging above the bath, the slave freed by Christ, the only true God.
- Legal: private study; new English from the Greek only. No modern copyrighted English used.
- Sources: Gebhardt 1902 (archive.org actamartyrumsel00gebhgoog), Greek copy-text. See `sources/manifest.json`.

## State (2026-10-18 night, Spark) — book COMPLETE 6/6

- §§1-6 drafted, critic-passed, gate-clean, promoted with justifications and filed receipts (`reviews/audit/justin_1..6.review.json`, all verdict pass, validate zero errors against the current book text).
- §1 needed its queue research attached (lane refused a research-less item: needs-research, by design) — requeued with three lookups, passed.
- §4 took the full repair path: first draft duplicated Paeon's answer (compare failed completeness), second draft added a (John 17:3) parenthetical inside the reading (compare failed scripture). Parent adjudicated both against the locked source, promoted the repair, ran muse_review.py directly on the promoted text — blind-gloss pass, validate clean. Both catches were real; the lane earned its keep twice in one section.
- §5's first draft came back near-empty (cut-off reply: draft-gate-failed); retried per the lane rule without spending repair — passed.
- Ordering lesson (new): the nightly drafts fresh each run, so a passing draft must be PROMOTED into the book and the packet+receipt REBUILT against the promoted text — sandbox receipts go stale the moment the book file moves. §§1,2,3,5,6 were re-reviewed on promoted text; §4's packet was rebuilt after the later promotions touched the book file. All six receipts validate clean against current files.
- DOCX/Logos/site: not started.

## Next

1. Next high-demand Gebhardt work: Perpetua (VII, Latin), Pionius (VIII), Apollonius (VI), Conon — lock from OCR next.
