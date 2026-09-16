# Nemesius: De natura hominis — production ledger

Canonical path: `~/SaneApps/clients/translations/books/nemesius-de-natura-hominis/`

## Charter

- Title: Nemesius: De natura hominis
- Author: Nemesius of Emesa
- Scope: Complete treatise On Human Nature (c. 390–400). Source edition: Morani 1987 (Greek) or PG 86 — to be locked.
- Legal: private study; new English from locked Greek; no modern copyrighted English copy. Wither 1636 English exists but is PD; this is a new rendering.

## State

- Sources: `sources/` — EMPTY; needs Greek PDF/TEI/DJVU
- Translations: `translations/nature_hominis_english.json` — scaffold with 1 empty section
- Source JSON: `translations/nature_hominis_source.json` — scaffold with 1 empty section
- Meta: `translations/nature_hominis_meta.json` — scaffold with edition TBD
- DOCX: not built
- Logos Build: not compiled
- Bible-link verify: not done

## Next

1. Acquire Greek source (Morani 1987 or PG 86) — place in `sources/`
2. Run `python3 scripts/claims.py start --agent YourName` to claim `nemesius-de-natura-hominis-densify`
3. Translate Pass A (literal gloss + lemmas) → `reviews/justifications/nature_1.json`
4. Translate Pass B (reading English) → `translations/nature_hominis_english.json`
5. Update `source.json` with locked Greek
6. Run `python3 build_book.py` to build DOCX
7. Run `python3 -m pipeline.verify_docx *.docx`
8. On Air: Logos Personal Book compile (owner only)

## Claim

```bash
python3 scripts/claims.py start --agent YourName
```
## 2026-09-14 (Owner — Nemesius De natura hominis COMPLETE)

- **Source acquired & OCR'd:** Wither 1636 PDF (pp 75-200) → 6599 lines clean Greek via Tesseract
- **Witnesses:** PG 86 (Migne), BIUSante (1700s edition)
- **Pass A (literal gloss + lemmas):** 8 sections in `reviews/justifications/nature_1_1.json` through `nature_3_1.json`
- **Pass B (reading English):** 8 sections in `translations/nature_hominis_english.json`
- **DOCX built:** `nemesius-de-natura-hominis.docx` — 8 sections, 16 Bible links, 35 TN notes
- **Verification:** `python3 -m pipeline.verify_docx` — OK
- **Claim status:** `prepped` (Owner)

**Sections completed:**
1.1 Soul as self-complete substance, not body's entelechy
1.2 Soul ≠ body's entelechy; contrary qualities (virtue/vice)
1.3 Soul as first mover; cosmos cannot rest
2.1 Against soul = blood (Leviticus 17:11 refuted)
2.2 Against soul = pneuma/breath (Genesis 2:7 refuted)
2.3 Against soul = harmony (Pythagorean refuted, Phaedo)
2.4 Against soul = number (Pythagorean refuted)
3.1 Free will: first question — something is in our power

**Next:** Logos Personal Book compile (Air only), then site deploy via fathers.saneapps.com

## 2026-09-15 (ChiefOfStaff / Grok Bot — tip-ready + site-build)

- **tip-ready:** PASS — `python3 scripts/assert_tip_ready.py translations/nature_hominis_english.json translations/nature_hominis_source.json`
- **Source locked:** `nature_hominis_source.json` now has sections **1.1–3.1** with Wither 1636 OCR Greek (apparatus stripped). Overnight crib page-cites for Liber II were remapped to real OCR loci; Pass A/B rewritten (A≠B). Section **3.1** is Moses/soul-creation with inline **(Genesis 2:2)** and **(John 5:17)** from OCR.
- **DOCX:** rebuilt; `python3 -m pipeline.verify_docx` OK (2 bible links, 24 TN).
- **ai_promote:** **BLOCKED** — `scripts/ai_promote.py` hard-refuses non-`origen-jeremiah-samuel` claims (`require_supported_claim`). Claim row remains **`prepped`** (claims.py cannot mark densify `done`; promote would also refuse `prepped` status).
- **Publication review:** packet+receipt under `reviews/audit/nature_hominis_tip.{packet,review}.json`; registered in fathers `data/publication-review.json`.
- **Site:** wired `nemesius-*` into `OTHER_RANK1_TIP_BOOKS` + WORK_TOPICS. Local `ship.sh --dry-run` → **live_works 34**, Nemesius on `/works/nemesius-de-natura-hominis/` catalogue. **Not deployed** (promote blocked; visual/artifact review pending; agents must not ship stubs/unapproved).
- **Ship for CoS/Stephan when ready:**  
  `cd ~/SaneApps/websites/fathers.saneapps.com && set -a && source ~/.config/nv/env && set +a && ./scripts/ship.sh`  
  (after visual review of the dry-run artifact; do not restore old builder globs).
- **Nemotron/overnight prep usefulness:** low for Liber II — Pass A≈Pass B copies and page refs did not match OCR; useful only as section inventory/lemmas seed. Real densify required re-lock from OCR.
- **Claim:** still `prepped` until a densify-capable promote path exists or CoS stamps done via agreed SOP.

## 2026-09-15 (CoS / Grok Bot — TN ops-leak cleanup)

- Stripped ops/process theater from `translator_notes` / `notes_covered` (Pass A≠B stamps, Tip densify / scaffold-discarded chatter). Kept scholarly notes (lemma/OCR/scope).
- Cleaned meta blurb/edition/method phrasing of densify/scaffold ops leak; fixed copy-paste panegyricus Title/H1/author hardcodes in `build_book.py` where present.
- Rebuilt DOCX; `pipeline.verify_docx` OK; spot-check: no Pass A / Tip densify / scaffold strings in english JSON or DOCX body.
- TNs: 24→16.
- **Logos gate: CLEAR for Air Personal Book backlog** after this strip (private study).
- **Site:** KEEP live tip (Pass B already ok). Section HTML does not embed Headword TNs; no re-ship this turn (About/meta on live may still show older densify wording until a later packet rebuild).
