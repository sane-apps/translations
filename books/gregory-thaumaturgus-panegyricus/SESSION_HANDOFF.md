# Gregory Thaumaturgus: Panegyricus — production ledger

Canonical path: `~/SaneApps/clients/translations/books/gregory-thaumaturgus-panegyricus/`

## Charter

- Title: Gregory Thaumaturgus: Panegyricus
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

## 2026-09-15 (ChiefOfStaff / Grok Bot — tip-ready + live ship)

- **tip-ready:** PASS for opening (silence / eight years without oratory / fear before Origen).
- **Source locked:** Vossius 1684 Latin column (PDF pp. ~72-74); Greek OCR damaged; Argumentum/scholia stripped; scaffold summary discarded.
- **Pass A≠B:** justification `reviews/justifications/paneg_1.json` OK.
- **DOCX:** `gregory-thaumaturgus-panegyricus.docx`; verify_docx OK; Headword TN; inline/editorial Bible Genesis 48:15; no footnotes.xml.
- **Live:** https://fathers.saneapps.com/works/gregory-thaumaturgus-panegyricus/ (200); `/1/` (200). Deploy `a1a8a899.fathers-site.pages.dev`. live_works=41.
- **Claim:** remains **prepped**.
- **Logos:** compile pending on Air.
- **Next densify:** greg-thaum-eccl-metaphrase (CLAIMS order); skip origen-numbers, cosmas, paulus-silentarius-*, photius.

## 2026-09-15 (CoS / Grok Bot — TN ops-leak cleanup)

- Stripped ops/process theater from `translator_notes` / `notes_covered` (Pass A≠B stamps, Tip densify / scaffold-discarded chatter). Kept scholarly notes (lemma/OCR/scope).
- Cleaned meta blurb/edition/method phrasing of densify/scaffold ops leak; fixed copy-paste panegyricus Title/H1/author hardcodes in `build_book.py` where present.
- Rebuilt DOCX; `pipeline.verify_docx` OK; spot-check: no Pass A / Tip densify / scaffold strings in english JSON or DOCX body.
- TNs: 4→3.
- **Logos gate: CLEAR for Air Personal Book backlog** after this strip (private study).
- **Site:** KEEP live tip (Pass B already ok). Section HTML does not embed Headword TNs; no re-ship this turn (About/meta on live may still show older densify wording until a later packet rebuild).

## 2026-10-23 (Claude, Mini) — whole address assembled

- **Scope now:** the whole Thanksgiving Address. Section 1 (Latin column, unchanged text) plus 26 new sections from the Greek column of the same print, in reading order: 2.1, 2.2, 3.1, 3.2, 4.1, 4.2, 5.1, 5.2, 5.3, 6.1, 6.2, 6.3, 7.1, 7.2, 8, 9-19. Section 19 ends the oration ('μόνον ἡμᾶς παραμυθήσεται'). Every staged chunk had review verdict 'pass' (clause-by-clause, same model family as the drafter).
- **Edition corrected:** the PDF's title page (PDF p. 7) reads Paris, Sonnius / Morel / Cramoisy, 1622, not 'Vossius 1684' (same file, same sha256 as the Ecclesiastes book's PDF). Meta, book.yml and the new rows say 1622; row 1's own old notes still say 'Vossius 1684'.
- **Source fixes applied at assembly** (each re-read on the page crops): 5.1 παρῆς -> πατρὸς; 5.3 τὸ πρὸς εὔλογον -> τὸ πρὸς τὴν ἀδελφὴν εὔλογον, ὁ διαπομπὸς -> ὁ διὰ παντὸς τοῦ βίου, τῆς οἰκονομίας παραδοὺς -> τὴν οἰκονομίαν παραδιδοὺς; 6.2 διαφερόντως -> δυσχερῶς; 6.3 βλέψον τῇ ἀνάγκῃ -> βλέψαν ταῖς ἀνάγκαις. The English already followed the print in each place; translator notes that described the old misreadings were reworded.
- **Other assembly changes (no meaning change):** American spelling (honor, labor, favor, Savior, traveler, marveled, practiced, offense, capitalized); Pass A Greek lemma tags moved into lemmas[] (chunk 0 tagged 'Greek (English)', so the English was kept in place). Row 1's note 'remainder of the oration remains' now says the address continues in 2.1.
- **Meta/book.yml/intro/research/work_brief:** title 'Thanksgiving Address to Origen'; no scope (whole work); blurb and description say 'fresh English translation'; text_history names the 1622 print, the Latin/Greek split and the Koetschau reading used in 6.3.
- **Checks:** check_pass_ab on the 26 new justifications ok (2 legacy files, paneg_1.json and panegyric_1.json, fail as before); --tip-ready ok; work_lint 0 findings; site loader reads 27 sections, no scope.
- **Open doubts:** divine pronouns are mixed (He/Him in 12 and 15, he/him elsewhere, e.g. 4.1 and 19); 5.3 damaged line-end clause passed with a note; 12 προσήγορον vs προήγορον; 15 planting syntax; 16 'our true father' (Origen or God?) and 'eat earth' cited as Genesis 3:17 with the Genesis 3:14 wording noted; 6.3 follows Koetschau's βλάψαν against the print's βλέψαν; other source parts not rechecked for abbreviation misreadings. DOCX, site and Logos not rebuilt; reviews/work_receipt.json not touched. Scripts and backups: /private/tmp/claude-501/-Users-stephansmac/81d4c24b-3d4b-41ac-b671-6f83478cbdfc/scratchpad/xl/gtpan_assemble/.
