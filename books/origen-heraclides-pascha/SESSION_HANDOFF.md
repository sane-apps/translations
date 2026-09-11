# Origen Book 2 — Dialogue with Heraclides + On Pascha

Canonical path: `~/SaneApps/clients/translations/books/origen-heraclides-pascha/`

## Charter

- **Title:** Origen — Dialogue with Heraclides and On Pascha
- **Author:** Origen of Alexandria (c. 185–c. 254)
- **Type:** Monograph. Language: English (new translation).
- **Why these two:** both Toura-papyrus recoveries; short complete (or near-complete)
  Greek works with no usable public-domain English. Modern English (Daly ACW, etc.)
  is copyrighted — **do not copy**.
- **Scope:**
  - *Dialogue with Heraclides* (διάλεκτος πρὸς Ἡρακλείδαν) — full surviving dialogue
    on Father/Son/soul.
  - *On Pascha* (Περὶ Πάσχα) — surviving text of both books as edited from the Toura
    papyrus (lacunae marked, never invented).
- **Out of scope:** Contra Celsum, De Principiis, Prayer, Martyrdom (Book 1).
- **Legal:** private study. New AI-assisted English from locked Greek. No modern
  translation wording. Public site OK when English is ready (fathers.saneapps.com).
- **Sources (locked):** see `sources/manifest.json`.
  - Heraclides: continuous Greek transcribed from Documenta Catholica Omnia /
    Aegean digital Patrologia tradition of Scherer’s text; prefer Scherer SC 67
    page-check when available (IA borrow-restricted).
  - Pascha: Bernd Witte, *Die Schrift des Origenes „Über das Passa“* (1993) —
    Archive.org PDF + OCR (`pascha_witte.pdf` / `pascha_witte_djvu.txt`). Critical
    base also Guéraud–Nautin 1979 (cite; use Witte text for continuous Greek).
- **Enrichment:** inline Bible links + Headword TN marks only. **No Word footnotes.**
  No `logosres:`.

## Status

- 2026-09-10: scaffolded; charter; sources locked.
  - `heraclides_greek.txt` (~37k chars, Scherer/DCO tradition; concordance trimmed).
  - `pascha_witte.pdf` + `pascha_witte_greek_ocr.txt` (tesseract grc OCR; needs cleanup before verified).
- 2026-09-10 (Pascha OCR): **not clean enough to translate.** `sources/pascha_ocr_status.md`. Greek body is ~126 dpi JPEGs; pdftotext = 0 Greek letters; re-OCR `grc+eng` at 180–220 dpi same error class (`tod` for τοῦ). Page images *are* readable. Witte Book I §§1–114 + Book II §§1–35 (149 §§; 31 Greek pages). No `pascha_source.json` (would be invention from dirty OCR). Prefer Witte 1993 over Guéraud–Nautin 1979 for continuous Greek. Do not copy Daly.
- Remaining Origen: `docs/ORIGEN_CORPUS.md`. Next Origen slugs after this book: `origen-jeremiah-samuel` → `origen-john-later` → `origen-song` → `origen-genesis-homilies`.

### 2026-09-11 (Heraclides prose pass)

Rewrote `translations/heraclides_english.json` (28 sections, 119 paragraphs). Scherer page cuts completed so each section can be read alone (hanging clause finished; next page opens with a lead-in). πάπα Ἡρακλείδα / Δημητρίου → "Bishop Heraclides" / "Bishop Demetrius" (translator notes keep the Greek). Minutes feel kept (`Origen said` / `Heraclides said`). Two-Gods / one-power and χωρὶς Θεοῦ not pious-washed. Daly not copied. Justifications updated where a sense choice moved (`heraclides_01`, `_02`, `_24`). Pascha English still not written. On Prayer / Martyrdom not touched.

### 2026-09-10 (Heraclides English finished)

New English from the locked DCO/Scherer Greek. Daly not copied. Grouped by Scherer pages **1–28**, not the 399 DCO micro-rows.

**Wrote**
- `translations/heraclides_source.json` — 28 records (`section` = Scherer page). Title DCO [00001] sits in §1.
- `translations/heraclides_english.json` — 28 records, 118 paragraphs, 147 `added_allusions`. Speaker labels (Origen / Heraclides / Maximus / Dionysius / Demetrius) at paragraph start where the minutes need them.
- `translations/heraclides_scripture_review.json`
- `reviews/justifications/heraclides_01.json` … `heraclides_28.json` (`reviewer: pending-human`). §5 `confidence: uncertain`; the rest `source_verified` with gaps marked.

**Scherer numbering**
- Markers `[1]`–`[25]`, `[27]`, `[28]` are in the dump (often mid-word).
- **`[26]` is not missing text.** DCO prints `ἀπο26 θνῄσκει` at [00365] = `ἀπο[26]θνῄσκει`. Recovered; disclosed in source/justification/review. Do not invent a lost page.
- Page-split words completed for reading (`πρόβλημα`, `πρόσωπον`, `πνευματικόν`, `ἡμετέραν`, `ἀποθνῄσκει`).

**Lacunae / cruxes (not filled)**
- §4 `† τῷ ἀχράντῳ`
- §5 daggered `αν † / ουτ † / και ναι †` (worst stretch)
- §6 `† ειπεναι`; Maximus double-mind dagger
- §8 `ἔσηνεν` uncertain
- §11 `† ὅτι ὡς πρὸς Θεόν` + ellipsis after φρονήσωμεν
- §12 `† ὄντος τοῦ Θεοῦ`
- §17 ellipsis after κωφωθῆναι
- §27 Heb 2:9 **χωρὶς Θεοῦ** kept (not χάριτι Θεοῦ); Jer 1:5 first clause doubled in dump, both copies kept
- §28 `[ὁρῶμεν]` not treated as certain Origen; no Amen added

### 2026-09-11 (Pascha first-pass Greek)

Transcribed Witte 1993 from 300 dpi page images (`sources/witte_pages/p-092.png` … even pages through 152). Not from tesseract. Not from Daly. Lacunae left as Witte printed them.

- `translations/pascha_source.json` — **149 / 149** numbered paragraphs (`1.1`–`1.114`, `2.1`–`2.35`). First pass. **Not `source_verified`.**
- 1.94 is Victor of Capua’s Latin (Greek lost in Witte). Not invented papyrus.
- Status: `sources/pascha_ocr_status.md`.

**Follow-up same session (Heraclides DOCX)**
- `build_book.py` replaced with the Prayer/Martyrdom TN pattern (no Word footnotes).
- DOCX `origen-heraclides-pascha.docx`: 28 sections, 138 Bible links, 94 TN notes. `verify_docx` OK. (Heraclides only; Pascha English not yet in this DOCX.)
- Public site: https://fathers.saneapps.com/works/origen-dialogue-heraclides/
- Logos Personal Book not compiled yet — ready to attach on Air.

### 2026-09-11 (Pascha English)

New English from the locked Witte Greek in `translations/pascha_source.json`. Daly ACW 54 not copied. Witte’s German not copied. No Word footnotes. No Logos compile.

**Wrote**
- `translations/pascha_english.json` — **149 / 149** (`1.1`–`1.114`, `2.1`–`2.35`). 151 paragraphs. 328 `added_allusions`.
- `translations/pascha_scripture_review.json`
- `reviews/justifications/pascha_1_1.json` … `pascha_1_114.json`, `pascha_2_1.json` … `pascha_2_35.json` (149 files; `reviewer: pending-human`).
- Confidence: **122** `source_verified`, **27** `uncertain` (mostly unrestored papyrus).

**Titles** from Witte `head`, polished. Prose: modern literary English; Origen hedges (`τάχα`, `σχεδόν`, `εἴς που`) kept. `διάβασις` = crossing; Book II `ὑπέρβασις` = going-over. `phas` / `phasek` / `pascha` kept where he is naming the word.

**Lacunae (not filled)**
- Unrestored dots / lost lines rendered `[lacuna]`. Witte restorations of damaged text kept in square brackets. Editorial `<insertions>` taken into the reading text and named in `translator_notes`, not shown as angle brackets.
- `[lacuna]` in English: 1.22, 1.26, 1.29, 1.32, 1.35, 1.39, 1.40, 1.45, 1.48, 1.49, 1.53, 1.57, 1.59, 1.60, 1.65, 1.66, 1.82, 1.84, 1.86, 1.95, 1.98, 1.99, 1.106, 2.4, 2.17, 2.22.
- **1.94** — Greek lost; Victor of Capua’s Latin translated. Opening English note: `[The Greek is lost. Victor of Capua preserves this in Latin.]`
- Uncertain justifications: 1.22, 1.26, 1.29, 1.32, 1.35, 1.39, 1.45, 1.48, 1.49, 1.53, 1.58–1.63, 1.65–1.66, 1.82, 1.86, 1.95, 1.98–1.99, 1.106, 2.16–2.17, 2.22.
- Load-bearing claims kept: πάσχα is not from πάθος; type of Christ, not of the passion (serpent on the wood is the passion-type); five days = five senses; raw letter / fire of the Spirit; 1 Cor 5:7 wording as in the papyrus.
- 2.17 quotation blends John 6:53 with John 13:8 (`μερίδα μετ’ ἐμοῦ`); not silently replaced with “life in yourselves.”
- 2.29: Christ goes over the bounds that stood through Adam’s disobedience (not Adam named as Lord).

### 2026-09-11 (Pascha literary pass)

Polished `translations/pascha_english.json` toward the On Prayer bar. Daly not copied. Lacunae not filled. Hedges kept (`τάχα`, `σχεδόν`, `εἴς που`). `phas` / `phasek` / `pascha` and `διάβασις` = crossing kept.

- 1.63: earlier English inverted disciples and crowds. Now: he tells the disciples to have the crowds recline on grass. Justification updated.
- 1.63 / 1.75: bare `lacuna` → `[lacuna]`.
- 2.1–2.3: hanging dashes closed so each section can be read alone.
- 2.35: “starting-points” / “well-disposed and love learning” → “seeds” / “willing and love to learn.”
- Light pass on remaining calques (`speaking thus`, `taken simply`, `one must`).
- Heraclides: `one must` / `Hence` / mid-paragraph `Thus` loosened; scripture `unto` kept.
- DOCX rebuilt: 177 sections (28 + 149), 454 Bible links, 306 TN. `verify_docx` OK. No Logos compile.
- Live: https://fathers.saneapps.com/works/origen-on-pascha/

**Not done**
- Second letter-pass of `pascha_source.json` against `sources/witte_pages/` (Greek still first-pass).
- Logos Personal Book compile (not asked today).

**Next**
- Human review of Pascha justifications (lacuna stretches first).
- Optional second letter-pass of the Greek.
- Air Logos Build when the owner asks.
