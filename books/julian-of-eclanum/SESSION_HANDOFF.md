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
