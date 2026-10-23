# Gregory Thaumaturgus: In annuntiationem — production ledger

Canonical path: `~/SaneApps/clients/translations/books/gregory-thaumaturgus-in-annuntiationem/`

## Charter

- Title: Gregory Thaumaturgus: In annuntiationem
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

- **tip-ready:** PASS for Sermo I opening (mystery unveiled through Gabriel reply / Filius Dei).
- **Source locked:** Vossius 1684 Latin column; Greek OCR damaged; Vossius scholia stripped; scaffold paraphrase discarded.
- **Pass A≠B:** justification `reviews/justifications/annunc_1.json` OK.
- **DOCX:** `gregory-thaumaturgus-in-annuntiationem.docx`; verify_docx OK; Headword TN; no footnotes.xml; inline Bible; no logosres:.
- **Live:** https://fathers.saneapps.com/works/gregory-thaumaturgus-in-annuntiationem/ (200); `/1/` (200). Deploy `a6ca72bd.fathers-site.pages.dev`. live_works=39.
- **Claim:** remains **prepped**.
- **Logos Personal Book:** compile pending on Air.
- **Next densify:** greg-thaum-sermo-omnes (CLAIMS order).

## 2026-09-15 (CoS / Grok Bot — TN ops-leak cleanup)

- Stripped ops/process theater from `translator_notes` / `notes_covered` (Pass A≠B stamps, Tip densify / scaffold-discarded chatter). Kept scholarly notes (lemma/OCR/scope).
- Cleaned meta blurb/edition/method phrasing of densify/scaffold ops leak; fixed copy-paste panegyricus Title/H1/author hardcodes in `build_book.py` where present.
- Rebuilt DOCX; `pipeline.verify_docx` OK; spot-check: no Pass A / Tip densify / scaffold strings in english JSON or DOCX body.
- TNs: 5→4.
- **Logos gate: CLEAR for Air Personal Book backlog** after this strip (private study).
- **Site:** KEEP live tip (Pass B already ok). Section HTML does not embed Headword TNs; no re-ship this turn (About/meta on live may still show older densify wording until a later packet rebuild).

## 2026-10-23 (Claude, Mini — rest of Sermo I translated; Cloudflare AI off, no outside model)

- **Translated:** the whole rest of the first sermon (Homily I), 19 new sections, from the true opening to the closing doxology. Section 0 "Today the angels sing and Adam is renewed" is the sermon's real opening and comes before existing section 1, which begins mid-sentence at 'Mysteriumque'. Sections 2-19 follow section 1: Mary's wisdom undoes Eve's fall; the Virgin's questions; Gabriel's answer (grace above nature); mysteries hidden from prophets and angels; the Son as the ever-living fountain of light; "Hail, full of grace" and "The Lord is with you"; the Hail litany (fountain, flower, meadow, vine, field); the pearl image and the two-natures formula; the ark (Psalm 132:8); "Hear, O daughter" (Psalm 45:10-11); the rod from Jesse; Luke 2:4-7; the swaddled Creator in the manger; no room for Him; Father's bosom and mother's arms; doxology. Homilies II and III are not translated.
- **Pages read:** `sources/gregory_thaumaturgus_opera_omnia.pdf` (Vossius 1684, archive bub_gb_DY2xvRwPetMC), Latin column, printed pp. 9-15 (PDF pp. 33-39), from the page images (crops p09b, p10a, p10b, p12a, p13a, p14b, p15a checked in review). Greek column not used: OCR damaged. Each source row's `notes` names its page and column, margin variants (none adopted), and readings: 'Fasciis cum' corrected to 'Fasciis eum' (s17); '[s]uper' and '[i]n quo' supplied from damaged letters on p. 15 (s19); 'servato' and 'patri per omnia similis' confirmed on p. 13.
- **Files:** rows 0 and 2-19 added to `translations/annunciation_source.json` and `translations/annunciation_english.json` in reading order (0, 1, 2 ... 19; row 1 unchanged). New `reviews/justifications/0.json` and `2.json`-`19.json` (Pass A, lemmas, choices, bible_refs, notes, review, source hash). Reader translator notes had workflow wording removed (s0 merge advice, "source row", "see source note"). Meta: status stays `available`, `scope` "Homily I", title "On the Annunciation (Homily I)", blurb/edition/first_english_note/text_history now name the first sermon. `book.yml`: description scope sentence names the whole First Discourse and says II-III are not yet translated; edition line updated; "New English translation" -> "Fresh English translation" (description and copyright).
- **Reviewer verdicts:** fresh-context, clause-by-clause review against the Latin: **pass** for all 19 sections; fixes are listed in each justification's `review.changes`. Assembly changes after review: s11 one long sentence split at "Mary:" ("He is perfect in Godhead ...") for the sentence-shape gate; s15 Pass A re-glossed in plain English (gate read it as a Latin note). No sense changed.
- **Scripture inline (English numbering; Vulgate Psalm numbers converted):** Malachi 4:2; Genesis 3:1-6; Luke 1:28, 1:30, 1:35, 1:37; Matthew 19:26; Hebrews 1:3; John 1:9; John 8:12; Psalm 46:4 (Vulg. 45); 1 Corinthians 7:34; Genesis 2:7; Genesis 2:21-22; Psalm 45:2 (Vulg. 44); Colossians 2:9; Hebrews 4:15; Matthew 13:17; Luke 10:24; Psalm 99:7 (Vulg. 98); Psalm 132:8 (Vulg. 131); Exodus 25:11; John 1:18; Isaiah 11:1; Psalm 45:10-11 (Vulg. 44); Luke 2:4-5; Colossians 1:15; Luke 2:6-7; Psalm 104:2 (Vulg. 103); Psalm 80:1 (Vulg. 79); Daniel 7:10; Luke 2:7; Genesis 1:1; 2 Corinthians 8:9; Luke 2:13-14.
- **Checks:** `pipeline.check_pass_ab` on reviews/justifications/: ok=20 fail=0. `--tip-ready` english/source pair: ok. `pipeline.verify_translation_qa` packet over sections 0-19: structural OK (packet in scratch, not committed). `pipeline.work_lint --slug`: **1 error** — boundary: section 0 ends without terminal punctuation (see first open item).
- **Open items for the parent (row 1 was left unchanged by instruction):**
  - Section 0 ends mid-sentence ("... the wonders that surpass mind and understanding,"); the sentence finishes in row 1 ("mysteriumque ... palam nobis facit"), whose English "He makes plain to us the mystery ..." gives the verb the wrong subject (the subject is divina gratia). Fix: move "Mysteriumque quod ab aeterno occultatum fuit, palam nobis facit." to the end of row 0's Latin, end row 0's English "... Today divine grace, the hope of things unseen, shines out, and makes plain to us the wonders that surpass mind and understanding and the mystery that was hidden from eternity.", and start row 1's English at "Today crowns of lasting virtue are woven." This also clears the work_lint boundary error.
  - Row 1 stops at "solam."; page p. 10 col. D reads "solam gratia elegit". Row 1's Latin needs "gratia elegit" and its last English sentence should read "Fittingly, then, grace chose holy Mary alone out of all generations." (the current "he marks out" supplies a wrong subject).
  - Row 1 differs from the print in other places seen on p. 10 (cols. A and C-D; row 1 was not fully re-read): after "virum non cognosco?" the print adds "nunquid amplius virgo permanebo? nunquid virginitatis dignitas in me prodetur et amittetur?" (missing from row 1's Latin and English); "Dominus Deus sedem David" (row 1: "Dominus sedem"); "sermonis summam profert" (row 1: "finem profert"); "Hodie sacra benevolorum" (row 1: "facta", a long-s misread; English omits "sacred"). Row 1 needs a full re-lock against pp. 9-10 and a fresh review.
  - s3 "Unde nobis donum materiam paravit?" is obscure; kept close to the letter ("From where has the gift made ready its substance for us?"); margin "al. promissum" not adopted. A Greek-column check would settle it if the Greek is ever read.
  - s10 "tempore motus" rendered "the child's stirring" is an interpretive reading; the sense of motus is uncertain.
- **Still to do (not done here):** `intro.md` and `research.json` still describe only the opening; site `data/publication-review.json` has a record for section 1 only; DOCX not rebuilt; site not rebuilt or deployed; Logos not recompiled. No commit.

## 2026-10-23 (Claude, Mini) — sentence boundary fix between sections 0 and 1

- Moved 'mysteriumque quod ab aeterno occultatum fuit, palam nobis facit.' (lowercase as printed, p. 10 col. A, checked on crop p10a) from the start of row 1 to the end of row 0. Row 0's English now ends '... shines out, and makes plain to us the wonders that surpass mind and understanding and the mystery that was hidden from eternity.' (subject: divine grace); row 1's English starts 'Today crowns of lasting virtue are woven.' Justifications 0.json and annunc_1.json updated to match; source notes reworded. intro.md and research.json now say the volume holds the whole First Discourse and that Homilies II and III are not translated; meta scope stays 'Homily I' (site shows 'Part only: Homily I').
- Checks: check_pass_ab ok=20, --tip-ready ok, work_lint 0 findings (the boundary error is gone).
- Still open (not done here): row 1 lacks 'gratia elegit' at its end ('he marks out' supplies a wrong subject); row 1 omits Mary's added questions after 'virum non cognosco?'; 'Dominus sedem' / 'finem' / 'facta' vs the print's 'Dominus Deus sedem' / 'summam' / 'sacra'. Row 1 needs a re-lock against printed pp. 9-10 and a fresh review.

## 2026-10-23 (Claude, Mini) — row 1 re-locked from the print and translated fresh; edition date corrected

- **Edition:** the PDF is the Paris 1622 Opera omnia (title page PDF p. 7: "Parisiis, sumptibus Michaelis Sonnii, Claudii Morelli et Sebastiani Cramoisy, MDCXXII"), not a 1684 Vossius edition. Meta `edition`, `text_history.method`, witness (id `paris1622`, name "Opera omnia, Greek and Latin (Paris: Sonnius, Morel and Cramoisy, 1622), page images") and `book.yml` edition line now say so. Same fix made in de-fide-xii and ad-tatianum-de-anima (meta + book.yml) and in panegyricus row 1 notes.
- **Row 1 Latin re-locked** from printed p. 10, cols. A-D (PDF p. 34, read at 330 dpi). It starts after row 0's "palam nobis facit." and ends "solam gratia elegit." (row 2 starts "Nam prudens revera"). Fixed against the old lock: "sacra" (was "facta"); "At Dominus"; "Hodie celebre atque ineffabile Christianorum, qui suam in Christum spem sponte obsignarunt, mysterium plane nobis adnunciatur" (old lock had "gaudium ... spem posuerunt, adnuntiatur", which the print does not have); "Dominus Deus sedem"; Mary's added questions "nunquid amplius virgo permanebo? nunquid virginitatis dignitas in me prodetur et amittetur?"; "summam" (was "finem"); "solam gratia elegit". Margin variants recorded in the row's notes, none adopted. Facing Greek checked on the page image at two places: the kingdom above is the subject of "vocat"; grace is the subject of "elegit".
- **English row 1 translated fresh** (Pass A + Pass B), then a second clause-by-clause pass against the Latin (changes listed in the justification's `review.changes`). Inline Scripture: Psalm 96:11-13, Matthew 3:8-10, John 16:22, Luke 1:19, 1:28 (twice), 1:29, 1:30-33, 1:34, 1:35. Last sentence now "Fittingly, then, grace chose holy Mary alone out of all generations."
- **Justification** `reviews/justifications/annunc_1.json` rewritten in the shape of 0.json/2.json (excerpt_id, edition, Pass A, lemmas, choices, bible_refs, notes, source_notes, source_sha256, review).
- **Checks:** `check_pass_ab` on annunc_1.json ok=1; on the whole folder ok=20 fail=0; `--tip-ready` pair ok; `work_lint` 0 findings (this book, de-fide-xii, ad-tatianum-de-anima, panegyricus).
- **Still stale (not touched here):** `sources/_annuntiationem_latin_lock.txt` (manifest `preferred_copy_text`) still holds the old row 1 text and "Vossius 1684"; row 2's source `notes` and 2.json `source_notes` still carry the "section 1 needs 'gratia elegit'" note; the English rows 0 and 2-19 still say "Vossius 1684" in `notes_covered`/`source_ref`; the site's `data/publication-review.json` record for section 1 predates this change; DOCX not rebuilt; no deploy; no commit.
