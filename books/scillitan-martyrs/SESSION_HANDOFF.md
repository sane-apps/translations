# Acts of the Scillitan Martyrs — production ledger

Canonical path: `~/SaneApps/clients/translations/books/scillitan-martyrs/`

## Charter

- Title: Acts of the Scillitan Martyrs (Passio sanctorum Scillitanorum)
- Author: anonymous court record / passio; martyrs of Scillium, executed at Carthage
- Scope: complete Latin passio as printed by Gebhardt (1902), sections 1-17. Hearing before the proconsul Saturninus, 17 July AD 180 — the earliest dated Latin Christian martyr act.
- Why this work: `docs/CORPUS_AUTHORITY.md` table A and `docs/EARLY_INVENTORY.md` list it as missing (180, ANF 9 prior English). It is the earliest highly desirable missing work with a clean, complete, readable original-language text. Aristides, Apology (c. 125) ranks higher but survives complete only in Syriac; its Greek is the Barlaam recast. Parked pending an owner witness decision — do not start it from the recast and call it Aristides.
- Legal: private study; new English from the Latin only. No modern copyrighted English used; ANF wording not consulted as source.
- Sources: Gebhardt, Acta martyrum selecta (1902), pp. 92-96 (archive.org actamartyrumsel00gebhgoog), Latin copy-text; Greek version alongside as check witness. See `sources/manifest.json`.

## State (2026-10-18)

- Sources: locked — `translations/scillitan_source.json` (17 sections, variants recorded); retained scan text `sources/gebhardt1902_scillitan.txt`.
- Translations: Muse direct draft complete — `translations/scillitan_english.json`; justification `reviews/justifications/scillitan_acts.json`; `check_pass_ab` green.
- Review: COMPLETE 2026-10-18. Blind-gloss critic passed with two small losses (§6 magis illi, §14 perseveraverunt), both fixed. First full `muse_review` run failed only §1 source_identity (emended Claudiano→Condianus); repair restored the printed name, history moved to the note; §1 re-review passed. Clean full receipt `reviews/audit/scillitan.review.json`: verdict pass, 17/17 sections, `validate_audit_receipt` zero errors. Pre-repair full receipt kept as `scillitan.review.pre-repair.json`; retry receipt for §§11/13/17 after transient Muse errors kept as `scillitan_retry.*`. Adapter fix landed: `muse_review` filters research to selected sections (gate caught the leak).
- DOCX: build_book.py written (frontmatter + sections + TN notes), but the build is on hold by gate: the passio cites no Scripture directly (Mt 22:21 is a possible allusion only), so `verify_docx` refuses a book with zero Bible links. Leave on hold per the tip exemption; do not invent links.
- Logos Build: not compiled. Bible-link verify: n/a yet (one possible allusion, Mt 22:21, recorded as possible only).

## Next

1. Promote receipt into the book's audit folder; replace build_book.py stub with a real assembly (follow a sibling martyr book, e.g. acts-of-justin) and build the DOCX.
2. Logos compile + site ship through the normal gates.
3. Owner call queued separately: Aristides witness decision (Syriac version as copy-text with disclosure, or Greek recast scoped as recast, or skip).
