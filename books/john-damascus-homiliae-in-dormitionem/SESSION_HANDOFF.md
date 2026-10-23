# Three Homilies on the Dormition of the Mother of God — production ledger

Canonical path: `~/SaneApps/clients/translations/books/john-damascus-homiliae-in-dormitionem/`

## Charter

- Title: Three Homilies on the Dormition of the Mother of God
- Author: John of Damascus (d. 749)
- Scope: the three Dormition homilies as printed in Migne, PG 96, cols. 699-762.
  The Euthymius-history passage of Homily II (cols. 747-750: Juvenal of Jerusalem
  and the empty tomb) was locked and translated first (2026-10-20, Spark) because
  the Timeline dossier mary-s-life-end-death (question 67) quotes it.
- Source: Migne, Patrologia Graeca 96 (Paris, 1860) — public domain; the Google
  scan is openly posted on archive.org (item pg-96). An earlier Timeline pass
  recorded "no PG 96 text is openly posted"; that was wrong — the volume stands
  open in archive.org's Patrologia Graeca set. Kotter's critical edition
  (Patristische Texte und Studien 29) and Daley's English (1998) are in copyright
  and were not used.
- Legal: private study; new English from allowed sources; no modern copyrighted English copy.

## State

- Sources: PG 96 PDF + OCR locked under sources/ (sha256 in sources/manifest.json), 2026-10-20.
  The scan's Greek OCR is poor; it is a finding aid only.
- Translations: Homily II's Juvenal passage (section "2", cols. 747-750) transcribed
  from the page images (PDF leaves 415-416) and translated, 2026-10-20.
  The rest of the three homilies: not started.
- DOCX: not built
- Logos Build: not compiled
- Bible-link verify: not done

## Next

Production lane: transcribe and translate the remainder of the three homilies from
the locked PG 96 scan, working from the page images, in question-priority order.

## 2026-10-23 (Claude, Mini — rest of all three homilies translated; Cloudflare AI off, no outside model)

- **Translated:** everything except the Juvenal passage, so the whole declared work (PG 96 cols. 699-762) now has English. 41 new sections: Homily I, 1.1-1.17 (heading and paragraphs α'-ιδ', to the Amen); Homily II, 2.1-2.17 and 2.18-2.19 (PG sections 1-17, the second half of 18, and 19); Homily III, 3.1-3.5 (sections α'-ε', to the Amen; John's encomium on Chrysostom, which follows in the column, is not part of this work).
- **Reading order:** 1.1 ... 1.17, 2.1 ... 2.17, then existing row `2` (unchanged: the first half of PG section 18, the Euthymian History quotation), then 2.18 (the rest of section 18: Dionysius at the tomb, the grave-cloths sent to Blachernae), 2.19, then 3.1 ... 3.5. Row `2` keeps its id, Greek, English and title.
- **Pages read:** `sources/pg-96.pdf`, Greek columns, from the page images (220 dpi; doubtful words at 400 or 600 dpi), PDF leaves 391-422 = cols. 700-761. The facing Latin was used to check doubtful readings. The OCR served only to find pages. Each justification's `edition.locus` names its columns and leaves, and `source_notes` holds the full transcription note (apparatus, margin Scripture, doubtful readings).
- **Files:** 41 rows added to `translations/dormition_homilies_source.json` ({greek, section, title}) and `translations/dormition_homilies_english.json` ({english, section, title}), matching row `2`'s shape. New `reviews/justifications/<section>.json` for each new section: Pass A, lemmas, choices, variants (printed text vs English), bible_refs, notes, source_notes, review, source hash. Titles: every Homily II title now starts "Homily II —", like Homilies I and III and row `2`. Inside the work, "Song of Solomon" is now "Song of Songs" (28 places). No `*_meta.json` exists for this book, and none was made: with no meta the site shows the work as available, and the whole work is now translated. `book.yml` has no description, so it was not changed.
- **Reviewer verdicts:** a fresh-context, clause-by-clause review against the Greek: **pass** on all 41 sections (`review.coverage` "every clause checked"; the fixes are in `review.changes`). Changes made during assembly, no sense changed: Pass A had inline Greek trimmed until the English-gloss gate passes (the lemmas are kept in `lemmas[]`; see `pass_a_note`); in 2.7 and 2.17, hyphenated word-for-word compounds in Pass A were written out in plain words. The 2.17 source note's misread footnote ("fn57 R. φορᾶς") was corrected in `source_notes` to what the page prints ("R. φθορᾶς").
- **Checks:** `pipeline.check_pass_ab` on reviews/justifications/: ok=41 fail=0. `--tip-ready` english/source pair: ok. `pipeline.work_lint --slug`: 0 findings. `pipeline.verify_translation_qa` packet over all 42 sections: structural OK (packet in scratch, not committed).
- **Places where the English departs from the printed Greek (all in `variants[]` and the notes):** 2.1 διαιρέσεως read as προαιρέσεως ('a good will'; Latin 'probaque voluntate'); 2.2 ἐνδέδυμαι as 'put off' and ὑπερέρχεται as 'undergoes' (facing Latin col. 726 'exui', 'subit'); 2.3 εὔτρεπτος, ὑπεχείτω; 2.4 θέσματα rendered 'wills' (print clear at 600 dpi; Latin 'voluntates'; the owner may want to confirm this one); 2.10 'our hands' read as 'my hands'; 2.13 Ἀμελητί read as 'at once'; 2.14 ἐλαίου read as 'mercy' (editor's note 52), γεύμασιν read as 'streams'; 3.2 κλίματι read as 'ladder', καρποὺς προθέσεως as 'bread of the presence', Ἐδείξατο as 'received' (Latin 'Recepit'; print confirmed on leaf 419).
- **Open doubts (noted, not blockers):** 1.6 and 1.12, whether the verb is 'they' or 'I' (kept 'they'; the Latin has Videbant at 1.12); 1.11/1.12, where the hymn introduced by λέγοντες ends (no quotation marks used); 1.11, the 'cornerstone' is cited as Ephesians 2:20 (1 Peter 2:6 and Isaiah 28:16 are other possible sources); 2.4, 'the name of the spirit' follows the print, though the Latin has 'lex'; 2.6, the last sentence is obscure (the editor says so, and the Latin translates a different text); 2.8, the 'who, unless it be the Word' riddle is left obscure; 2.17, the tomb's speech begins at Τί ζητεῖτε; 3.1, φθορᾷ κτησάμενος τὸ ἄφθαρτον is rendered against Migne's Latin; 3.3, τὴν δεδωρημένην ... ζωήν has two possible readings; 3.4, her own 'spirit' is lowercase though Migne capitalises it. LXX Psalm numbers are converted to English numbering inline and noted in the translator notes, which follows the house style.
- **Still to do (not done here):** the site blurb in `websites/fathers.saneapps.com/data/work-blurbs.json` still says this book holds one passage; it should now describe all three homilies. Row `2`'s title still ends "(the Euthymius History, cols. 747-750)", which is an edition locus and not a thought. The site reader shows no translator notes for this book: the english rows keep row `2`'s three fields, so the notes and emendations live only in the justifications. If readers should see the departures from the print, they need `translator_notes` on the english rows or a `text_history` in a meta file. `book.yml` still says `language: Greek` and has no description. The `build_book.py` stub is not written, so no DOCX exists; the site has not been rebuilt; Logos has not been compiled. No commit.

## 2026-10-23 (Claude, Mini) — meta added

- New translations/dormition_homilies_meta.json: title 'Three Homilies on the Dormition of the Mother of God', author John of Damascus (john-of-damascus), status available, scope '' (all three homilies), edition PG 96 cols. 699-762, topics as data/work-topics.json, text_history naming the PG 96 scan and the seven places where the English follows the sense / facing Latin over the printed Greek. first_english is false (Daley 1998 exists); without a meta the site defaulted to true.
- book.yml: description and copyright added with 'Fresh English translation'. language: Greek left as it was.
- Site loader check: author, author slug, era (Byzantine) and sort year (749) unchanged; edition and witnesses now come from the meta. The site's data/work-blurbs.json entry ('One passage ...') overrides the meta blurb and still needs updating in the site repo.
