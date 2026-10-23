# Gregory Thaumaturgus: Sermo in omnes sanctos — production ledger

Canonical path: `~/SaneApps/clients/translations/books/gregory-thaumaturgus-sermo-in-omnes-sanctos/`

## Charter

- Title: Gregory Thaumaturgus: Sermo in omnes sanctos
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

- **tip-ready:** PASS for opening (blessing through Hades despoiled / sting of death).
- **Source locked:** MGR Greek extract (TLG 2063.010 / Documenta Catholica Omnia); PG 10.1200–1201 cues.
- **Pass A≠B:** justification `reviews/justifications/omnes_1.json` OK.
- **DOCX:** `gregory-thaumaturgus-sermo-in-omnes-sanctos.docx`; verify_docx OK; Headword TN; inline Bible (1 Cor 15:55); no footnotes.xml.
- **Live:** https://fathers.saneapps.com/works/gregory-thaumaturgus-sermo-in-omnes-sanctos/ (200); `/1/` (200). Deploy `6dba211d.fathers-site.pages.dev`. live_works=40.
- **Claim:** remains **prepped**.
- **Logos:** compile pending on Air.
- **Next densify:** greg-thaum-panegyricus — current english is scaffold summary; needs real Latin lock Pass A≠B before ship.

## 2026-09-15 (CoS / Grok Bot — TN ops-leak cleanup)

- Stripped ops/process theater from `translator_notes` / `notes_covered` (Pass A≠B stamps, Tip densify / scaffold-discarded chatter). Kept scholarly notes (lemma/OCR/scope).
- Cleaned meta blurb/edition/method phrasing of densify/scaffold ops leak; fixed copy-paste panegyricus Title/H1/author hardcodes in `build_book.py` where present.
- Rebuilt DOCX; `pipeline.verify_docx` OK; spot-check: no Pass A / Tip densify / scaffold strings in english JSON or DOCX body.
- TNs: 5→4.
- **Logos gate: CLEAR for Air Personal Book backlog** after this strip (private study).
- **Site:** KEEP live tip (Pass B already ok). Section HTML does not embed Headword TNs; no re-ship this turn (About/meta on live may still show older densify wording until a later packet rebuild).

## 2026-10-23 (Claude, Mini — rest of the sermon translated; Cloudflare AI off, no outside model)

- **Translated:** sections 2 and 3, the whole rest of the sermon. Section 2 "The devil caught on his own hook, and heaven opened" (Goliath, the devil hooked on the Godhead, Adam and Jonah brought up, Jacob's ladder, the Angel of Great Counsel). Section 3 "The devil's short laughter and endless grief" (the arrow forged in the Virgin, the fallen archangel, closing doxology). The work is now complete: sections 1-3 cover PDF lines [00001]-[00058]; PDF pages 3-8 are the print's concordance, not text.
- **Pages read:** `sources/sermo_omnes_sanctos_MGR.pdf` (MGR / Documenta Catholica Omnia, TLG 2063.010) page 1 lines [00026]-[00028] (PG 10.1201) and page 2 lines [00029]-[00058] (PG 10.1201-1204). Text file checked line by line against the rendered page images. Print typos normalised in section 2: [00026] οὔτω read οὕτω; [00037] τὸν ἅνθρωπον read τὸν ἄνθρωπον. The print's own editorial brackets [κόσμου] and [τοῦ] ... [Θεοῦ] kept in the source.
- **Files:** rows 2-3 appended to `translations/omnes_sanctos_source.json` and `translations/omnes_sanctos_english.json` (row 1 unchanged); new `reviews/justifications/2.json` and `3.json` (Pass A, lemmas, choices, bible_refs, review notes, source hash). Meta: title drops "(tip opening)", blurb/edition/era_note/first_english_note/text_history updated for the whole sermon, status stays `available`, no `scope` (work complete). `book.yml` description now says the volume holds the whole sermon; "New English translation" changed to "Fresh English translation" in description and copyright.
- **Reviewer verdicts:** fresh-context clause-by-clause review of both rows against the Greek: **pass** for section 2 and section 3. Review fixes (agency of εὑρίσκει, restored γάρ twice, Jonah clause made active, removed an added "on it", ἀλάστωρ as "the accursed one", object-first order removed) are recorded in each justification's `review.changes`.
- **Scripture inline:** 1 Samuel 17:51; 1 Corinthians 15:45-47; Jonah 1:17-2:10 (Greek/Hebrew 2:1-11); Genesis 28:12; Isaiah 9:6 (LXX 9:5); Psalm 95:4 (LXX 94:4, renumbered); Genesis 3:14.
- **Checks:** `pipeline.check_pass_ab` on 1.json, 2.json, 3.json: ok=3. `--tip-ready` english/source pair: ok. `pipeline.work_lint --slug`: 0 findings. `pipeline.verify_translation_qa` packet for sections 2-3: structural OK. Legacy `omnes_1.json` still fails check_pass_ab (hyphen gloss); it predates this work and was left alone.
- **Open doubts for the owner:**
  - σκιρτῶσιν τὴν τοῦ δράκοντος κεφαλήν: page image confirms the print; rendered "leap upon the dragon's head".
  - The print's bracketed [τοῦ] ... [Θεοῦ] is followed ("the God of all"); without it the clause reads "never separated from all things". Recorded in translator_notes.
  - φυλακὴ τῶν χοίρων rendered "the pen of the swine"; "prison" is the more usual sense and may be preferred. The swine allusion (Matthew 8:30-32; Mark 5:11-13) stays uncited as uncertain.
  - Possible echo of Ephesians 4:9-10 in "came down once and went up once ... fills all things" stays uncited as uncertain.
- **Still to do (not done here):** row 1's translator note "Tip scope only; remainder of the sermon remains." is now false but row 1 was left unchanged by instruction; `intro.md`, `work_brief.json` and `research.json` describe only the opening. DOCX not rebuilt; site not rebuilt or deployed; Logos not recompiled. No commit.

## 2026-10-23 (Claude, Mini) — stale scope wording fixed

- Row 1 translator note 'Tip scope only; remainder of the sermon remains' now says the sermon continues in sections 2-3; source_ref 'tip opening' -> 'opening'. intro.md, research.json (SCOPE) and work_brief.json (argument + outline 2-3) now describe the whole sermon. Checks: --tip-ready ok, work_lint 0 (legacy omnes_1.json still fails check_pass_ab, as before).
