# Julian of Eclanum — production ledger

Canonical path: `~/SaneApps/clients/translations/books/julian-of-eclanum/`
Former path (pointer only): `~/Documents/Logos Personal Books/Julian of Eclanum/`

## Charter

User authorized full surviving material preserved by Augustine, newly translated into plain English; English only in Logos, Bible quotations/allusions linked. Do not present as complete works: Ad Florum books VII–VIII lost; independent biblical commentaries outside this Augustine-based scope. No modern English translations may be copied. No purchases or public publication.

## Verified complete, 2026-09-09

- Personal Books Build succeeded with 0 errors, 0 warnings (`LastCompiled` 2026-09-09T20:59:52-04:00).
- ArticleCache titles cleaned (0 remaining `[[@Headword:]]` glue).
- Headword emitted as its own paragraph after clean heading (pipeline rule).
- Owner confirmed live in Logos: Bible-link hover and click both work.
- Air GUI capture path: Terminal.app-hosted Peekaboo/screencapture.

## Corpus counts

- To Florus 1–6: 834 sections (141/236/216/136/64/41)
- Contra Julianum supplements + Marriage II + Letter to Rome + Collective letter → ~1164 DOCX sections, ~1702 Bible links, ~580 Scripture-index entries

## Build

```bash
cd ~/SaneApps/clients/translations
python3 books/julian-of-eclanum/build_book.py
python3 -m pipeline.verify_docx books/julian-of-eclanum/*.docx
# On Air after Logos rebuild:
python3 -m pipeline.verify_logos_db --title-substr "Julian"
```

Sources: Augustinus.it Latin (private study); CCEL NPNF context PD; Migne PL 45 for hard cases. Latin only in `sources/`.

## Two-pass justifications (remaining works, not To Florus)

Prefix chosen: **`turbantius_B_NNN`** for Against Julian / To Turbantius fragments (not `contra_B_NNN`). `B` is Augustine's book number; `NNN` is 1-based order in `translations/contra_julianum_B_english.json`.

| Work | Files | Prefix | English rows | Notes |
|------|------:|--------|--------------|-------|
| Against Julian fragments | 251 | `turbantius_{1–6}_{nnn}.json` | 13+9+50+55+60+64 | Latin from `sources/contra_julianum_{n}.json` (`candidate_quotations` / `latin_context`; no `julian` field). `kind=report` when the English is Augustine reporting. |
| Marriage II extracts | 28 | `marriage_{nnn}.json` | 33 | Skipped 5 rows with no Julian Latin: 2.2.3–2.2.6 (Augustine quoted in the intermediary) and 2.4.11 (compiler heading). Latin from `sources/marriage2_sections.json`. |
| Letter to Rome | 15 | `rome_{nnn}.json` | 15 | Latin from `sources/letter_to_rome_selected_context.json` (`inquit` clauses). 1.12.25 is `kind=report`. |
| Collective letter | 31 | `collective_{nnn}.json` | 31 | Latin from `sources/letters{2,3,4}_latin.txt`. Reports marked `kind=report`. |

`python3 -m pipeline.check_pass_ab` on these 325 files: **ok=325 fail=0**. Pass A ≠ Pass B; lemmas ≥2; choices ≥1; `source_text` Latin; `reviewer: pending-human`; NPNF not copied; Julian is not first-English (Victorian English exists inside NPNF Augustine). Pass A is a literal gloss of Julian's Latin only.
