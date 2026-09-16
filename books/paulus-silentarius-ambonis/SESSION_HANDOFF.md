# Paulus Silentarius: Descriptio Ambonis — production ledger

Canonical path: `~/SaneApps/clients/translations/books/paulus-silentarius-ambonis/`

## Charter

- Title: Paulus Silentarius: Descriptio Ambonis
- Author: Paulus Silentarius (6th century, fl. 563)
- Scope: **Full work densify** — 275 hexameter verses + 29 trimeter prologue. The Ekphrasis of the Ambo of Hagia Sophia, recited separately after the main ekphrasis, likely at Epiphany 563 AD.
- Legal: private study and fathers.saneapps.com publication of new English from locked Greek. No modern copyrighted English copy. Lethaby & Swainson 1894 (Hakluyt Society) is PD English reference only — do not copy.

## Source lock

- **Copy-text:** PG 86b (Migne); Friedländer 1912 Teubner; De Stefani 2011 Teubner. Greek text locked from PG 86b / Friedländer 1912.
- Local: `sources/paulus_silentarius_ambonis_greek_lock.txt` (copy-text); Lethaby & Swainson 1894 as PD English reference; `sources/manifest.json`.
- Lethaby & Swainson 1894 (Hakluyt Society) is public domain — used as PD English reference for densify; new English must be from Greek.

## State

- Sources: locked (Greek copy-text + Lethaby PD English reference)
- Translations: Pass A + Pass B for prologue + body (7 sections total)
- DOCX: built 2026-09-15; verify_docx OK; 7 sections, 14 Bible links, 24 TN notes
- Logos Build: Air backlog after live ship
- Site: publication-review registered; ship next

## 2026-09-15 (densify build + verify complete)

- Created `build_book.py` for prologue + body
- Built DOCX: `paulus-silentarius-ambonis English.docx` — 7 sections, 14 Bible links, 24 TN notes, 0 footnotes
- `python3 -m pipeline.verify_docx` → OK. `python3 -m pipeline.check_pbb_guards` → OK.
- Lethaby & Swainson 1894 not copied; new English from PG 86b / Friedländer 1912 Greek.
- Ready for Logos compile on Air (close panels → Tools → Utilities → Personal Books → Build).
- Next: site publication (era banner; ekphrasis with no earlier English).

## Next

Follow `docs/SOP.md`. Claim `paulus-silentarius-ambonis-densify` prepped; continue densify slices.