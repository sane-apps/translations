# Passion of Marianus and James — production ledger

Canonical path: `~/SaneApps/clients/translations/books/marianus-james/`

## Charter

- Title: Passion of Marianus and James
- Author: A friend of the martyrs (Numidia, Valerianic era, Cyprian's circle)
- Scope: the complete Passio as printed by Gebhardt XIII, in nightly queue order.
- Why this work: high demand — the Numidian pair, the exiled bishops, the glittering Christ; told by their closest friend.
- Legal: private study; new English from the Latin only. No modern copyrighted English used.
- Sources: Gebhardt 1902 (archive.org actamartyrumsel00gebhgoog), Latin copy-text. See `sources/manifest.json`.

## State (2026-10-19 night, Spark)

- §§1-3 drafted, critic-passed first try, gate-clean, promoted with justifications and filed receipts (`reviews/audit/marianus_1/2/3.review.json`, all verdict pass, validate clean against current book text).

## State (2026-10-19 night, Spark, continued)

- §§4-5 through the lane: §4's first draft dropped the followers' march (Sequebantur–antecessuri) and left operational text as p2 — compare critic failed completeness. Parent repair round: restored both sentences, normalized Marianus, promoted, re-reviewed on promoted text — pass. §5's first draft cut off (retry passed).
- Lesson repeated: the nightly drafts fresh, so sandbox receipts never cover promoted repairs — re-review promoted text directly.

## State (2026-10-19 night, Spark, §§6-7)

- §§6-7 through the lane, both pass, validate ALL_CLEAN (`reviews/audit/marianus_6/7.review.json`), justifications filed. §6: Marianus's tribunal vision — Cyprian at the judge's right, the meadow road, the shared bowl, waking at his own Deo gratias. §7: James's midday cart vision — the youth above the clouds, one purple girdle per lap, follow me swiftly.
- Parent repairs this round: §6 trimmed draft redundancies (My turn came too; palace for praetorium); §7 fixed literal garbage (the face of his mouth → his face; How rejoicing → How exultant; Marian → Marianus; ungirt garment; he who keeps watch in faith). Rebuilt packets with selected_sections (hand-subsetting breaks packet_id — use the builder flag), re-reviewed on promoted text, clean.
- Lesson repeated again: my two queue-writer slips (wrong item shape, then missing raw/identity/research) — the runner's docstring shape is english/source/raw/identity/section/research; write the full shape first time.

## State (2026-10-19 night, Spark, §§8-9)

- §§8-9 through the lane, both pass, validate ALL_CLEAN (`reviews/audit/marianus_8/9.review.json`), justifications filed. §8: Aemilianus's dialogue — doubled fasts, sword and blood near, the star analogy (1 Cor 15:41), the unnamed two, the camel logion (Mt 19:24, plural caelorum as printed). §9: the Cirta transfer — honored with the formal charge, the shining bystander-convert, Lambaesis again.
- §8's first draft cut off mid-dialogue (stars, two, camel left as raw Latin) — compare critic failed completeness rightly. Parked per rule, retried: full draft passed, parent-polished (superposed fasts smoothed; next day; caelorum kept with disclosed reference), re-reviewed on promoted text, clean.
- §9 parent tweak only: record → formal charge for elogio, keeping the indictment sense.

## State (2026-10-19 night, Spark, §§10-11)

- §§10-11 through the lane, both pass, validate ALL_CLEAN (`reviews/audit/marianus_10/11.review.json`), justifications filed. §10: the clergy held back while the laity bled — ingenious cruelty's split, the slow victory grieved. §11: Agapius's banquet — Tertulla and Antonia, the twin boy rose-crowned with green palm (tomorrow you sup with us, Mt 5:12 disclosed), the sentence serving God's promises, the crown-place valley, baptized in blood and washed in the river.
- §11's first draft was near-empty (Justin §5 pattern) — parked, retried full, parent-polished (Marian→Marianus x2; hasten; natural amphitheatre; sacrament over sacred sign), re-reviewed on promoted text, clean.
- §10 parent tweak only: Marian→Marianus; suis bound to saeculi.

## State (2026-10-19 night, Spark, §§12-13 — COMPLETE)

- §§12-13 through the lane, both pass, validate ALL_CLEAN (`reviews/audit/marianus_12/13.review.json`), justifications filed. §12: the arena's logistics of slaughter, veiled eyes seeing snow-white horses and white-robed youths, Marianus's plagues sermon (cynomyia venoms, Ex 8:21) as trumpet-call. §13: Maria's Maccabean joy (2 Macc 7) — the name pun, neck-wound kisses, blood-redemption doxology (Gal 1:5 disclosed).
- Parent repairs: Marian→Marianus; riders→youths; pit→riverbed; gnawing→tormenting venoms; give thanks→congratulate. No fails this round — both passed first try.
- **Marianus & James COMPLETE 13/13.** Next: Polycarp (Gebhardt XIV follows) — scaffold, then lock §§1+.

## Next

1. Scaffold Polycarp, lock §§1-2 Greek with OCR corrections + research, then queue.
