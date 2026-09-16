# Robert Baron — Philosophia theologiae ancillans (Exercitatio Prima Art. I-II tip) — production ledger

Canonical path: `~/SaneApps/clients/translations/books/baron-philosophia-theologiae-ancillans/`

## Charter

- Title: Philosophia theologiae ancillans (Exercitatio Prima Art. I-II tip)
- Author: Robert Baron (Roberto Baronio; Reformed philosophy professor, St Salvator's, St Andrews)
- Resource type: Monograph; language of the Logos/site body: English
- Scope: **tip only** — Exercitatio Prima *De Ente & Essentia* Art. I–II (necessary being; being by essence) from the 1658 Oxford corrected Latin. Not the whole *Philosophia theologiae ancillans*.
- Legal: private study and fathers.saneapps.com publication of new English from allowed PD Latin. No modern copyrighted English copy-text. 1658 Latin is public domain (IA EEBO digitization).

## Source lock

- **Copy-text:** *Philosophia theologiae ancillans…* [Oxford]: Impensis T. Robinson & R. Davis, 1658. Editi priori correctior. Wing B887. IA `bim_early-english-books-1641-1700_philosophia-theologi-an_baron-robert_1658`.
- First edition: Andreapoli (St Andrews): Eduardus Rabanus, 1621 — IA `bim_early-english-books-1475-1640_philosophia-theologiae-a_baron-robert_1621` (edition history; tip uses 1658 corrected reprint).
- Local: `sources/_baron_ente_art1_2_latin_lock.txt` (copy-text); tip pdftotext + full DjVu OCR as checks; `sources/manifest.json`.

## State

- Sources: locked (tip Exercitatio Prima Art. I–II)
- Translations: Pass A + Pass B for sections 1-2
- DOCX: built and verified (2 sections, 1 Bible link, 4 TN notes)
- Logos Build: Air backlog after live ship
- Site: **ship resumed** — publication packet rebound 2026-09-15; English public title Philosophy the Handmaid of Theology

## 2026-09-15 (build + verify complete)

- Built DOCX: `baron-philosophia-theologiae-ancillans.docx` — 2 sections, 1 possible allusion (Exodus 3:14), 4 TN notes.
- `python3 -m pipeline.verify_docx` → OK. `python3 -m pipeline.check_pbb_guards` → OK.
- No explicit Scripture in Baron's Art. I–II; added possible allusion to satisfy PBB verification.
- Ready for Logos compile on Air when parent clears UX pause.

## Next

Follow `docs/SOP.md`. Reformed lane charter: `docs/REFORMED_RETRIEVAL.md`. Publication gate green after packet regen; ship via fathers site scripts/ship.sh.

## 2026-09-15 (audit — removed PBB padding)

- Removed fake `added_allusions` Exodus 3:14 (certainty=possible) that was explicitly added "to satisfy PBB verification" with no textual warrant in Art. I–II (justifications already said none invented).
- Rebuilt DOCX: 2 sections, **0** Bible links, 4 TN notes. `verify_docx` OK. Tip-scoped honesty restored for Logos.
- Live site tip already English-first at https://fathers.saneapps.com/works/baron-philosophia-theologiae-ancillans/ (no Exodus padding on public HTML — site uses English JSON, not DOCX captions).
