# Cyril of Alexandria — Fragments on Matthew

Canonical path: `~/SaneApps/clients/translations/books/cyril-alexandria-matthew-fragments/`

## Charter

- **Title:** Cyril of Alexandria: Fragments on Matthew
- **Author:** Cyril of Alexandria (d. 444) — **not** Origen on Matthew
- **CPG:** **5206** *Fragmenta in Matthaeum* (catena fragments)
- **Type:** Monograph. Language: English (new translation).
- **Scope:** Surviving Greek catena fragments on Matthew. Continuous commentary is lost; do not ship as a finished continuous commentary.
- **Out of scope:** CPG 5219/5220 (*recta fide* — closed). Origen Matthew. Melito. Reuss TU 61 as copy-text (copyright).
- **Legal:** private study. New English from locked PD Greek (Migne PG 72 extract). No modern English copy.
- **Enrichment:** inline Bible links + Headword TN marks when built. No Word footnotes. No CSS on site claims.

## Source lock (2026-09-12)

- **Copy-text:** `sources/khazarzar_commentarii_in_matthaeum.pdf` + `.txt` (Aegean Digital Patrologia / khazarzar). SHA256 PDF `695f6e2a…6908`.
- **Mirror check:** `matia_commentarii_in_matthaeum.pdf` — **byte-identical** to khazarzar (same witness family).
- **IA PG 72 OCR** (`ia_pg72_bim_djvu.txt`): independent volume lineage; **OCR junk — not copy-text**, locus confirmation only (~cols 365ff). No silent merge.
- Manifest: `sources/manifest.json`
- Source JSON: `translations/matthew_fragments_source.json` (**290** fragment heads parsed)
- Meta / text history: `translations/matthew_fragments_meta.json`

## Claims

| Claim | Status | Slice |
|-------|--------|-------|
| `cyril-matt-frag-lock` | done | Source lock only |
| `cyril-matt-frag-a1` … `a15` | done | entries 1–60 |
| `cyril-matt-frag-a16` | done | entries 61–64 (ed. fr.70–74; Mt 6:2–16) Pass A≠B |
| `cyril-matt-frag-a17` | done | entries 65–68 (ed. fr.75–80; Mt 6:16–25); lacuna on 65 disclosed |
| `cyril-matt-frag-a18` | done | entries 69–72 (ed. fr.81–84; Mt 6:25–7:5) Pass A≠B |
| `cyril-matt-frag-a19` | done | entries 73–76 (ed. fr.85–89; Mt 7:7–26) Pass A≠B |

## Next

- `cyril-matt-frag-a20` from entry 77 (Mt 8+)
- Keep IA OCR out of reading text
- Skip Melito; preserve jer-h20b; no CSS; CPG 5219/5220 stay closed
