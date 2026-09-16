# Photius: Bibliotheca (Myriobiblon) — production ledger

Canonical path: `~/SaneApps/clients/translations/books/photius-bibliotheca/`

## Charter

- Title: Photius: Bibliotheca (Myriobiblon)
- Author: Photius of Constantinople (c. 820–891)
- Scope: **densify** — full work 279 codices. Claim `photius-bibliotheca-densify` prepped. Freese 1920 (PD English, codices 1-165) is reference only — do not copy. No modern copyrighted English.
- Legal: private study and fathers.saneapps.com publication of new English from locked Greek.

## Source lock

- **Copy-text:** Bekker, *Photii Bibliotheca* (Berlin 1824). Also PG 103 (Schott Latin). Greek text reconstructed from multiple PD witnesses.
- Local: `sources/photius_bibliotheca_greek_lock.txt` (copy-text, codices 1-17); Freese 1920 Vol. I as PD English reference; `sources/manifest.json`.
- Freese 1920 Vol. I (codices 1-165) is public domain — used as PD English reference for densify; new English must be from Greek.

## State

- Sources: locked (Greek copy-text + Freese PD English reference)
- Translations: Pass A + Pass B for codices 1-10
- DOCX: built 2026-09-15; verify_docx OK; 10 sections, 3 Bible links, 25 TN notes
- Logos Build: Air backlog after live ship
- Site: publication-review registered; ship next

## 2026-09-15 (densify tip build + verify complete)

- Created `build_book.py` for codices 1-10
- Built DOCX: `photius-bibliotheca English.docx` — 10 sections, 3 Bible links, 25 TN notes, 0 footnotes
- `python3 -m pipeline.verify_docx` → OK. `python3 -m pipeline.check_pbb_guards` → OK.
- Freese 1920 not copied; new English from Bekker 1824 Greek.
- Codices 1-5: Theodore on Dionysius, Hadrian, Nonnosus, Theodore of Mopsuestia, Sophronius
- Codices 6-10: Gregory of Nyssa ×2 (Against Eunomius), Origen (De Principiis), Eusebius (Praeparatio Evangelica, Demonstratio Evangelica)
- Next: codices 11-15 (Eusebius lost works, Apollinarius, Gelasius, Acts of Councils)

## Next

Follow `docs/SOP.md`. Claim `photius-bibliotheca-densify` prepped; continue densify slices.

## 2026-09-15 (CoS hard fix — ops-leak TN strip)

- Stripped ops-leak `translator_notes` naming `claim photius-bibliotheca-densify` + `reviews/justifications/...` paths from english JSON (codices 1–9).
- **TN counts:** before **31** total across codex english files → after **22** (9 stripped). Tip codices 1–5 DOCX TN notes: **18 → 13**.
- Scholarly lexical/historical notes kept.
- FRONT_MATTER densify-claim name removed from DOCX front matter.
- Tip DOCX rebuilt (codices 1–5 only); `verify_docx` OK; no further densify; OpenCode Cosmas/Paulus densify untouched.
