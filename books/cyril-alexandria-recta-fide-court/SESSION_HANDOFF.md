# Cyril of Alexandria — On the True Faith to the Imperial Women

Canonical path: `~/SaneApps/clients/translations/books/cyril-alexandria-recta-fide-court/`

## Charter

- **Title:** Cyril of Alexandria: On the True Faith to the Imperial Women
- **Author:** Cyril of Alexandria (d. 444)
- **Type:** Monograph. Language: English (new translation).
- **Scope:** CPG **5219** *De recta fide ad dominas* (to Arcadia and Marina) and CPG **5220** *De recta fide ad augustas* (to Pulcheria and Eudocia). Not *ad Theodosium* (King FC 129 already has modern English of that one).
- **Why:** No complete English of these two court treatises. Post-Nicene. Not Cyril of Jerusalem. Not the complete Cyril corpus.
- **Legal:** private study. New English from locked PD Greek (PG 76 / Pusey 1877). Modern English (King FC 129 covers other treatises) may be a style/QA check only — never copied.
- **Enrichment:** inline Bible links + Headword TN marks. No Word footnotes. No `logosres:`.
- **First English:** yes, when shipped.

## State

- 2026-09-11: Pusey 1877 locked (`sources/pusey1877_de_recta_fide.pdf` + `_djvu.txt`, IA `SPNCyrilli7`). *Ad Arcadiam Marinamque* running heads start ~p. 155; *ad Pulcheriam et Eudociam* ~p. 265. Skip *ad Theodosium* (opens the volume).
- 2026-09-12: **Source lock done** (claim `cyril-rf-lock`). Sliced OCR Greek into:
  - `translations/ad_arcadiam_marinamque_source.json` (CPG 5219, Pusey pp. 155–264)
  - `translations/ad_pulcheriam_eudociamque_source.json` (CPG 5220, Pusey pp. 265–333)
  - Ingest: `scripts/ingest_pusey_recta_fide.py`
  - No English in this claim.


## State update 20260912T045319Z

- Claim **cyril-rf-a1** done: Arcadia §§1–4 Pass A≠B.
- Greek clean: `translations/ad_arcadiam_marinamque_greek_clean_a1.json`
- English: `translations/ad_arcadiam_marinamque_english.json` (4 sections)
- Justifications: `reviews/justifications/rf_arcadia_01.json` … `_04.json`
- Next: continue Arcadia from §5 / p.158 (`cyril-rf-a2`), then Pulcheria; or topics lane.


## State update 20260912T050233Z

- Claim **cyril-rf-a2** done: Arcadia §§5–8 Pass A≠B.
- Greek clean: `translations/ad_arcadiam_marinamque_greek_clean_a2.json`
- Justifications: `rf_arcadia_05.json` … `_08.json`
- Next: `cyril-rf-a3` from §9 / p.162 (Athanasius citation continues).


## State update 20260912T051001Z

- Claim **cyril-rf-a3** done: Arcadia §§9–12 Pass A≠B (Athanasius close + florilegium).
- Next: `cyril-rf-a4` from §13 / p.166 (Vitalis continues; Theophilus vs Origenists).


## State update 20260912T051606Z

- Claim **cyril-rf-a4** done: Arcadia §§13–16 Pass A≠B (Vitalis/Theophilus + Cyril on Χριστός name).
- Next: `cyril-rf-a5` from §17 / scripture catena heads.

## Next

Translate from locked `*_source.json` (Pass A/B) → DOCX → site (era banner; treatises with no earlier English). OCR cleanup as needed while translating.


## State update 20260912T052915Z

- Claim **cyril-rf-a5** done: Arcadia §§17–20 Pass A≠B (scripture catena heads + Rom 1–4/7 argument that Christ is God).
- Next: `cyril-rf-a6` from §21 / continuing Pauline catena.


## State update 20260912T053538Z

- Claim **cyril-rf-a6** done: Arcadia §§21–24 Pass A≠B (Rom 8 Spirit of Christ; love/judgment; gospel ministry; 1 Cor church/cross).
- Next: `cyril-rf-a7` from §25.


## State update 20260912T054410Z

- Claim **cyril-rf-a7** done: Arcadia §§25–28 Pass A≠B.
- Next: `cyril-rf-a8` from §29.


## State update 20260912T054854Z

- Claim **cyril-rf-a8** done: Arcadia §§29–32 Pass A≠B.
- Next: `cyril-rf-a9` from §33.

## State update 20260912T060958Z

- Claim **cyril-rf-a9** done: Arcadia §§33–36 Pass A≠B (2 Cor 10 captive thoughts; Gal law/faith/Spirit; baptism/cross/Eph seating & indwelling; Phil refuse / Col mystery).
- Next: `cyril-rf-a10` from §37.
- 2026-09-12: **cyril-rf-a11** Arcadia §§41–44 Pass A≠B (greek_clean_a11; Tim/Titus Savior; James gifts; 1 Pet sanctification/Spirit; 2 Pet/1 John/Jude Master).
- 2026-09-12: **cyril-rf-a12** Arcadia §§45–48 Pass A≠B (greek_clean_a12; Matt infancy/Spirit-baptism/harvest/yoke/temple).
- 2026-09-12: **cyril-rf-a13** Arcadia §§49–52 Pass A≠B (greek_clean_a13; angels/Peter/tax/Hosanna/cross/John hearts).
- 2026-09-12: **cyril-rf-a14** Arcadia §§53–56 Pass A≠B (greek_clean_a14; ask-in-name one God; John 17 life/oneness; locked doors/Spirit; Luke Baptist/David throne).
- 2026-09-12: **cyril-rf-a15** Arcadia §§57–60 Pass A≠B (greek_clean_a15; annunciation/Baptist/Simeon; forgive sins; Isaiah+sea; Gerasene/Jairus).
- 2026-09-12: **cyril-rf-a16** Arcadia §§61–64 Pass A≠B (greek_clean_a16; servant/throne; last Adam; Life raises; Word handled / faith as in God).
- 2026-09-12: **cyril-rf-a17** Arcadia §§65–68 Pass A≠B (greek_clean_a17; 1 John flesh/antichrist; water-blood-Spirit; Jordan/Jairus union; sealed/hilasterion).
- 2026-09-12: **cyril-rf-a18** Arcadia §§69–72 Pass A≠B (greek_clean_a18; blood-redemption/second Adam/Eph near/mediator impassible-passible).
- 2026-09-12: **cyril-rf-a19** Arcadia §§73–76 Pass A≠B (greek_clean_a19; grain-glory/hypostasis/right-hand/Rom14 lordship/2 Cor 5:16).
