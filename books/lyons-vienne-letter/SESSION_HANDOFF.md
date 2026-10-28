# Letter of the Churches of Lyons and Vienne — production ledger

Canonical path: `~/SaneApps/clients/translations/books/lyons-vienne-letter/`

## Charter

- Title: Letter of the Churches of Lyons and Vienne (177)
- Author: the churches of Vienne and Lyons, Gaul
- Scope: the complete letter as printed by Gebhardt (Eusebius HE 5.1-3), in nightly queue order starting with the greeting. Later source sections are locked one by one as their scan OCR is read and corrected.
- Why this work: `docs/EARLY_INVENTORY.md` lists the Lyons letter as missing (177) — the next highly desirable missing early work after the finished Scillitan Acts. Aristides Apology stays parked on its witness problem (complete text only in Syriac; Greek is the Barlaam recast; needs an owner witness decision).
- Legal: private study; new English from the Greek only. No modern copyrighted English used.
- Sources: Gebhardt 1902 (archive.org actamartyrumsel00gebhgoog), Greek copy-text; preserving work Eusebius HE 5.1-3 (letter only, not the Eusebian frame).

## State (2026-10-18)

- Sources: section 1 (greeting, HE 5.1.3) locked and corrected.
- Translations: holding row only; the nightly lane drafts it.
- Queue: `outputs/muse-lane/queue.json` holds lyons-vienne-letter §1 with two recorded research entries. Next nightly run (05:10) drafts, critic-reviews, and gate-validates it.
- Review: COMPLETE 2026-10-18 for sections 1-4. §1 via nightly run 20261019T013101Z (100s); §§2-3 via nightly run 20261019T013623Z (under 4 min for both). §4 failed its first draft gate (whole paragraph as one English sentence) — the lane's first real catch; one repair round split it into read-aloud sentences, critic pass, gate clean. Filed receipts `reviews/audit/lyons_1/2/3/4.review.json`, all verdict pass, `validate_audit_receipt` zero errors on each. Drafts promoted into `translations/lyons_english.json` with justifications `reviews/justifications/lyons_1/2/3/4.json`.
- Review: COMPLETE 2026-10-18 for section 5 as well (§5 via nightly run 20261019T015033Z, straight pass; receipt `reviews/audit/lyons_5.review.json`, gate clean; justification `reviews/justifications/lyons_5.json`).
- Review: COMPLETE 2026-10-18 for section 6 as well (§6 via nightly run 20261019T020051Z, under 2 min, straight pass; receipt `reviews/audit/lyons_6.review.json`, gate clean; justification `reviews/justifications/lyons_6.json`). The flagged φόνον→φόβον emendation was accepted by the drafter and unflagged by the blind critic; recorded in source, research, and justification.
- Review: COMPLETE 2026-10-18 for sections 7-8 as well (§§7-8 via nightly run 20261019T020817Z, ~3 min for both, straight passes; receipts `reviews/audit/lyons_7/8.review.json`, gate clean; justifications `reviews/justifications/lyons_7/8.json`). Letter stands at §§1-8, every section receipted.
- Review: COMPLETE 2026-10-18 for section 9 as well (§9 via nightly run 20261019T021451Z, straight pass; receipt `reviews/audit/lyons_9.review.json`, gate clean; justification `reviews/justifications/lyons_9.json`). Letter stands at §§1-9, every section receipted.
- Review: COMPLETE 2026-10-18 for section 10 as well (§10 via nightly run 20261019T021844Z, straight pass; name normalized Biblis→Biblias with a re-review of the changed section, gate clean; receipt `reviews/audit/lyons_10.review.json`; justification `reviews/justifications/lyons_10.json`). Letter stands at §§1-10, every section receipted.
- Review: COMPLETE 2026-10-18 for section 11 as well (§11 via nightly run 20261019T022342Z, straight pass; receipt `reviews/audit/lyons_11.review.json`, gate clean; justification `reviews/justifications/lyons_11.json`). The flagged προκατήχιστο was rendered 'hardened beforehand' and unflagged by the critic; decision recorded. Letter stands at §§1-11, every section receipted.
- Review: COMPLETE 2026-10-18 for section 12 as well (§12 via nightly run 20261019T022742Z, straight pass; Lugdunum→Lyons normalized for consistency with §1, re-reviewed, gate clean; receipt `reviews/audit/lyons_12.review.json`; justification `reviews/justifications/lyons_12.json`). Letter stands at §§1-12, every section receipted.
- Usage tonight: runner healthy throughout; only errors were the earlier transient trio on the Scillitan rerun (all passed on retry). Calls run ~30s median on Spark.
- Review: COMPLETE 2026-10-18 for section 13 as well. First adapter run failed on an unparsed compare (model echoed the schema; the verdict itself was a clean pass) — parser fixed in `scripts/muse_review.py` with a test, prompt hardened. A second ordering mistake (receipt generated against a sandbox copy, then promotion changed the row hash) is now a lane rule: file the receipt only against the promoted text. Final receipt `reviews/audit/lyons_13.review.json` verdict pass, gate clean; justification `reviews/justifications/lyons_13.json`. Both flagged forms resolved by the draft and unflagged by the critic: 'punished twice as severely', 'breathed out together the fragrance of Christ'. Letter stands at §§1-13, every section receipted.
- Next: lock section 14 Greek (the varied crowns of the outgoing martyrs — HE 5.1.36b-37, check the page-35 tail) with OCR corrections, then queue it with research. Repeat nightly.
- DOCX/Logos/site: not started.
