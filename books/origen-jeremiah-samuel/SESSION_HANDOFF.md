# Origen: Homilies on Jeremiah and on 1 Samuel 28 — production ledger

Canonical path: `~/SaneApps/clients/translations/books/origen-jeremiah-samuel/`

## Charter

- Title: Origen: Homilies on Jeremiah and on 1 Samuel 28
- Author: Origen of Alexandria
- Scope: GCS Orig. III (Klostermann 1901): 20 Greek Jeremiah homilies, Lamentations fragments, Homily on 1 Kingdoms 28. Two further Jeremiah homilies survive only in Jerome’s Latin and are not in this Greek lock. Not the complete Origen corpus.
- Legal: private study; new English from GCS 1901. First1KGreek TEI is a transcription of that edition. PDF + djvu.txt retained as witnesses. Do not copy FOTC 97 (Smith).

## State

- 2026-09-11 (afternoon): **Homilies 3–4** translated (8 §§). First pass from GCS Greek lock; second pass (literary tighten on 3.1; Scripture/OCR gap notes on Matt 5:45 and Acts echoes). Justifications `jeremiah_3_1`…`jeremiah_4_6` (`source_verified`, pending-human). Scripture review entry appended. DOCX rebuilt: **27** sections / 111 Bible links / 13 TN; `verify_docx` OK. Site updated (Homilies 1–4 of 20). Thought titles on each section for the fathers reader SOP. Logos not compiled.
- 2026-09-11: Greek locked. Homilies 1–2 English (19 §§). Pipeline review against Klostermann PDF + TEI: Jonah as Hebrew prophet; make/form in the womb; nitre/soap; no tropology jargon. Scripture review + 19 justifications (`source_verified`, pending-human). DOCX 19 sections / 111 Bible links / 7 TN; `verify_docx` OK. Site work `origen-homilies-jeremiah` (Homilies 1–2 of 20; in progress). Logos not compiled.
- Sources: `sources/origeneswerke03orig.pdf`, `_djvu.txt`, `sources/first1k/*.xml`, `sources/manifest.json`.
- Locked Greek: `books/origen-jeremiah-samuel/translations/jeremiah_source.json` (155 §§), also `samuel_source.json` (10), `lamentations_source.json` (118).
- Pass B English: `books/origen-jeremiah-samuel/translations/jeremiah_english.json` (Homilies **1–4** = 27 §§ so far).
- Pass A + receipts: `books/origen-jeremiah-samuel/reviews/justifications/jeremiah_H_S.json` (section `H.S` → that basename; copy `jeremiah_1_1.json`). Every new section needs `pass_a_gloss` ≠ joined Pass B.
- **Debt:** Homilies 3–4 receipts (`jeremiah_3_*`, `jeremiah_4_*`) are missing `pass_a_gloss` — backfill before treating those as SOP-complete; do not copy that incomplete shape for new claims.
- Contributor claims: take a free row via `python3 scripts/claims.py take <id> --agent YourName` (see `docs/START_HERE.md`). Homily 5 is split `jer-h5a` / `jer-h5b` / `jer-h5c`.

## Next

Homilies 5–20, then 1 Samuel 28, then Lamentations fragments. Do not present Homilies 1–4 as the complete volume. Logos compile when the owner asks — keep this as its own monograph for now (separate from Origen Prayer/Martyrdom and Heraclides/Pascha); bundling into a multi-volume Origen series is undecided.
