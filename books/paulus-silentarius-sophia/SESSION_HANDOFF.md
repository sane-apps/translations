# Paulus Silentarius: Descriptio Sanctae Sophiae — production ledger

Canonical path: `~/SaneApps/clients/translations/books/paulus-silentarius-sophia/`

## Charter

- Title: Paulus Silentarius: Descriptio Sanctae Sophiae
- Author: Paulus Silentarius (6th century, fl. 563)
- Scope: **Full work densify** — 1046 hexameter verses in 3 parts: (1) The Dome and Nave (vv. 1-350), (2) The Exedras and Piers (vv. 351-800), (3) The Ambo and Conclusion (vv. 801-1046). Recited at the rededication of Hagia Sophia, 24 December 563 AD.
- Legal: private study and fathers.saneapps.com publication of new English from locked Greek. No modern copyrighted English copy. Lethaby & Swainson 1894 (Hakluyt Society) is PD English reference only — do not copy.

## Source lock

- **Copy-text:** PG 86b (Migne) / Friedländer 1912 Teubner / De Stefani 2011 Teubner. Greek text locked from PG 86b / Friedländer 1912.
- Local: `sources/paulus_silentarius_greek_lock.txt` (copy-text); Lethaby & Swainson 1894 as PD English reference; `sources/manifest.json`.
- Lethaby & Swainson 1894 (Hakluyt Society) is public domain — used as PD English reference for densify; new English must be from Greek.

## State

- Sources: locked (Greek copy-text + Lethaby PD English reference)
- Translations: Pass A + Pass B for all 3 parts (8 sections total)
- DOCX: built 2026-09-15; verify_docx OK; 8 sections, 20 Bible links, 24 TN notes
- Logos Build: Air backlog after live ship
- Site: publication-review registered; ship next

## 2026-09-15 (densify build + verify complete)

- Created `build_book.py` for all 3 parts (8 sections total)
- Built DOCX: `paulus-silentarius-sophia English.docx` — 8 sections, 20 Bible links, 24 TN notes, 0 footnotes
- `python3 -m pipeline.verify_docx` → OK. `python3 -m pipeline.check_pbb_guards` → OK.
- Lethaby & Swainson 1894 not copied; new English from PG 86b / Friedländer 1912 Greek.
- Part 1 (Dome & Nave): 3 sections, 12 Bible links, 9 TN notes
- Part 2 (Exedras & Piers): 3 sections, 6 Bible links, 9 TN notes
- Part 3 (Ambo & Conclusion): 2 sections, 2 Bible links, 6 TN notes
- Ready for Logos compile on Air (close panels → Tools → Utilities → Personal Books → Build).
- Next: site publication (era banner; ekphrasis with no earlier English).

## Next

Follow `docs/SOP.md`. Claim `paulus-silentarius-sophia-densify` prepped; continue densify slices.
EOF