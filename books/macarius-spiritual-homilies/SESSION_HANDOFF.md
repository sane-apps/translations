# Macarius: The Spiritual Homilies — production ledger

Canonical path: `~/SaneApps/clients/translations/books/macarius-spiritual-homilies/`

## Charter

- Title: Macarius: The Spiritual Homilies
- Author: Macarius the Egyptian (attributed)
- Scope: 50 Homilies on the spiritual life. Source edition: PG 34 or critical ed. (Campbell 2009) — to be locked.
- Legal: private study; new English from locked Greek; no modern copyrighted English copy. Luibheid 1992 English (PD) exists; this is a new rendering.

## State

- Sources: `sources/` — EMPTY; needs Greek PDF/TEI/DJVU
- Translations: `translations/spiritual_homilies_english.json` — scaffold with 1 empty section
- Source JSON: `translations/spiritual_homilies_source.json` — scaffold with 1 empty section
- Meta: `translations/spiritual_homilies_meta.json` — scaffold with edition TBD
- DOCX: not built
- Logos Build: not compiled
- Bible-link verify: not done

## Next

1. Acquire Greek source (PG 34 or critical ed.) — place in `sources/`
2. Run `python3 scripts/claims.py start --agent YourName` to claim `macarius-spiritual-homilies-densify`
3. Translate Pass A (literal gloss + lemmas) → `reviews/justifications/mac_1.json`
4. Translate Pass B (reading English) → `translations/spiritual_homilies_english.json`
5. Update `source.json` with locked Greek
6. Run `python3 build_book.py` to build DOCX
7. Run `python3 -m pipeline.verify_docx *.docx`
8. On Air: Logos Personal Book compile (owner only)

## Claim

```bash
python3 scripts/claims.py start --agent YourName
```

## 2026-09-15 (ChiefOfStaff / Grok Bot — tip-ready + live ship)

- **tip-ready:** PASS — `assert_tip_ready.py` on spiritual_homilies_{english,source}.json (Homilies 5–6).
- **Source locked:** PG 34 OCR Greek; Latin column stripped; Hom 6 locus from Ἀγωνισώμεθα through Xanthicus (stigma header lost in OCR).
- **Pass B densified:** real reading English; Pass A≠B; scripture gate inline; justifications mac_5/mac_6.
- **DOCX:** rebuilt; `pipeline.verify_docx` OK — no footnotes.xml; inline `[[… >> Bible:…]]`; Headword TN marks; Heading styles; no logosres:.
- **ai_promote:** still Jeremiah-only — claim remains **prepped**.
- **Site:** wired `macarius-*` into OTHER_RANK1_TIP_BOOKS + WORK_TOPICS; publication packet+receipt under `reviews/audit/spiritual_homilies_tip.{packet,review}.json`.
- **Live:** https://fathers.saneapps.com/works/macarius-spiritual-homilies/ (200) — tip Homilies 5–6.
- **Logos Personal Book:** compile pending on Air (owner) — cover art, description, upload backlog; DOCX at `macarius-spiritual-homilies.docx`.
- **Collision:** OpenCode PID left alone; did not touch cosmas/paulus/photius.
- **Next densify:** philostorgius-he (CLAIMS prepped order).

## 2026-09-15 (CoS / Grok Bot — TN ops-leak cleanup)

- Stripped ops/process theater from `translator_notes` / `notes_covered` (Pass A≠B stamps, Tip densify / scaffold-discarded chatter). Kept scholarly notes (lemma/OCR/scope).
- Cleaned meta blurb/edition/method phrasing of densify/scaffold ops leak; fixed copy-paste panegyricus Title/H1/author hardcodes in `build_book.py` where present.
- Rebuilt DOCX; `pipeline.verify_docx` OK; spot-check: no Pass A / Tip densify / scaffold strings in english JSON or DOCX body.
- TNs: 9→7.
- **Logos gate: CLEAR for Air Personal Book backlog** after this strip (private study).
- **Site:** KEEP live tip (Pass B already ok). Section HTML does not embed Headword TNs; no re-ship this turn (About/meta on live may still show older densify wording until a later packet rebuild).
