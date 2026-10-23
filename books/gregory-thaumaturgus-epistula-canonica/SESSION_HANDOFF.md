# Gregory Thaumaturgus: Epistula canonica — production ledger

Canonical path: `~/SaneApps/clients/translations/books/gregory-thaumaturgus-epistula-canonica/`

## Charter

- Title: Gregory Thaumaturgus: Epistula canonica
- Author: Gregory Thaumaturgus
- Scope: (fill)
- Legal: private study; new English from allowed sources; no modern copyrighted English copy.

## State

- Sources: not started
- Translations: not started
- DOCX: not built
- Logos Build: not compiled
- Bible-link verify: not done

## Next

Follow `docs/SOP.md`.

## 2026-09-15 (Grok Bot — tip-ready)

- **tip-ready:** PASS for Canon I (captives / captive women).
- **Source locked:** Documenta Catholica Omnia Canones GR; scaffold English discarded.
- **Pass A≠B:** `reviews/justifications/epistula_1.json` OK.
- **DOCX:** `gregory-thaumaturgus-epistula-canonica.docx`; verify_docx OK; inline Bible (1 Cor 6:13, Matt 15:11, Deut 22:25-27).
- **Live:** https://fathers.saneapps.com/works/gregory-thaumaturgus-epistula-canonica/ (200); `/1/` (200). Deploy `5590190c.fathers-site.pages.dev`. live_works=43.
- **Claim:** remains **prepped**.
- **Logos:** compile pending on Air.

## 2026-09-15 (CoS / Grok Bot — TN ops-leak cleanup)

- Stripped ops/process theater from `translator_notes` / `notes_covered` (Pass A≠B stamps, Tip densify / scaffold-discarded chatter). Kept scholarly notes (lemma/OCR/scope).
- Cleaned meta blurb/edition/method phrasing of densify/scaffold ops leak; fixed copy-paste panegyricus Title/H1/author hardcodes in `build_book.py` where present.
- Rebuilt DOCX; `pipeline.verify_docx` OK; spot-check: no Pass A / Tip densify / scaffold strings in english JSON or DOCX body.
- TNs: 3→2.
- **Logos gate: CLEAR for Air Personal Book backlog** after this strip (private study).
- **Site:** KEEP live tip (Pass B already ok). Section HTML does not embed Headword TNs; no re-ship this turn (About/meta on live may still show older densify wording until a later packet rebuild).

## 2026-10-23 (Claude, Mini — Canons 2-11 translated; whole letter now in English)

- **Translated:** Canons 2-11 (sections 2-11), by Claude directly from the Greek; Cloudflare AI off, no outside model called. Canon 1 rows left as they were. The letter now has all 11 canons.
- **Copy-text read:** `sources/canones_GR.pdf` (Documenta Catholica Omnia "Canones GR" typed print), page images at 300 dpi, pages 1-3 (Canons 2-3 on p. 1; Canons 4-10 and the Canon 11 rubric on p. 2; Canon 11 text on p. 3), matched against `canones_GR.txt`. Vossius' Latin notes (`sources/epistula_canonica_djvu.txt`) used for Canons 5 and 11; they hold no running Greek. PG 10 not in hand. Rubrics of the canon collection left out of `greek` (editorial, not Gregory's); print slips corrected and listed in each source row's `notes`.
- **Files:** 10 rows appended to `translations/epistula_canonica_source.json` and `translations/epistula_canonica_english.json` in reading order; new `reviews/justifications/2.json` to `11.json`; `translations/epistula_canonica_meta.json` (title "Canonical Letter", scope "Canons 1–11", blurb, era_note, first_english_note, text_history.method, edition); `book.yml` (description scope sentence, "Fresh English translation", edition).
- **Review:** fresh-context review of every clause of Canons 2-11 against the Greek and the page-image crops c2b, c2c, c2d, c2e, c3a. Verdict pass for all 10. Changes made in review: Canon 2 ("denounced as", "the mark of impious men", restored γάρ); Canon 7 (closing clause matches δόξῃ … τῷ ἁγίῳ Πνεύματι and the Acts 15:28 echo); Canon 8 ("the rank of those who are returning"); Canon 9 (modality "are to be admitted"); Canon 10 (spelling "fulfill").
- **Assembly change (structural gate only):** Canon 7 English was one 93-word sentence and failed the `check_pass_ab` sentence-shape rule; split at the dash ("Some were enlisted … did not know them. These must be barred …"); no clause added or dropped. Greek parentheticals moved out of Pass A into `lemmas[]` so Pass A reads as English.
- **Checks:** `python3 -m pipeline.check_pass_ab` on justifications 2-11: ok=10 fail=0. `--tip-ready` on the english/source pair: ok. `pipeline.verify_translation_qa` structural packet (scratch only, not saved in the book): OK.
- **Open doubts:** Canon 5, the print's καὶ αὐτὸς δῴῃ ("he too may give direction") is followed; Vossius' Latin suggests ἐκεῖ ("there"), with no Greek witness in hand to check it (recorded in the translator note). Canon 5, συγγέρων "fellow elder" keeps both senses open (fellow presbyter, or companion in old age as ANF reads it). Canon 6, μὴ καὶ σκηπτοὶ πέσωσιν "lest thunderbolts fall" (καί only intensifies). Canon 8, ἐν τῇ τῶν ὑποστρεφόντων τάξει ὑποπίπτειν not checked against a second Greek witness. Canon 11 is probably a later addition (absent from the Greek Nomocanon per Vossius); translated in full and disclosed in era_note.
- **Stale text left in Canon 1 rows (not edited, existing rows kept as they were):** the source row `notes` say "Canons II–XI remain" and the English row `translator_notes` say "Tip covers Canon I only." Both are now out of date; remove on the next Canon 1 touch. `reviews/audit/epistula_canonica_tip.packet.json` still names the old Canon I tip scope.
- **Not done:** DOCX rebuild, Logos build, site ship. No commit.

## 2026-10-23 (Claude, Mini) — stale scope wording fixed

- Canon 1 source note ('Canons II–XI remain') and English translator note ('Tip covers Canon I only') now say Canons II–XI follow in sections 2–11. Meta 'scope: Canons 1–11' removed: the whole letter is present, and the site showed any scope as 'Part only'. intro.md, research.json (SCOPE) and work_brief.json (argument + outline 2-11) now describe the whole letter. Checks: --tip-ready ok, work_lint 0 (legacy epistula_1.json / epistula_can_1.json fail check_pass_ab, as before).
