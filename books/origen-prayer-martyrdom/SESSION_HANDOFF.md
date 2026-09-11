# Origen Book 1 — On Prayer + Exhortation to Martyrdom

Canonical path: `~/SaneApps/clients/translations/books/origen-prayer-martyrdom/`

## Charter

- **Title:** Origen: On Prayer and Exhortation to Martyrdom
- **Author:** Origen of Alexandria (c. 185–c. 254)
- **Type:** Monograph. Language: English (new translation).
- **Why these two:** both short complete Greek treatises from the same window
  (c. 233–235, Maximinus persecution), written for the same patron Ambrose
  (Martyrdom adds Protoctetus; Prayer adds Tatiana). Zero public-domain
  English exists for either: only copyrighted modern versions
  (O'Meara ACW 19, Greer CWS 1979, Oulton/Chadwick LCC 1954 selections,
  Daly for Heraclides/Pascha — all DO NOT COPY).
- **Scope:** the full surviving text of both treatises as printed by Koetschau.
  Out of scope: Contra Celsum (ANF 4 serves it), De Principiis (ANF 4 + repo
  excerpts serve it), and everything else Origen (Book 2+).
- **Numbering:** Koetschau's chapter numbers are followed exactly, including
  Martyrdom LI (51) at the close. Disclosed, not normalized.
- **Legal:** private study. New AI-assisted English from the 1899 GCS editions
  (public domain). No modern translation copied or consulted for wording.
  No public publish unless the owner asks.
- **Sources:** `sources/gcs2_bd1_full_ocr.txt` (Bd 1, GCS 2) and
  `sources/gcs3_bd2_full_ocr.txt` (Bd 2, GCS 3), sliced to
  `gcs2_martyrium_slice.txt` / `gcs3_gebet_slice.txt`.
  See `sources/manifest.json` for URLs + SHA256.
- **Known source limits:** Google OCR of 1899 Greek is noisy (breathings,
  minuscule confusions, Latin-script intrusions like MAPTYPION). Apparatus
  lines are separated at ingest but every chapter is re-read against the
  slice before translating; unreadable words go `[lacuna]`, never invented.
  Manuscript sigils (A B C M P T, Ox. Lond. Del. Bo. Rob.) are recorded in
  justifications where they affect sense.
- **Enrichment policy (Logos):** Bible datatype links + Headword milestones +
  Headword TN note links + Word-native footnotes + internal bookmarks +
  external source URLs + hand-built Scripture index ONLY. No `logosres:` /
  cross-resource links (they hardcode owner library IDs and confront
  recipients without the resource with a store prompt — verified by PBB
  research 2026-09-10), no Strong's/GK/Louw-Nida, no alternate Bible
  datatypes, no new milestones. See research note in handoff history.

## Session log

### 2026-09-10 (Air, Muse)

- Surveyed full Origen corpus; ranked Prayer + Martyrdom first (pure PD gap).
- Locked sources: archive.org `origenes-werke.-bd-1-1899` (GCS 2, Martyrium
  Bd I 3,1–47,16) and `origenes-werke.-bd-2-1899` (GCS 3, Gebet
  Bd II 297,1–403,10). Rejected `origeneswerkevo00baehgoog` as a Gebet
  source after prayer-vocab counts refuted the assumption (Celsus scan).
- Scaffolded via `pipeline.new_book`; ingest in `scripts/extract_sources.py`.
- Charter written. Translation in progress (Gebet first, then Martyrdom).
- Gebet chs. I–V complete with source/english/justification files
  (source_verified, reviewer pending-human). 6 T-gaps/lacunae marked,
  conjectures refused. Segmentation model proven: chapter heads mostly
  lost in OCR; chapters delimited by §-resets + running heads
  (pp. 299/301/303/305/306/309 confirm I–V) + topic blocks.
  Systematic 3→8 glyph confusion documented (verify on page images).
- STOP POINT per owner: no Logos GUI work. Build DOCX + verify + audit,
  then report ready-to-attach. Owner handles Personal Books Build on Air.

### 2026-09-10 (later, Muse — translation + build complete)

- Translated Gebet XV–XXXIV (20 chapters) and all of Martyrdom (proem + 51):
  `translations/gebet_english.json` (34/34), `martyrium_english.json` (52 entries),
  sources extended (`gebet_source.json` 34, new `martyrium_source.json` 52),
  justifications 34 + 52 (all source_verified, pending-human).
- Chapter-number rulings: Gebet XXII/XXIII split per running heads (XXII §§1-2,
  XXIII §§1-5); Martyrdom XIII/XIV seam — XIV opening (promartyron) recovered
  from slice, added as section 13; GCS print duplicates XV in Bd I pp. 20-24,
  content sequence followed. All flagged for page-image verification.
- Scripture review receipts written for both works; load-bearing (?) cruxes:
  Gebet XVI (T damage/lacuna), XXII/XXIII, XXIX, XXX; Mart 11, 41 (Germany).
- Built `origen-prayer-martyrdom.docx` (137KB): 86 sections, 216 paragraphs,
  612 Bible links, 88 headwords, 144 footnotes, 88 bookmarks.
  `verify_docx` OK; all 612 targets parse; 0 placeholders/TODO/junk/empties.
- READY-TO-ATTACH. Remaining human gates (owner): page-image verification of
  flagged passages, then Air Personal Books Build + 0-errors check +
  `verify_logos_db`. No GUI work done here per stop point.

### 2026-09-10 (Cursor — review + Logos attach)

- Re-verified: `verify_docx` OK; 86 justifications `source_verified` /
  `pending-human`; gebet/martyrium english↔source section sets match 1:1
  (34 + 52). Germany crux matches GCS slice `ἀνῃρέθην ἐν Γερμανίᾳ` with
  honest `(?)` flags in English.
- Fixed compound Bible-loc expansion before attach: semicolon chapter groups
  (`John 13:1,3; 14:23,28; 16:5`) had been mis-split into illegal
  `John 28; 16:5` targets. `_expand_comma_verses` + caption emit path repaired;
  rebuilt DOCX → **571** clean Bible links, 0 semicolon targets, 0 `logosres:`,
  88 Headwords, 144 footnotes.
- Air Logos Personal Book **Id=6**, ResourceId
  `PBB:4f41cb276f014e1aa7ee22103e299a76`. Body:
  `books/origen-prayer-martyrdom/origen-prayer-martyrdom.docx`.
- Build observed: **0 errors, 0 warnings.** LastCompiled
  `2026-09-10T17:54:40-04:00`. `verify_logos_db --title-substr "Origen: On Prayer"`
  OK; ArticleCache 89; 0 Headword/jargon pollution. TOC samples clean
  (`On Prayer`, `On Prayer 1`). Receipts under
  `outputs/logos-attach-2026-09-10/`.
- Page-image gate still open for flagged OCR cruxes (Gebet XVI T damage,
  XXII/XXIII, Mart XIII/XIV, Mart 41 Germany commentary) — not blocking
  private-study attach; disclosed in footnotes/justifications.
- Next: owner page-image pass if desired; Book 2 when asked.

### 2026-09-10 (Cursor — footnotes + inline Scripture fix)

- Word footnotes were ignored by Logos PBB (hover fell back to book description).
  Switched to Ante-Nicene pattern: `[[ⁿ >> Headword:TN n]]` + Translator notes section.
  ArticleCache now has A_TN1…A_TN144.
- Removed "Scripture connection:" caption dumps. Clear allusions are injected as
  parenthetical Bible links beside the matching clause in the English paragraphs.
  Only `possible` allusions stay as short captions.
- Rebuilt DOCX + Logos Id=6: 0 errors, 1 warning (same class as Ante-Nicene often
  shows). verify_logos_db OK. LastCompiled 2026-09-10T18:03:49-04:00.
