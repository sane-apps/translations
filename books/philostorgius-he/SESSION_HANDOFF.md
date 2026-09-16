# Philostorgius: Ecclesiastical History — production ledger

Canonical path: `~/SaneApps/clients/translations/books/philostorgius-he/`

## Charter

- Title: Philostorgius: Ecclesiastical History
- Author: Philostorgius
- Scope: Books 1–12 (as preserved). Source edition: Bidez 1913 (Greek) or PG 65 — to be locked.
- Legal: private study; new English from locked Greek; no modern copyrighted English copy. Walford 1855 English (PD) exists; this is a new rendering.

## State

- Sources: `sources/` — EMPTY; needs Greek PDF/TEI/DJVU
- Translations: `translations/ecclesiastical_history_english.json` — scaffold with 1 empty section
- Source JSON: `translations/ecclesiastical_history_source.json` — scaffold with 1 empty section
- Meta: `translations/ecclesiastical_history_meta.json` — scaffold with edition TBD
- DOCX: not built
- Logos Build: not compiled
- Bible-link verify: not done

## Next

1. Acquire Greek source (Bidez 1913 or PG 65) — place in `sources/`
2. Run `python3 scripts/claims.py start --agent YourName` to claim `philostorgius-he-densify`
3. Translate Pass A (literal gloss + lemmas) → `reviews/justifications/phil_1.json`
4. Translate Pass B (reading English) → `translations/ecclesiastical_history_english.json`
5. Update `source.json` with locked Greek
6. Run `python3 build_book.py` to build DOCX
7. Run `python3 -m pipeline.verify_docx *.docx`
8. On Air: Logos Personal Book compile (owner only)

## Claim

```bash
python3 scripts/claims.py start --agent YourName
```

## 2026-09-15 (ChiefOfStaff / Grok Bot — tip-ready + ship path)

- **tip-ready:** PASS for Book 1 tip.
- **Source locked:** Bidez 1913 tess OCR Greek (pages ~181-190); apparatus stripped; Δικαίᾳ≈Νικαίᾳ disclosed.
- **DOCX:** rebuilt; verify_docx OK; Logos markup (inline Bible, Headword TN, no footnotes.xml).
- **Claim:** remains **prepped** (ai_promote Jeremiah-only).
- **Logos Personal Book:** compile pending on Air.
- **Next:** live ship after visual review of dry-run artifact.


## 2026-09-15 (ChiefOfStaff / Grok Bot — live ship)

- **Live:** https://fathers.saneapps.com/works/philostorgius-he/ (200) and `/1/` (200). Deploy `562928b8.fathers-site.pages.dev`. live_works=36.
- **Visual review:** artifact `e3e27f8037fd64521e6220642bf8a06c1bf73b17bf9f45a5e406cae96ec7ae54` passed image-inspection (32 shots).
- **Claim:** remains **prepped** (ai_promote Jeremiah-only).
- **Logos Personal Book:** compile pending on Air (cover art, description, upload). DOCX at `philostorgius-he.docx`.
- **Collision:** OpenCode PID left alone; did not touch cosmas/paulus/photius.
- **Next densify:** greg-thaum-fide-xii (CLAIMS prepped order).

## 2026-09-15 (CoS hard fix — Pass B tip rewrite)

- **Problem:** live tip English opened with editorial frame (“preserved chiefly through Photius…”) instead of locked Greek (Maccabees/Daniel judgments).
- **Fix:** Pass B rewritten to track `sources/_phil1_greek_lock.txt` order: Maccabees 1–4 → Phlegon/Josephus → Eusebius piety fault → Arius/Baukalis/homoousion → Constantius/York → Constantine/Maxentius.
- Removed unsourced Prov 8 / John 1 / Col 1 / Heb 1 packing; Daniel 8 / Daniel 11 kept as sourced.
- No densify/ops-leak prose in reading English; Pass A≠B justifications updated; audit packet+receipt regenerated (`packet_id` 86a4b67e…).
- DOCX rebuilt; `verify_docx` OK; tip-ready ok.
- **Site:** rewrite done — reship required so live URL matches lock (prefer rewrite+reship).
