# Gregory Thaumaturgus: Ad Tatianum de anima — production ledger

Canonical path: `~/SaneApps/clients/translations/books/gregory-thaumaturgus-ad-tatianum-de-anima/`

## Charter

- Title: Gregory Thaumaturgus: Ad Tatianum de anima
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

- **tip-ready:** PASS for preface + inquiry program.
- **Source locked:** Vossius 1684 Latin column; Greek OCR damaged; scaffold paraphrase discarded.
- **DOCX:** rebuilt; verify_docx OK (editorial Genesis 1:27 contrast in front matter only; Gregory voice has no Bible quotes by commission).
- **Claim:** remains **prepped**.
- **Logos:** compile pending on Air.
- **Next:** live ship after visual review.


## 2026-09-15 (ChiefOfStaff / Grok Bot — live ship)

- **Live:** https://fathers.saneapps.com/works/gregory-thaumaturgus-ad-tatianum-de-anima/ (200); `/1/` (200). live_works=38.
- **Claim:** remains **prepped**.
- **Logos Personal Book:** compile pending on Air. DOCX at `gregory-thaumaturgus-ad-tatianum-de-anima.docx`.
- **Next densify:** greg-thaum-annuntiationem (CLAIMS order).

## 2026-09-15 (CoS hard fix — Genesis strip)

- **Genesis 1:27 removed** from FRONT_MATTER / build config; rebuild receipt now has **0 bible_links** (was 1 with `editorial: false` wrongly).
- DOCX rebuilt; Genesis absent from document.xml; Gregory voice still has **0** inline Bible (commission forbids Scripture testimonies).
- `verify_docx` **FAIL closed** on “no Bible datatype links” — expected honest-0-Bible exemption (Baron pattern). Do **not** reintroduce Genesis padding to green the gate.
- **Logos gate:** hold pending Air compile; honest 0-Bible tip — same exemption class as Baron Exodus padding removal.
- **Site tip:** KEEP (Pass B Latin still OK; this fix is DOCX/front-matter only).
- tip-ready: ok.

## 2026-10-23 (Claude, Mini — rest of the treatise translated; Cloudflare AI off, no outside model)

- **Translated:** sections 2-8, edition chapters I-VII, the whole rest of the treatise. 2 "How the soul can be known: by what it does"; 3 "That the soul exists: it moves the body and gives it life"; 4 "That the soul is a substance"; 5 "That the soul is not a body"; 6 "That the soul is simple"; 7 "That the soul is immortal"; 8 "That the soul is rational". Section 8 ends the treatise (printed p. 48 begins the Panegyric on Origen). The work is now complete: preface plus seven chapters.
- **Pages read:** `sources/gregory_thaumaturgus_opera_omnia.pdf` (Vossius 1684, archive bub_gb_DY2xvRwPetMC), Latin column, printed pp. 43-47 (PDF pages 67-71), from the page images. The DjVu OCR was badly damaged in places (worst in chapter VI); every OCR correction and every doubtful print reading is recorded in the source row `notes`. Edition asterisks dropped from the Latin; their blurred margin variants are noted and not adopted.
- **Files:** rows 2-8 appended to `translations/anima_tatianum_source.json` and `translations/anima_tatianum_english.json` (row 1 unchanged); new `reviews/justifications/2.json`-`8.json` (Pass A, lemmas, choices, bible_refs, review notes, source hash). Meta: edition and blurb now name the whole treatise, `first_english_note` and `text_history.method` updated, status stays `available`, no `scope` (work complete). `book.yml` description now says the volume covers the whole treatise; "New English rendering" changed to "Fresh English translation"; edition line updated.
- **Reviewer verdicts:** fresh-context clause-by-clause review against the Latin: **pass** for all seven sections. Fixes (restored connectives porro/nam/ergo/Ex quibus quidem, removed added 'their', 'only' and 'the very', 'not the whole body is animate', a statement no longer turned into a question in section 8) are in each justification's `review.changes`.
- **Scripture:** none quoted or clearly alluded to in sections 2-8, so `bible_refs` stay empty and no inline citations; the treatise by Tatian's request avoids Scripture testimonies. Philosophical sources (Aristotle, Categories 5; Plato, Phaedrus 245c-e and Republic 10) are named in translator notes only.
- **Checks:** `pipeline.check_pass_ab` on reviews/justifications/: ok=9 fail=0. `--tip-ready` english/source pair: ok. `pipeline.work_lint --slug`: 0 findings. `pipeline.verify_translation_qa` packet for sections 2-8: structural OK.
- **Open doubts for the owner:**
  - Section 8 'At quia nec in hisce volumus inhaerere': 'volumus' is clear on the page image (PDF p. 70) and is rendered as printed ("we do not wish to stop at the senses"); 'valemus' ("we are not able to rest in them") would read more easily.
  - Section 5 'e propria Animae ratione deiecta' ("fallen from what properly makes it a soul") and 'tripliciter dividi potest' ("can be divided in three ways"): sense uncertain; the English follows the Latin closely and adds nothing.
  - Section 5 'ratione et verbo nutritur' may echo Matthew 4:4 / Deuteronomy 8:3; left uncited as uncertain.
  - Section 7 'tam diu ... quod' (print 'quod' where 'quoad' is expected) rendered "as long as".
- **Still to do (not done here):** row 1 keeps its stale note "Tip scope: preface + program only; Capita I-VII remain" and an `added_allusions` Genesis 2:7 "possible" entry (left unchanged by instruction). `work_brief.json` outline, `research.json` and the `build_book.py` front-matter scope line still describe only the preface. DOCX not rebuilt; site not rebuilt or deployed; Logos not recompiled. No commit.

## 2026-10-23 (Claude, Mini) — stale scope wording fixed

- Row 1 notes_covered 'Tip scope: preface + program only; Capita I-VII remain' now says Capita I-VII follow in sections 2-8. intro.md and work_brief.json (argument + outline 2-8) now describe the whole treatise. Still stale, not touched: build_book.py front-matter scope line ('Tip densify preface + inquiry program'). Checks: check_pass_ab ok=9, --tip-ready ok, work_lint 0.
