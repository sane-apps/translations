# Gregory Thaumaturgus: De fide XII — production ledger

Canonical path: `~/SaneApps/clients/translations/books/gregory-thaumaturgus-de-fide-xii/`

## Charter

- Title: Gregory Thaumaturgus: De fide XII
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

## 2026-09-15 (ChiefOfStaff / Grok Bot — tip-ready + ship path)

- **tip-ready:** PASS for Capita I–II.
- **Source locked:** Vossius 1684 Latin column (Greek column OCR damaged; disclosed). Scholia stripped.
- **Pass B densified:** new English, not ANF Crombie; Pass A≠B; John 20 / Phil 2 inline.
- **DOCX:** `gregory-thaumaturgus-de-fide-xii.docx`; verify_docx OK; no footnotes.xml; Headword TN; no logosres:.
- **Claim:** remains **prepped** (ai_promote Jeremiah-only).
- **Logos Personal Book:** compile pending on Air.
- **Next:** live ship after visual review of dry-run artifact.


## 2026-09-15 (ChiefOfStaff / Grok Bot — live ship)

- **Live:** https://fathers.saneapps.com/works/gregory-thaumaturgus-de-fide-xii/ (200); `/1/` and `/2/` (200). Deploy `faac724c.fathers-site.pages.dev`. live_works=37.
- **Visual review:** artifact `07c93cb76e5cdbd10dce629107311ddb948d0787745286644f47fbfabb39ae29` passed image-inspection (32 shots).
- **Claim:** remains **prepped**.
- **Logos Personal Book:** compile pending on Air. DOCX at `gregory-thaumaturgus-de-fide-xii.docx`.
- **Next densify:** greg-thaum-ad-tatianum (CLAIMS order).

## 2026-09-15 (CoS / Grok Bot — TN ops-leak cleanup)

- Stripped ops/process theater from `translator_notes` / `notes_covered` (Pass A≠B stamps, Tip densify / scaffold-discarded chatter). Kept scholarly notes (lemma/OCR/scope).
- Cleaned meta blurb/edition/method phrasing of densify/scaffold ops leak; fixed copy-paste panegyricus Title/H1/author hardcodes in `build_book.py` where present.
- Rebuilt DOCX; `pipeline.verify_docx` OK; spot-check: no Pass A / Tip densify / scaffold strings in english JSON or DOCX body.
- TNs: 6→4.
- **Logos gate: CLEAR for Air Personal Book backlog** after this strip (private study).
- **Site:** KEEP live tip (Pass B already ok). Section HTML does not embed Headword TNs; no re-ship this turn (About/meta on live may still show older densify wording until a later packet rebuild).

## 2026-10-23 (Claude, Mini — Chapters III-XII translated; Cloudflare AI off, no outside model)

- **Translated:** sections 3-12, edition Capita III-XII, the whole rest of the work. 3 "Christ is not a man taken up like one of the prophets"; 4 "Christ was born of the Holy Spirit and the Virgin, not of a man's seed"; 5 "The Son before the ages and the Son of the last times are one"; 6 "The Word who cannot suffer suffered in his own flesh"; 7 "Christ is the Savior, not one who was saved"; 8 "Christ is not divided into a perfect man and God the Word"; 9 "Christ is not changeable or alterable"; 10 "Christ took the whole of our humanity, not a part"; 11 "Christ's body was not without soul or mind"; 12 "Christ came truly in the flesh, not in appearance only". Section 12 holds Interpretatio XII with the closing doxology and exhortation (the edition prints no separate closing heading) and ends the work at 'nomen meum in gentibus'; the following 'In vetere quadam Graeca collectione' is a separate piece and is not included. The work is now complete: Capita I-XII.
- **Pages read:** `sources/gregory_thaumaturgus_opera_omnia.pdf` (Vossius 1684, archive bub_gb_DY2xvRwPetMC), Latin column, printed pp. 3-8 (PDF pp. 27-32), from the page images; the facing Greek column was checked on the images at doubtful places. `gregory_page_129-200` images and `duodecim_fide_djvu_clean.txt` hold Vossius's later Notae, not this text. Corrections (Deus dittography in 12, expanded abbreviations) and every marginal variant are in each source row's `notes`.
- **Files:** rows 3-12 appended to `translations/fide_xii_source.json` and `translations/fide_xii_english.json` in reading order (rows 1-2 unchanged); English rows mapped to the book's shape (notes_covered, added_allusions, translator_notes list, source_ref, orientation, confidence). New `reviews/justifications/3.json`-`12.json` (Pass A, lemmas, choices, bible_refs, translator notes, review object, source hash). Meta: edition, blurb, `first_english_note`, `text_history.method` and copy-text coverage now name all twelve chapters; status stays `available`; no `scope` (work complete). `book.yml`: description scope sentence, edition line, and "New English translation" -> "Fresh English translation" in description and copyright.
- **Reviewer verdicts:** fresh-context clause-by-clause review against the Latin: **pass** for all ten sections. Changes made in review are listed in each justification's `review.changes` (3: "like one of the prophets", dropped added "appointed", "it is said"; 8: John 7:19 added beside John 8:40, dropped added "you", single subject Deus Verbum; 10: "except for sin"; 12: five wording fixes, question mark restored). Pre-review copy kept at the scratchpad `rev0/en.chunk0.before.json` (temporary).
- **Scripture:** inline citations in every section where quoted or clearly alluded to; Vulgate/LXX Psalm 15:10 given as English Psalm 16:10 (section 9, noted). Uncertain echoes (John 3:13; Ephesians 5:2 / Galatians 2:20 / Titus 2:14; Isaiah 53:5; 1 Corinthians 15:20; 1 Thessalonians 1:3; John 6:63; 1 Timothy 3:16; 1 Timothy 6:1) stay uncited in translator notes.
- **Checks:** `pipeline.check_pass_ab` on reviews/justifications/: ok=14 fail=0. `--tip-ready` english/source pair: ok. `pipeline.work_lint --slug`: 0 findings. `pipeline.verify_translation_qa` packet (all 12 sections expected, sample 10): structural OK.
- **Open doubts for the owner:**
  - Section 9: the print has 'immutabilem spiritu, * corruptibilem carne' with margin 'al. incorruptibilem' (page image PDF p. 29 checked); the facing Greek prints phtharton with margin al. aphtharton. The printed reading ("corruptible in flesh") is translated and the variant disclosed; the variant fits the Acts 2:31 quotation that follows. Owner may choose between them.
  - Section 12 margins on pp. 6-8 were read only at scan resolution; one gloss at 'circunferentes' is unreadable; at 'nomen meum' the margin has al. nomen Dei (partly obscured). Text kept in each case.
  - Section 3 margin variant at 'cursum temporum complevit' (et numeratione temporum suscept…) has a blurred last word; text kept.
- **Still to do (not done here):** row 1 `notes_covered` keeps the stale line "Tip scope: Capita I-II only; remaining ten anathemas later", and row 2 `orientation` still says Gregory "is closing his treatise with a final anathema" (both left unchanged by instruction; both now wrong). `research.json` still claims "SCOPE: Chapters 1–2." The `book.yml` attribution sentence ("some ascribe the work to the circle of Apollinaris") sits oddly beside Chapter XI, which condemns the Apollinarian soulless/mindless Christ; worth a source check. `reviews/work_receipt.json` lists only sections 1-2. DOCX not rebuilt; site not rebuilt or deployed; Logos not recompiled. No commit.

## 2026-10-23 (Claude, Mini) — stale scope wording fixed

- Row 1 notes_covered 'Tip scope: Capita I-II only; remaining ten anathemas later' now says Capita III-XII follow in sections 3-12; row 2 orientation now says Gregory continues with a second anathema (it said 'closing his treatise'). intro.md, research.json (SCOPE) and work_brief.json (argument + outline 3-12) now describe all twelve chapters. Checks: check_pass_ab ok=14, --tip-ready ok, work_lint 0.
