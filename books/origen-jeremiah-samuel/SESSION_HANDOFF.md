# Origen: Homilies on Jeremiah and on 1 Samuel 28 — production ledger

Canonical path: `~/SaneApps/clients/translations/books/origen-jeremiah-samuel/`

## Charter

- Title: Origen: Homilies on Jeremiah and on 1 Samuel 28
- Author: Origen of Alexandria
- Scope: GCS Orig. III (Klostermann 1901): 20 Greek Jeremiah homilies, Lamentations fragments, Homily on 1 Kingdoms 28. Two further Jeremiah homilies survive only in Jerome’s Latin and are not in this Greek lock. Not the complete Origen corpus.
- Legal: private study; new English from GCS 1901. First1KGreek TEI is a transcription of that edition. PDF + djvu.txt retained as witnesses. Do not copy FOTC 97 (Smith).

## State

- 2026-09-11 (StephanMini grind): Homily **5** Pass B + AI promote done (`jer-h5a`/`jer-h5b`/`jer-h5c`). Receipts under `outputs/ai-promote/20260912T033224Z-jer-h5a`, `…033544Z-jer-h5b`, `…033821Z-jer-h5c`. OCR `Μνῶν`→ἐθνῶν noted. Next prepped: Homilies 11–20. Site deploy / Logos left to SOP owner lane.


- 2026-09-11 (EOD): **Homily 8 (`jer-h8`)** claimed by `overnight-mini-nv`. English draft present; AI promote may still be running on Mini. Do not re-claim. Next free Homily 5 splits `jer-h5a/b/c`, then 11–20. Overnight: Mini calendar 21:10 + flock locks (`docs/AI_CROSSCHECK.md`).
- 2026-09-11 (witness disclosure): Site “About this text” names GCS 1901 as copy-text, Archive page image/DjVu and First1KGreek TEI as checks of the same print, and the three TEI-vs-page-image joins in Homilies 1.1, 1.5, and 1.11. `publish_homilies: [1, 2]` keeps later JSON drafts off the public reader. Do not claim PG 13 or Jerome until those are locked and shipped. No silent merge.
- 2026-09-11 (evening): **Homilies 6, 7, 9, 10** AI-done (`jer-h6`/`jer-h7`/`jer-h9`/`jer-h10`) via `draft_claim.py` + `ai_promote.py` (Qwen draft; Gemma + Llama 70B). Fixed ἐπιδημία→sojourn (not “epidemic”). Daily burner: `scripts/overnight_quota.py`. Logos still owner-only on Air.
- 2026-09-11 (afternoon): **Homilies 3–4** translated (8 §§). First pass from GCS Greek lock; second pass (literary tighten on 3.1; Scripture/OCR gap notes on Matt 5:45 and Acts echoes). Justifications `jeremiah_3_1`…`jeremiah_4_6` (`source_verified`; promote via AI cross-check — no standing human review gate). Scripture review entry appended. DOCX rebuilt: **27** sections / 111 Bible links / 13 TN; `verify_docx` OK. Site updated (Homilies 1–4 of 20). Thought titles on each section for the fathers reader SOP. Logos not compiled.
- 2026-09-11: Greek locked. Homilies 1–2 English (19 §§). Pipeline review against Klostermann PDF + TEI: Jonah as Hebrew prophet; make/form in the womb; nitre/soap; no tropology jargon. Scripture review + 19 justifications (`source_verified`; AI cross-check path for done). DOCX 19 sections / 111 Bible links / 7 TN; `verify_docx` OK. Site work `origen-homilies-jeremiah` (Homilies 1–2 of 20; in progress). Logos not compiled.
- Sources: `sources/origeneswerke03orig.pdf`, `_djvu.txt`, `sources/first1k/*.xml`, `sources/manifest.json`.
- Locked Greek: `books/origen-jeremiah-samuel/translations/jeremiah_source.json` (155 §§), also `samuel_source.json` (10), `lamentations_source.json` (118).
- Pass B English: `books/origen-jeremiah-samuel/translations/jeremiah_english.json` (Homilies **1–4**, **6–7**, **9–10**; Homily **8** draft under `jer-h8` claim; Homily **5** still free as `jer-h5a/b/c`).
- Pass A + receipts: `books/origen-jeremiah-samuel/reviews/justifications/jeremiah_H_S.json` (section `H.S` → that basename; copy `jeremiah_1_1.json`). Every new section needs `pass_a_gloss` ≠ joined Pass B.
- **Debt:** Homilies 3–4 receipts (`jeremiah_3_*`, `jeremiah_4_*`) are missing `pass_a_gloss` — backfill before treating those as SOP-complete; do not copy that incomplete shape for new claims.
- Contributor claims: `python3 scripts/claims.py start --agent YourName` (see `docs/START_HERE.md`). Homily 5 is split `jer-h5a` / `jer-h5b` / `jer-h5c`.

## Next

Finish/sync **`jer-h8`** when Mini promote settles (pull CLAIMS + english/justifications from Mini). Then Homilies **5**, **11–20**, then 1 Samuel 28, then Lamentations fragments. Do not present the current English set as the complete volume. **Logos Personal Book compile stays on the owner’s MacBook Air only** — contributors and overnight agents never run `build_book.py` / Logos Build; when a volume’s English is far enough along, the owner batches PBB compile locally.
