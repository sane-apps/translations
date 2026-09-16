# Robert Baron — Philosophia theologiae ancillans (Exercitatio Prima Art. I-III tip) — production ledger

Canonical path: `~/SaneApps/clients/translations/books/baron-philosophia-theologiae-ancillans/`

## Charter

- Title: Philosophia theologiae ancillans (Exercitatio Prima Art. I-III tip)
- Author: Robert Baron (Roberto Baronio; Reformed philosophy professor, St Salvator's, St Andrews)
- Resource type: Monograph; language of the Logos/site body: English
- Scope: **tip→FULL densify** — Exercitatio Prima *De Ente & Essentia* Art. I–III (necessary being; being by essence; actual/potential/mixed; God as actus purus) from the 1658 Oxford corrected Latin. Not the whole *Philosophia theologiae ancillans*.
- Legal: private study and fathers.saneapps.com publication of new English from allowed PD Latin. No modern copyrighted English copy-text. 1658 Latin is public domain (IA EEBO digitization).

## Source lock

- **Copy-text:** *Philosophia theologiae ancillans…* [Oxford]: Impensis T. Robinson & R. Davis, 1658. Editi priori correctior. Wing B887. IA `bim_early-english-books-1641-1700_philosophia-theologi-an_baron-robert_1658`.
- Local: `sources/_baron_ente_art1_2_latin_lock.txt` (Art. I–II); `sources/_baron_ente_art3_latin_lock.txt` (Art. III); Art. III pdftotext pages + full DjVu OCR as checks; `sources/manifest.json`.

## State

- Sources: locked (Exercitatio Prima Art. I–III)
- Translations: Pass A + Pass B for sections 1-3
- DOCX: built (3 sections, 0 Bible links, 6 TN notes) — tip exemption: no unwarranted Bible links
- Site: Art. III expand ready for ship 2026-09-15 evening ET

## 2026-09-15 (Art. III live expand — Scribe / Grok Bot)

- Locked Art. III Latin from IA PDF leaves ~19–21 + DjVu check (`_baron_ente_art3_latin_lock.txt`).
- Pass A ≠ B (`ente_3.json`); English section 3: God as pure act; objective/passive/ad-non-esse potencies denied of God; finite mixed being.
- Stripped residual Exodus 3:14 `added_allusions` from section 1 (honesty / tip exemption).
- Regenerated audit packet + receipt for sections 1–3; registered digests in fathers `data/publication-review.json`.
- DOCX rebuild: 3 sections, 0 Bible links. `verify_docx` fails closed on Bible-link presence — expected under tip exemption; do **not** reintroduce fake refs.
- Next locus: Art. IV (modes of existing / per se vs in alio) then remainder of Exercitatio Prima toward FULL.

## Prior notes (Art. I–II tip; PBB exemption)

- Tip exemption for no-Bible-links locus documented. Do not reintroduce Exodus 3:14 or any unwarranted ref to green Logos verify_docx.
- Live public title: Philosophy the Handmaid of Theology — https://fathers.saneapps.com/works/baron-philosophia-theologiae-ancillans/

## Next

Follow `docs/SOP.md`. Reformed lane: Art. IV+ densify. Ship via fathers `scripts/ship.sh` when OUR gate clear.
