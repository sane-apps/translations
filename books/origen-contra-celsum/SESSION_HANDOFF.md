# Against Celsus — session handoff

## 2026-10-23 (assembled 2026-10-24): Book 1 translated whole from the Greek

Claude translated Book 1 from Koetschau's Greek (GCS 2–3, 1899, Perseus TEI), with Cloudflare AI off and no outside model. Each chapter got a fresh translation (Pass A gloss with lemmas, then Pass B reading English), then a separate clause-by-clause review against the Greek. Crombie (ANF 1872) and Chadwick (1953) were not used or consulted.

Counts: 71 chapters, 71 English rows, 71 source rows, 208 paragraphs, about 26,800 English words, 71 justifications (2,842 Greek lemma tags). All 71 review verdicts are pass.

Files:
- `translations/cels_b1_source.json` and `translations/cels_b1_english.json`: the whole book, one row per chapter.
- `reviews/justifications/cels_b1_01.json` to `cels_b1_71.json` (the old 01, 02 and 71 receipts were replaced; git has them).
- `translations/cels_b1_meta.json`: title "Against Celsus, Book I", new blurb, first_english false with the Crombie/Chadwick note, text_history names the copy-text.
- Old slices `cels_b1_01_02_*` and `cels_b1_02_71_*` moved with `git mv` to `translations/_superseded/` (the site loader reads only the top folder, so they no longer shadow the new rows).

Assembly changes, no change of meaning:
- 1.1 source: the staged row stopped at exactly 1,200 characters. The locked source is the whole chapter from the TEI; the English already covered it. All other 70 staged rows match the TEI exactly, apart from whitespace. The staging script that wrote `source_<book>.json` needs fixing before other books are assembled.
- Titles 1–32 put in sentence case to match 33–71; curly apostrophes throughout.
- 1.36: "the Third Book of Kingdoms" changed to "First Kings" (house lint: English book titles; same book). Note and review entry updated.
- 1.22, 1.41, 1.64: some Greek lemma tags moved from the Pass A text into `lemmas[]` (7, 8 and 17), so the gloss reads as English. No gloss words changed. No sentences were split.

Checks run: `pipeline.check_pass_ab` on all 71 justifications (ok=71 fail=0); `--tip-ready` on the pair (ok); `output_guard_errors` with full-stop check (clean); `work_lint` rules on the Book 1 rows (0 findings); site loader `load_origen_contra_celsum` shows 71 sections, status available.

Not run: `pipeline.verify_translation_qa` packet and the source/English hash receipt (SOP section 3). No `work_receipt.json` was written. Nothing committed.

Open doubts (none block; the owner may want to look):
- 1.1, 1.17 (κωλύεται, translated "prevents"), 1.49 (καταβαλών or καταλαβών), 1.60 (ἢ ποῦ γεννηθήσεται γινώσκοντες may be corrupt): not checked against Koetschau's apparatus.
- 1.23: the copy-text calls Eurynome "one of the Graces"; Hesiod suggests "mother". Translated as it stands; noted.
- 1.25: a compressed clause (τῷ ὀνόματι ἐφαρμοζόμενον) kept as "joined to this designation"; Psalm 146:6 is one of several places with "Creator of heaven and earth".
- 1.34: Origen says "aalma" occurs in Deuteronomy 22; the Hebrew text there has na'arah betulah. Given as written; noted.
- 1.43: the staged Greek says "no labourers" where Matthew 9:37 says "few"; possibly a dropped word. The seven Genesis citations are representative; the owner may prefer to drop them.
- 1.47: Origen's report that Josephus blamed the fall of Jerusalem on James's death is not in surviving Josephus; given as Origen reports it.
- Style calls: 1.19, 1.35, 1.36, 1.43 θεῖον/θειότερον πνεῦμα capitalised as God's Spirit; 1.46 "as the Word wills" (or "as reason wills"); 1.54 "We announced him" supplies "him"; 1.56 "bend your bow" supplies "your bow"; 1.57 "spirit of adoption" lower case, and where Celsus's words end is uncertain; 1.5 Zeno's ἱερὸν οὐδὲν can be parsed two ways, same sense.
- Left out of the reading text on purpose: Hebrews 3:3 at 1.18 (possible allusion only), Timaeus 22c–d at 1.19 (Origen does not name it).

Next: run the `verify_translation_qa` packet for Book 1; fix the staging script's 1,200-character cut and check the other books' staged rows for the same cut (Preface ch. 1 and Book 4 ch. 73 are also exactly 1,200 characters long; compare them with the TEI). Other lanes are assembling further books in this folder at the same time; their entries go below.

## 2026-10-23 (assembled 2026-10-24): Book 3 translated whole from the Greek

Claude translated Book 3 from Koetschau's Greek (GCS 2–3, 1899, Perseus TEI), with Cloudflare AI off and no outside model. Each chapter got a fresh translation (Pass A gloss with lemmas, then Pass B reading English), then a separate clause-by-clause review against the Greek. Crombie (ANF 1872) and Chadwick (1953) were not used or consulted.

Counts: 81 chapters, 81 English rows, 81 source rows, 212 paragraphs, about 25,300 English words (18,400 Greek words), 81 justifications, 140 Scripture references in `bible_refs`. Review verdicts: 80 pass, 1 needs-owner (3.37, below).

Files:
- `translations/cels_b3_source.json` and `translations/cels_b3_english.json`: the whole book, one row per chapter.
- `reviews/justifications/cels_b3_01.json` to `cels_b3_81.json` (the old 01 and 81 receipts were replaced; git has them).
- `translations/cels_b3_meta.json`: title "Against Celsus, Book III", new blurb, first_english false with the Crombie/Chadwick note, text_history names the copy-text. Old "closeout"/"sampled" wording removed.
- Old `cels_b3_english.json` and `cels_b3_source.json` (the 4-row summary) moved with `git mv` to `translations/_superseded/`. Book 3 had no other slice files.

Source check: all 81 staged rows match the TEI chapters letter for letter (Greek letters compared, punctuation and spacing ignored). Book 3 has no 1,200-character cut; 3.13 is 1,199 characters long and complete.

Assembly changes, no change of meaning:
- Titles put in sentence case to match Book 1 (57 titles; letter case only). Three wording touches: 3.4 "the promised one", 3.25 "a god" (pagan god, lower case), 3.68 "The power of the apostles’ words" (their preaching, not the Word).
- 20 justifications (3.9, 11, 15–18, 21, 23, 34, 39, 40, 44, 48, 51, 54–56, 59, 76, 78): 1 to 11 Greek lemma tags each moved from the Pass A text into `lemmas[]` so the gloss is under the 25% Greek share. No gloss words changed; each record says so in `pass_a_structural_fix`. The staged chunks keep the full tagged gloss. No sentences were split.

Checks run: `pipeline.check_pass_ab` on all 81 justifications (ok=81 fail=0); `--tip-ready` on the pair (ok); `output_guard_errors` with full-stop check (clean); `work_lint` rules on the Book 3 rows (0 findings); TEI comparison (0 mismatches); site loader `load_origen_contra_celsum` shows "Against Celsus, Book III", 81 sections, status available, first_english false.

Not run: `pipeline.verify_translation_qa` packet and the source/English hash receipt (SOP section 3). No `work_receipt.json` was written. Nothing committed.

Open doubts:
- **3.37 (needs owner, check before certifying):** the staged Greek and the TEI (line 6157) both read "οἱ δὲ τοιοῦτοι Χριστιανοὶ εἶναι ἐν ἀληθείᾳ, ἤτοι ἑαυτοὺς" before "ὥσπερ πολλοὶ". It cannot be construed and looks like a duplicated line, so the English leaves it out. Check the printed Koetschau page (GCS 2, p. 70).
- Text problems rendered by sense and noted: 3.17 crux (†ἐστὶ τὰ καὶ κατ᾿ αὐτὸν σεμνά); 3.23 lacuna kept as [ … ]; 3.27 main verb lost ("So we address our reply to him" supplied); 3.75 ἐπιστρεπτικὸν καὶ ψυχῶν μαθήματα (a word may be missing); 3.77 crux at τίνες οὖν † εἴποιμεν Ἕλληνες; 3.78 the last clause; 3.81 οὐδὲν οὐκ ἐπινοηθῆναι read as "nothing can be conceived as better".
- Not checked against Koetschau's apparatus: 3.5 μόλις καὶ μετ᾿ οὐ πολύ ("grudgingly, though before long"); 3.22 καὶ πρῶτοι (perhaps for πρῶτον); 3.43 the Callimachus line differs from the modern text of Hymn 1.10; 3.45 περί in 1 Kings 4:34 rendered by the LXX sense παρά.
- Readings that could go either way, kept and noted: 3.10 οὐχ ὑποτεμνομένας; 3.12 οὐ πάντως ("not altogether"); 3.14 "he" taken as Jesus (ὁ λόγος possible); 3.26 the εἶτ' clause as a statement (could be a question); 3.30 τίνες rendered "some"; 3.33 "siding with those who did not accept it"; 3.34 "him" taken as the God over all; 3.35 an unclosed TEI quotation mark, not quoted; 3.45 Ezekiel 28:3 as a question expecting yes; 3.48 προηγουμένως; 3.54 τὰ ἐγκείμενα and πρεσβεύοντες; 3.58 "notorious for his opposition to virtue"; 3.74 τερατωδεστέρους; 3.75 and 3.79 "the father of the Christian teaching" left open (God likelier).
- Checked from memory only, no printed text at hand: 3.32 the article in εἰς ᾅδην (Psalm 16:10, Acts 2:27); classical sources in the notes (Herodotus 4.95, Diogenes Laertius 7.36, Clement Stromata 5.9.57, Iamblichus Life of Pythagoras 17.74, Plato Phaedrus 260c, Aristophanes Wasps 191). No classical citation is inline.
- 3.21: the mountain citations (Matthew 5:1, 17:1–2, 17:14–18) mark a pattern, not a quotation; alternatives are in the notes.

Next: settle 3.37 against the printed page; run the `verify_translation_qa` packet for Book 3.

## 2026-10-23 (assembled 2026-10-24): Book 5 translated whole from the Greek

Claude translated Book 5 from Koetschau's Greek (GCS 2–3, 1899, Perseus TEI), with Cloudflare AI off and no outside model. Each chapter got a fresh translation (Pass A gloss with lemmas, then Pass B reading English), then a separate clause-by-clause review against the Greek. Crombie (ANF 1872) and Chadwick (1953) were not used or consulted.

Counts: 65 chapters, 65 English rows, 65 source rows, 213 paragraphs, about 24,200 English words (17,200 Greek words), 65 justifications (2,969 Greek lemma tags, 209 Scripture references in `bible_refs`). All 65 review verdicts are pass.

Files:
- `translations/cels_b5_source.json` and `translations/cels_b5_english.json`: the whole book, one row per chapter.
- `reviews/justifications/cels_b5_01.json` to `cels_b5_65.json` (the old 01 and 65 receipts were replaced; git has them). Each record keeps the review coverage, changes and verdict, and lists the open doubt for its chapter in `notes`.
- `translations/cels_b5_meta.json`: title "Against Celsus, Book V", new blurb, first_english false with the Crombie/Chadwick note, text_history names the copy-text. Old "Complete on this page"/"closeout"/"sampled" wording removed.
- Old `cels_b5_english.json` and `cels_b5_source.json` (the 4-row summary) moved with `git mv` to `translations/_superseded/`. Book 5 had no other slice files.

Source check: all 65 staged rows match the TEI chapters letter for letter (Greek letters compared, punctuation and spacing ignored). No row is near the 1,200-character cut; the shortest is 769 characters.

Assembly changes, no change of meaning:
- Titles put in sentence case to match Books 1 and 3 (33 titles; letter case only); straight apostrophes in five titles made curly. God, the Church, the Teacher (5.51) and the Angel of Great Counsel (5.53) keep capitals.
- 10 justifications (5.4, 8, 39, 40, 42, 43, 46, 60, 63, 64): the inline Greek lemma tags were moved from the Pass A text into `lemmas[]` so the gloss is under the 25% Greek share. No gloss words changed; each record says so in `notes`. The staged chunks keep the full tagged gloss. No sentences were split.
- Two inline citations are written in short form and left as they are: 5.33 "(Jeremiah 16:19; 14:22)" and 5.58 "(Matthew 21:41, 43)".

Checks run: `pipeline.check_pass_ab` on all 65 justifications (ok=65 fail=0); `--tip-ready` on the pair (ok); `output_guard_errors` with full-stop check (clean); `work_lint` rules on the Book 5 rows (0 findings); TEI comparison (0 mismatches); site loader `load_origen_contra_celsum` shows "Against Celsus, Book V", 65 sections, status available, first_english false.

Not run: `pipeline.verify_translation_qa` packet and the source/English hash receipt (SOP section 3). No `work_receipt.json` was written. Nothing committed.

Open doubts (none block; the owner may want to look at the first group):
- Owner's choice: 5.33 λογικὰς μαχαίρας as "swords of speech" ("rational" or "verbal" swords also possible); 5.37 ἔδοξεν as "was seen to have become man only lately" ("seemed" is more literal; kept to avoid a docetic reading); 5.65 οἱ ἐν τοῖς λόγοις διαβεβηκότες as "well grounded in the teachings" (or "gone far in the doctrines").
- Check against Koetschau's apparatus: 5.48 περιτεμνομένων (the argument may want the uncircumcised; translated as printed); 5.55 υἱοὺς θεῶν rendered "sons of God" to match Genesis 6:2; 5.50 crux († ἑωρακέναι τινά), rendered by its clear sense; 5.53 the last sentence is broken and has an editorial supplement, printed as a broken-off quotation; 5.58 συνεργὸς τοῦ ἀγγέλου ἄγγελος θεοῦ kept as printed with "Angel" for Christ (τοῦ λόγου may be meant).
- Text problems rendered by sense and noted: 5.14 ἀποφαίνειν has no governing verb ("one may show"); 5.19 εἰρημένα may be corrupt; 5.27 θεῖον may be corrupt; 5.28 the double negative rests on Koetschau's supplement (καὶ).
- Readings that could go either way, kept and noted: 5.4 "named gods in the sacred Scriptures" (no verse given, none cited inline); 5.5 ἄλλο τι γένος παρὰ θεοῦ; 5.12 νοητὰ κλήματα as "spiritual branches" (the word means "grasped by the mind"); 5.16 ἐπί τινι τέλει "for some end" (purpose or time limit); 5.17 καθαρσίου as a noun; 5.19 οἰκονομικῶς ἀληθοῦς "truth given by way of accommodation"; 5.25 τῶν νομοθετουμένων with τῆς γῆς; 5.26 μετρίως "goes some way toward"; 5.36 ὁ λόγος as Ammon's ruling; 5.39 γεγενημένην as "begotten"; 5.41 Δία Ὕψιστον word order; 5.44 τινα taken as singular (the soul of Jesus); 5.56 three things said of each account; 5.57 προνοεῖσθαι with αὐτόν (the risen Jesus); 5.59 where Celsus's quotation ends; 5.64 διὰ τί γὰρ οὔ φαμεν as "For do we not also say ...?" ("why" left out).

Next: run the `verify_translation_qa` packet for Book 5; check the apparatus items above against the printed Koetschau page.

## 2026-10-23 (assembled 2026-10-24): Book 2 translated whole from the Greek

Claude translated Book 2 from Koetschau's Greek (GCS 2–3, 1899, Perseus TEI), with Cloudflare AI off and no outside model. Each chapter got a fresh translation (Pass A gloss with lemmas, then Pass B reading English), then a separate clause-by-clause review against the Greek. Crombie (ANF 1872) and Chadwick (1953) were not used or consulted.

Counts: 79 chapters, 79 English rows, 79 source rows, 250 paragraphs, about 30,100 English words (21,700 Greek words), 79 justifications (3,478 Greek lemma tags, 348 Scripture references in `bible_refs`). Review verdicts: 77 pass, 2 needs-owner (2.77, 2.78, below).

Files:
- `translations/cels_b2_source.json` and `translations/cels_b2_english.json`: the whole book, one row per chapter.
- `reviews/justifications/cels_b2_01.json` to `cels_b2_79.json` (the old 01 and 79 receipts were replaced; git has them).
- `translations/cels_b2_meta.json`: title "Against Celsus, Book II", new blurb, first_english false with the Crombie/Chadwick note, text_history names the copy-text. Old "closeout"/"sampled" wording removed.
- Old `cels_b2_english.json` and `cels_b2_source.json` (the 4-row summary) moved with `git mv` to `translations/_superseded/`. Book 2 had no other slice files.

Source check: all 79 staged rows match the TEI chapters letter for letter (Greek letters compared, punctuation and spacing ignored). No 1,200-character cut in Book 2.

Assembly changes, no change of meaning:
- Titles put in sentence case to match Books 1 and 3 (letter case only). Straight quotes and apostrophes made curly in chapters 13–79; 2.20 gained a missing space before a quotation.
- 2.10: lacuna marker ". . . [lacuna]" changed to "[…]", the marker `work_lint` expects.
- 2.40: one sentence split for the sentence-shape gate. The bracketed clause "(men who think the pious most impious …)" became its own sentence, "These men think …", and "and above all when these men even rush" became "above all when they even rush". Recorded in the row's notes and the receipt's `revisions`.
- 2.67: "For not all that he was was known even to those by whom he was known" became "For even those who knew him did not know all that he was" (the output guard reads "was was" as a doubled word). Same sense; recorded.
- 2.22, 2.31, 2.40, 2.68: the longest Greek lemma tags (4, 4, 4 and 7) taken out of the Pass A text so the gloss is under the 25% Greek share. All stay in `lemmas[]`; no gloss words changed. The staged chunks keep the full tagged gloss.

Checks run: `pipeline.check_pass_ab` on all 79 justifications (ok=79 fail=0); `--tip-ready` on the pair (ok); `output_guard_errors` with full-stop check (clean); `work_lint` rules on the Book 2 rows with source (0 findings); TEI comparison (0 mismatches); site loader `load_origen_contra_celsum` shows "Against Celsus, Book II", 79 sections, status available, first_english false.

Not run: `pipeline.verify_translation_qa` packet and the source/English hash receipt (SOP section 3). No `work_receipt.json` was written. Nothing committed.

Open doubts:
- **2.77 (needs owner):** ὅτι μερίς ἐστι τοῦ θεοῦ has no stated subject. "That God has a portion" is a guarded rendering (likely Israel as the Lord's portion, Deuteronomy 32:9 LXX). Check Koetschau's apparatus.
- **2.78 (needs owner):** λεγέτωσαν δ᾿ Ἰουδαῖοι, ἐὰν ἡμῖν ἐγκαλοῦντες φάσκωσιν is rendered by sense ("if the Jews bring charges against us, let them answer this"); the wording may be corrupt. Check Koetschau's apparatus.
- Check against Koetschau's apparatus: 2.34 (ἦ γάρ may be ἢ γάρ; the last sentence rests on Koetschau's supplied ἤ); 2.44 ὁ θεός ("God was numbered with the lawless") kept as printed, possibly corrupt; 2.61 τῇ φασκούσῃ (Thomas agrees with "the woman", where John 20:25 has the disciples), look for a variant τοῖς φάσκουσι; 2.68 οὐκ ἀδύνατον ἥξειν looks corrupt, rendered by its sense; 2.71 ἢ μεταγνόντας may be damaged.
- Readings that could go either way, kept and noted: 2.4 ὁ τοῦ θεοῦ παῖς as "the Son of God" ("Child of God" is the literal choice); 2.6 τοῦτον as "that law" (could be God); 2.9 κατὰ τὸν τῶν ὅλων θεόν as "in accordance with"; 2.11 read as a question (could be a concession); 2.14 "made it seem a trivial thing", and "our" added in "the fathers of our doctrines"; 2.27 ὡς ἐκ μέθης ἥκοντας εἰς τὸ ἐφεστάναι αὑτοῖς (doubtful); 2.30 "the many peoples of the earth" (or "most of those on earth"); 2.44 "than he" supplied; 2.51 "Celsus caught a hint from Scripture" and the appositive "the uncreated first principle, the God of all"; 2.56 βίᾳ νομιζομένων as "thought to have gone down to Hades by force"; 2.66 ὁ λόγος as lower-case "the word" (Scripture), the divine Word possible; 2.72 οὐ πάντως "by no means" (or "not necessarily").
- 2.50: the Daniel pointer (Daniel 8:23–25) comes from memory that Origen quotes it in 6.46; check against the Book 6 text.
- 2.13: the translator note calls the Sicarii "apparently Samaritan"; a scholarly inference, notes only, not in the English.

Next: settle 2.77 and 2.78 against the printed Koetschau page; run the `verify_translation_qa` packet for Book 2.

## 2026-10-23 (assembled 2026-10-24): Book 4 translated whole from the Greek

Claude translated Book 4 from Koetschau's Greek (GCS 2–3, 1899, Perseus TEI), with Cloudflare AI off and no outside model. Each chapter got a fresh translation (Pass A gloss with lemmas, then Pass B reading English), then a separate clause-by-clause review against the Greek. Crombie (ANF 1872) and Chadwick (1953) were not used or consulted.

Counts: 99 chapters, 99 English rows, 99 source rows, 314 paragraphs, about 36,600 English words (26,700 Greek words), 99 justifications (4,675 Greek lemma entries, 263 Scripture references in `bible_refs`). Review verdicts: 97 pass, 1 needs-owner (4.31), 1 translator-checked only (4.99, below).

Files:
- `translations/cels_b4_source.json` and `translations/cels_b4_english.json`: the whole book, one row per chapter.
- `reviews/justifications/cels_b4_01.json` to `cels_b4_99.json` (the old 01 and 98 receipts were replaced; git has them).
- `translations/cels_b4_meta.json`: title "Against Celsus, Book IV", new blurb, first_english false with the Crombie/Chadwick note, text_history names the copy-text. Old "closeout"/"sampled" wording removed.
- Old `cels_b4_english.json` and `cels_b4_source.json` (the 4-row summary) moved with `git mv` to `translations/_superseded/`. Book 4 had no other slice files.

Source check: the staged `source_4.json` stopped at 4.98, but the TEI has 99 chapters. 4.99 (Celsus's "all things were not made for man", Origen's reply, and the closing prayer of the book) was taken from the TEI and translated from the Greek on 2026-10-24. The other 98 staged rows match the TEI letter for letter (Greek letters compared, punctuation and spacing ignored). No 1,200-character cut in Book 4. The staging script should be checked for a dropped last chapter in the other books.

Assembly changes, no change of meaning:
- Titles put in sentence case to match Books 1–3 (42 titles; letter case only); straight apostrophes made curly in 12 chapters and one title.
- 4.35: Celsus's re-quoted words now match the final 4.33 wording for the same Greek ("tracing their descent back to a first stock of sorcerers"), as the 4.35 reviewer asked.
- 4.39: "[lacuna]" changed to "[…]", the gap mark `work_lint` expects.
- 4.72: "the second book of Kingdoms" became "the second book of Samuel" (house book names; citation 2 Samuel 24:1 unchanged). 4.95: "(Wisdom 7:27)" written as "(Wisdom of Solomon 7:27)".
- 17 justifications (4.6, 7, 9, 14, 17, 18, 20, 22, 23, 26, 46, 63, 81, 92, 95, 96, 98): 1 to 15 Greek lemma tags each moved from the Pass A text into `lemmas[]` so the gloss is under the 25% Greek share. No gloss words changed; each record says so in `pass_a_structural_fix`. The staged chunks keep the full tagged gloss. No sentences were split.

Checks run: `pipeline.check_pass_ab` on all 99 justifications (ok=99 fail=0); `--tip-ready` on the pair (ok); `output_guard_errors` with full-stop check (clean); `work_lint` rules on the Book 4 rows with source (2 warnings, both expected: 4.1 ends "He says:" because Celsus's words open 4.2, and the "[ordinances]" supplement in 4.31); TEI comparison (0 mismatches over 99 chapters); site loader `load_origen_contra_celsum` shows "Against Celsus, Book IV", 99 sections, status available, first_english false.

Not run: `pipeline.verify_translation_qa` packet and the source/English hash receipt (SOP section 3). No `work_receipt.json` was written. Nothing committed.

Open doubts:
- **4.31 (needs owner):** the last sentence (αἱ λοιπαὶ παρ᾿ αὐτοῖς ἱερέων καὶ θυσιῶν, μυρία σύμβολα περιεχουσῶν ... σαφηνιζόμενα;) has no feminine noun, so a word has probably dropped out; the TEI has the same text and the same doubled "οὔτ᾿ ἐν λόγῳ". The supplied "[ordinances]" needs checking against the printed Koetschau, GCS 2, pp. 301–302.
- **4.99 (needs a second reviewer):** translated from the TEI at assembly and checked clause by clause by the translator only. The subject "God" is supplied for οἰκονομεῖ (masculine ἑαυτόν), "it" (the whole) for Celsus's ἐπιστρέφει, and the Son's titles in the closing prayer are cited inline (John 1:1; 1 Corinthians 1:24; John 14:6; 1 Corinthians 1:30). The TEI misprints ουν and τοῖ πέμπτου; read as οὖν and τοῦ πέμπτου.
- Check against Koetschau's apparatus: 4.11 Ἰνάχου τοῦ Φορωνέως kept as "Inachus, father of Phoroneus" (the article plus genitive would normally mean "son of"); 4.15 τὰ τραύματα marked as a quotation, no certain verse (Luke 10:34 likely), uncited inline; 4.24 γρῦπες ("griffins") not rechecked against the page; 4.36 "two other books against the Christians" follows the staged text (the identity of the Epicurean Celsus is disputed); 4.43 παρ᾿ οἷς τὸ ποικίλα ἤθη … πολιτεύεται may be corrupt, rendered by sense; 4.73 θεοῦ καταστήματι (θεοῦ twice) may be garbled, rendered "by God's appointment"; 4.78 ἂ ἀχθοφόροις read as ἢ ἀχθοφόροις.
- Readings that could go either way, kept and noted: 4.3 φύσει as "by way of nature", and "in their seasons" keeps the possessive of Matthew 21:41; 4.13 τοῦ ἐξαφανιοῦντος taken with θεοῦ; 4.18 "the teaching" (or "the Word"); 4.21 "as the teaching of Jews and Christians would have it" attaches to the flood or to the whole claim; 4.26 δριμυτάτην as a full superlative; 4.28 ἰδιωτικά as "naive" (or "peculiar to themselves"); 4.35 "the charge" supplied as subject of παρέρριπται; 4.51 πολλῷ κρεῖττον with no stated comparison; 4.52 "immortal beings" added to explain ἐκείνων; 4.55 subject of ᾔδει taken as Moses (the Spirit possible); 4.69 θέλει οὖν read as a statement, as Koetschau punctuates; 4.88 γνῶσιν αὐτοῦ as "knowledge of it" (or "of him"), and εὑρόντων/μαθόντων taken with the philosophers.
- House-style calls for the whole work: δαίμονες as "demons" even for "the good demons" (4.24); "Spirit" capitalised in 4.37 and in Wisdom of Solomon 12:1; "word of God" (4.43) and ὁ λόγος (4.44) lower case where Scripture may be meant, but "Word" capitalised in 4.71–72.
- Citation notes: 4.19 Hebrews 2:15 is cited for the verb "set free" (that verse is about fear of death); 4.48 Iliad 1.544 is one instance of the formula "father of men and gods"; 4.80 Genesis 3:8 and 18:1–2; 19:1 are sample verses for Origen's general reference, not quotations (the owner may want them removed); 4.95 Wisdom of Solomon 7:27 is a probable allusion; 4.94 the sneeze line (ὁ δ᾿ ἐπέπταρεν εὐχομένοιο) is not located and has no citation; Sirach 39:17 follows NRSV numbering (other Bibles 39:16–17); Euripides, Phoenician Women 546 and Odyssey 9.109 were checked from memory of the Greek line.
- Resolved at assembly: the reviewer's worry that 4.88 and 4.96 rendered θείας ὁμιλίας differently; both now read "converse with the divine" (7 uses). Still stale but harmless: in chunk 10 the Pass A gloss and notes say "corruptible" and "worm/maggot" where the English says "perishable" and "maggot".

Next: settle 4.31 against the printed Koetschau page; have a second reviewer check 4.99; run the `verify_translation_qa` packet for Book 4.

## 2026-10-23 (assembled 2026-10-24): Book 6 translated whole from the Greek

Claude translated Book 6 from Koetschau's Greek (GCS 2–3, 1899, Perseus TEI), with Cloudflare AI off and no outside model. Each chapter got a fresh translation (Pass A gloss with lemmas, then Pass B reading English), then a separate clause-by-clause review against the Greek. Crombie (ANF 1872) and Chadwick (1953) were not used or consulted.

Counts: 81 chapters, 81 English rows, 81 source rows, 281 paragraphs, about 31,400 English words (22,600 Greek words), 81 justifications (3,843 Greek lemma tags), 342 Scripture references in `bible_refs`. All 81 review verdicts are pass.

Files:
- `translations/cels_b6_source.json` and `translations/cels_b6_english.json`: the whole book, one row per chapter.
- `reviews/justifications/cels_b6_01.json` to `cels_b6_81.json` (the old 01 and 81 receipts were replaced; git has them). Reviewer doubts for a chapter sit in its `review.open_items`.
- `translations/cels_b6_meta.json`: title "Against Celsus, Book VI", new blurb, first_english false with the Crombie/Chadwick note, text_history names the copy-text. Old "closeout"/"sampled" wording removed.
- Old `cels_b6_english.json` and `cels_b6_source.json` (the 4-row summary) moved with `git mv` to `translations/_superseded/`. Book 6 had no other slice files.

Source check: all 81 staged rows match the TEI chapters letter for letter (Greek letters compared, punctuation and spacing ignored). No 1,200-character cut in Book 6.

Assembly changes, no change of meaning (the words of every section match the reviewed chunks):
- Titles put in sentence case to match Books 1 and 3 (letter case only); 6.70 and 6.71 use lower-case "spirit", as the text does ("God is spirit", John 4:24; "the spirit of the Stoics").
- Straight quotes made curly; 14 verse ranges written with a hyphen changed to the en dash used in the other 69.
- 6.16: "[lacuna]" written "[…]", the house form for a gap.
- 6.25–26: the Greek sentence runs across the chapter break (6.26 opens καὶ κατὰ ...). The comma at the end of 6.25 became "…", and 6.26 opens with "…". No sentence was split.
- 6.45: the final colon became a full stop; 6.46 opens "He speaks as follows:".
- 6.1, 7, 14, 31, 34, 37, 38, 44: 3 to 7 Greek lemma tags each moved from the Pass A text into `lemmas[]` so the gloss is under the 25% Greek share. No gloss words changed; each record says so in `pass_a_structural_fix`. The staged chunks keep the full tagged gloss.

Checks run: `pipeline.check_pass_ab` on all 81 justifications (ok=81 fail=0); `--tip-ready` on the pair (ok); `output_guard_errors` with full-stop check (clean); `work_lint` rules on the Book 6 rows (0 findings; 5 before the punctuation fixes above); TEI comparison (0 mismatches); site loader `load_origen_contra_celsum` shows "Against Celsus, Book VI", 81 sections, status available, first_english false.

Not run: `pipeline.verify_translation_qa` packet and the source/English hash receipt (SOP section 3). No `work_receipt.json` was written. Nothing committed.

Open doubts (none block; the owner may want to look):
- Doctrine and capitals: 6.17 ἀγένητον of the Son kept as transmitted ("uncreated", not "unbegotten"; some editors doubt or emend it); 6.2, 6.6, 6.16, 6.62 ὁ λόγος capitalised "the Word" (reason, the teaching, or Scripture possible; 6.62 could be "His reason requires"); 6.79 kept "our doctrine", with "our" implied.
- Text problems rendered by sense and noted: 6.8 προαιρεῖσθαι ("to weigh"; a verb of asking would fit, possibly corrupt); 6.10 εἴη γὰρ ἂν τυχὸν ῥητὸν καὶ τὸ μηδέν (literal, possibly corrupt); 6.16 lacuna after αὐτῷ ταῦτα ("refer to" supplied); 6.29 ἀντὶ τούτου καὶ τοῦ πατρός (literal, may be corrupt); 6.42 two damaged spots; 6.67 dittography (διὰ τὴν ἔτι δὲ φῶς, οὐ ἀσθένειαν, read as διὰ τὴν ἔτι ἀσθένειαν): the TEI (line 15089) has the same text, so only the printed page can settle it; 6.72 ἀναπεπνευκέναι ("drew his breath back in", or "breathed out").
- Check against Koetschau's apparatus or printed page: 6.37 whether "For truly, even a drunken old woman..." is Celsus's fragment or Origen's remark (the TEI has no spaced type; kept as Origen's voice); 6.77 the long angle-bracketed passage (καὶ τὰ ἱμάτια ... τῶν δικαίων αὐτοῦ), translated in full.
- Readings that could go either way, kept and noted: 6.1 πολὺ δὲ τὸ ἥμερον "a great civilizing work" (or "great gentleness"); 6.4 φησιν with no subject; 6.15 the list of humiliating gestures left unquoted (probably Celsus's caricature, not attributed in the Greek); 6.19 "prophetic" added to fix the antecedent of ἐκείνων γε τῶν λόγων; 6.31 the Ialdabaoth formula may describe the speaker; 6.35 "psychic demiurge" in quotation marks; 6.61 ἐν αὐτῇ (the Sabbath or the contemplation); 6.63 τοῦ θεοῦ with ναός or with κατ' εἰκόνα; 6.69 ὁμολογῶν ἀναγράφειν unclear; 6.77 "you will see his light and his garments" (or "that even his garments are light").
- Citations: checked from memory, no printed text at hand: Plato, Laws 5.742e–743a (6.16) and Letter 6, 322d–e (6.12); the Scripture in 6.31, 6.35, 6.36 (Ecclesiastes 1:6, 1 Corinthians 15, Psalms 118 and 9 in LXX numbering, Genesis 1–3, the woman with the flow of blood). 6.9 possible allusions (Song of Songs 2:5, John 20:25, Galatians 4:19) in the notes only. 6.25 the prophet who condemns Leviathan is unnamed, no citation. 6.43 Nebuchadnezzar has no inline citation (no single Ezekiel passage fits). 6.61 "compare Isaiah 45:12". 6.64 Romans 8:9 cited; 1 Corinthians 7:40 has the closer wording. 6.67 Matthew 20:30 recorded in `bible_refs` but not cited inline. 6.78 the comedy is not identified. 6.60 the earlier "days before days" passage is placed only "around 6.49–51".
- For the Book 2 lane (2.50): Book 6 quotes Daniel 8:23–25 in full in 6.46, after naming it in 6.45.

Next: settle 6.37, 6.67 and 6.77 against the printed Koetschau page (GCS 3); run the `verify_translation_qa` packet for Book 6.

## 2026-10-23 (assembled 2026-10-24): Book 7 translated whole from the Greek

Claude translated Book 7 from Koetschau's Greek (GCS 2–3, 1899, Perseus TEI), with Cloudflare AI off and no outside model. Each chapter got a fresh translation (Pass A gloss with lemmas, then Pass B reading English), then a separate clause-by-clause review against the Greek. Crombie (ANF 1872) and Chadwick (1953) were not used or consulted.

Counts: 70 chapters, 70 English rows, 70 source rows, 209 paragraphs, about 25,700 English words (18,350 Greek words), 70 justifications (3,378 Greek lemma tags), 274 Scripture references in `bible_refs`, all cited inline. All 70 review verdicts are pass.

Files:
- `translations/cels_b7_source.json` and `translations/cels_b7_english.json`: the whole book, one row per chapter.
- `reviews/justifications/cels_b7_01.json` to `cels_b7_70.json` (the old 01 and 70 receipts were replaced; git has them). Reviewer doubts for a chapter sit in its `review.open_items`.
- `translations/cels_b7_meta.json`: title "Against Celsus, Book VII", new blurb, first_english false with the Crombie/Chadwick note, text_history names the copy-text. Old "closeout"/"sampled"/"Complete on this page" wording removed.
- Old `cels_b7_english.json` and `cels_b7_source.json` (the 4-row summary) moved with `git mv` to `translations/_superseded/`. Book 7 had no other slice files.

Source check: all 70 staged rows match the TEI chapters letter for letter (Greek letters compared, punctuation and spacing ignored).

Assembly changes, no change of meaning (the words of every section match the reviewed chunks except the one spelling fix below; paragraph counts unchanged; no sentence split):
- Titles put in sentence case to match Books 1, 3 and 6 (letter case only); 7.3 "her unclean spirit" lower case (the Pythia's spirit, not the Holy Spirit).
- Straight quotes made curly (chunks 2–3, 6–8, 10–12 used straight marks); 8 verse ranges written with a hyphen changed to the en dash used in the other 26.
- 7.54: "the daemon of Heracles" became "the demon of Heracles" (δαίμων), the spelling used everywhere else in the work. This was the only "daemon" left in Book 7.
- 7.70: the Pass A gloss wrote 85 pairs as "Greek (English)"; each pair was turned round to the house form "English (Greek)" so the lemma tags could be read. No gloss word changed.
- 7.9, 24, 47, 48, 49, 70: 4 to 18 Greek lemma tags each moved from the Pass A text into `lemmas[]` so the gloss is under the 25% Greek share. No gloss words changed; each record says so in `pass_a_structural_fix`. The staged chunks keep the full tagged gloss.

Checks run: `pipeline.check_pass_ab` on all 70 justifications (ok=70 fail=0); `--tip-ready` on the pair (ok); `output_guard_errors` with full-stop check (clean); `work_lint` rules on the Book 7 rows (0 findings); TEI comparison (0 mismatches); site loader `load_origen_contra_celsum` shows "Against Celsus, Book VII", 70 sections, status available, first_english false.

Not run: `pipeline.verify_translation_qa` packet and the source/English hash receipt (SOP section 3). No `work_receipt.json` was written. Nothing committed.

Open doubts (none block; the owner may want to look):
- Check against the printed Koetschau page (GCS 3): 7.15 the copy-text prints εἰ ἐπίστασαι ὅτι οὐ τέθνηκας, where the Stoic proof seems to need "you know that you are dead"; translated as printed, with a note.
- Text problems rendered by sense and noted: 7.5 δηλοῖ δὲ τὸ τοιοῦτον ... τρεφόμενα αὐτῶν τὰ σώματα (awkward, may be corrupt); 7.47 ἐπειγομένη inside the Romans 1:21 quotation ("for all its eagerness"; doubtful reading); 7.48 οὐ μόνον ἀπὸ πάσης μίξεως has no "but also" clause (possible lacuna, rendered literally); 7.54 the Greek names the tyrant Aristocreon (the usual tradition says Nicocreon, Diogenes Laertius 9.59), kept as written.
- Readings that could go either way, kept and noted: 7.15 ἀδύνατον ἦν αὐτὸν παθεῖν ἢ δρᾶσαι χρῆναι πιστεύειν (same sense either way, no negation added); 7.23 τῶν ἐξισταμένων "those who were amazed" (Mark 10:24–26) or "those who give up their possessions"; 7.25 θεοῦ τὸ εὐαγγέλιον "the Gospel of God" (or "the God of the Gospel"); 7.32 "a 'tent' with an earthly house" is an interpretation of compressed Greek; 7.33 νοῦς, ὁρῶν τὸ κατ᾿ εἰκόνα ... ἀνειληφώς (two readings, same doctrine); 7.51 τοῦ διδάξαντος λόγου "the word that taught" (or the divine Word); 7.60 τῶν λοιπῶν Ἑλλήνων "the rest of the Greeks" as printed; 7.62 στῶμεν δ᾿ ἐκεῖθεν "But let us stop there" (or "let us take our stand from there"); 7.70 οὑτινοσοῦν ἔργου "of any task at all" (or "over each work whatever").
- Capitals: 7.18 "his Son" capitalised in Celsus's speech to match "the Father" there; the staged chunks of other books are mixed (29 "his son", 24 "his Son"), so a work-wide rule may be wanted. 7.36 Celsus's sneer "a father like him" kept in lower case, matching the requotation in 7.40.
- Citations: 7.6 the oracle "Sophocles is wise, Euripides wiser" has no inline source (scholia on Aristophanes, Clouds 144, or Diogenes Laertius 2.37, not certain); 7.18 Matthew 19:24 cited for Celsus's loose "no access to the Father" (Luke 18:25 parallel); 7.22 and 7.29 keep Origen's LXX ordinal "hundred and thirty-sixth psalm" in the text, with Psalm 137:8–9 beside it; 7.34 "the word of the Lord came by the hand of Jeremiah" matches no single verse (Jeremiah 37:2, LXX 44:2, nearest), and Deuteronomy 13:4 is likely but not certain; 7.38 ἐπέκεινα νοῦ καὶ οὐσίας echoes Plato, Republic 509b, not cited inline (Origen's own phrase); 7.55 Matthew 27:12–14 cited for Jesus's silence "under the scourges" (the nearest passage; no Gospel puts the silence at the scourging; the owner may prefer to drop it).
- Stale but harmless: Pass A glosses were not rewritten after review, so a few still give the literal sense the English corrected (for example "upon the gourd" in 7.53).

Next: check 7.15 against the printed Koetschau page (GCS 3); decide one capital rule for "his Son"/"a father like him" in Celsus's speech across the work; run the `verify_translation_qa` packet for Book 7.

## 2026-10-23 (assembled 2026-10-24): Preface translated whole from the Greek

Claude translated the Preface from Koetschau's Greek (GCS 2–3, 1899, Perseus TEI), with Cloudflare AI off and no outside model. Each chapter got a fresh translation (Pass A gloss with lemmas, then Pass B reading English), then a separate clause-by-clause review against the Greek. Crombie (ANF 1872) and Chadwick (1953) were not used or consulted. The old page held only chapters 2–6 as one-paragraph summaries; chapter 1 is now on the page for the first time.

Counts: 6 chapters, 6 English rows, 6 source rows, 18 paragraphs, about 1,830 English words (1,300 Greek words), 6 justifications (245 Greek lemma tags), 20 Scripture references in `bible_refs`, all cited inline. All 6 review verdicts are pass.

Files:
- `translations/cels_pref_source.json` and `translations/cels_pref_english.json`: the whole Preface, one row per chapter.
- `reviews/justifications/cels_pref_01.json` to `cels_pref_06.json` (the old 02 and 06 receipts were replaced; git has them). Reviewer doubts sit in each chapter's `review.open_items`.
- `translations/cels_pref_meta.json`: title "Against Celsus, Preface", new blurb, first_english false with the Crombie/Chadwick note, text_history names the copy-text, coverage "Preface, chapters 1–6". Old "closeout"/"Complete on this page"/"OET" wording removed.
- Old `cels_pref_02_06_english.json` and `cels_pref_02_06_source.json` moved with `git mv` to `translations/_superseded/`. There was no older `cels_pref_english.json`/`cels_pref_source.json`.

Source fix: the staged row for chapter 1 (`websites/fathers.saneapps.com/outputs/contra-celsum-20261023/source_pref.json`) is cut at 1200 characters, ending at "ὁ δὲ Ἰησοῦς ἐσιώπα." The translation covers the whole chapter (the tail is Matthew 27:11–14, checked word for word against the TEI, v.1 p.52). At assembly the whole chapter (1,620 characters) was taken from the TEI into `cels_pref_source.json`, so the source text, its hash in the justification and the English now cover the same words. The staged file was left as it is. Chapters 2–6 match the TEI letter for letter (Greek letters compared, punctuation and spacing ignored). Loci were made uniform ("Koetschau GCS 2–3, Contra Celsum, Preface N"); the old `section_end: null` fields were dropped.

Assembly changes, no change of meaning (the words of every section match the reviewed chunk; paragraph counts unchanged; no sentence split):
- Titles put in sentence case to match the other books (letter case only); straight apostrophes in two titles made curly.
- Lemma tags copied from the Pass A gloss into `lemmas[]`; no gloss moved or changed (Greek share of each gloss 19–23%, under the 25% gate).

Checks run: `pipeline.check_pass_ab` on the 6 justifications (ok=6 fail=0); `--tip-ready` on the pair (ok); `output_guard_errors` with full-stop check (clean); `work_lint` rules on the Preface rows (0 findings); TEI comparison (chapters 2–6 equal, chapter 1 replaced by the full TEI text); site loader `load_origen_contra_celsum` shows "Against Celsus, Preface", 6 sections, status available, first_english false, chapter 1 Greek 1,620 characters.

Not run: `pipeline.verify_translation_qa` packet and the source/English hash receipt (SOP section 3). No `work_receipt.json` was written. Nothing committed.

Open doubts (none block):
- Pref.6 οὐ πάνυ πιστοῖς kept as "not for believers at all"; "not for firm believers" is possible, since the weak in faith are named as readers. Recorded in the notes.
- Pref.3 ἡ ἐν αὐτῷ ἀγάπη kept as Paul's own love ("the love within him"), because ἦν is past; αὐτῷ could grammatically be Christ.
- Pref.1 the edition prints ὅτι οὗτοί σου καταμαρτυροῦσιν; read as ὅ τι ("what"), as in the Gospel; Origen's Matthew 26:59 has "the high priest" (singular), kept.
- Pref.2 καὶ τοῦ, ὡς ἐπιφέρει ἡ γραφή is awkward in the edition; taken as "and Scripture adds".
- Pref.1 πάντων γραμμάτων κρείττονος λόγου kept as "word" in lower case (possible play on the Word).

Next: re-extract chapter 1 in the staged `source_pref.json` if the staging tools reuse it; run the `verify_translation_qa` packet for the Preface.

## 2026-10-23 (assembled 2026-10-24): Book 8 translated whole from the Greek

Claude translated Book 8 from Koetschau's Greek (GCS 2–3, 1899, Perseus TEI), with Cloudflare AI off and no outside model. Each chapter got a fresh translation (Pass A gloss with lemmas, then Pass B reading English), then a separate clause-by-clause review against the Greek. Crombie (ANF 1872) and Chadwick (1953) were not used or consulted.

Counts: 76 chapters, 76 English rows, 76 source rows, 231 paragraphs, about 26,800 English words (19,200 Greek words), 76 justifications (3,451 Greek lemma tags), 264 Scripture references in `bible_refs`. Review verdicts: 73 pass, 2 needs-owner (8.10, 8.72); 8.76 has only the translator's own second pass (see below).

Files:
- `translations/cels_b8_source.json` and `translations/cels_b8_english.json`: the whole book, one row per chapter.
- `reviews/justifications/cels_b8_01.json` to `cels_b8_76.json` (the old 01 and 75 receipts were replaced; git has them). Reviewer doubts for a chapter sit in its `review.open_items`.
- `translations/cels_b8_meta.json`: title "Against Celsus, Book VIII", new blurb, first_english false with the Crombie/Chadwick note, text_history names the copy-text and says 8.76 had the translator's pass only. Old "closeout"/"sampled" wording removed.
- Old `cels_b8_english.json` and `cels_b8_source.json` (the 4-row summary, §§1–56) moved with `git mv` to `translations/_superseded/`. Book 8 had no other slice files.

Source check: the staged `source_8.json` stopped at 8.75, but the TEI has 76 chapters (the same dropped last chapter as Book 4). 8.76 (Origen's closing words to Ambrose and his request for Celsus's promised second treatise) was taken from the TEI (line 20232; GCS 3, pp. 292–293) and translated from the Greek on 2026-10-24. All 76 rows match the TEI letter for letter (Greek letters compared, punctuation and spacing ignored). No 1,200-character cut in Book 8.

Assembly changes, no change of meaning (the words of every section match the reviewed chunks, except 8.46 below):
- Titles put in sentence case to match Books 1, 3, 6 and 7 (63 titles; letter case only). Kept capitals for God and "His" (Book 8 capitalises pronouns for God in the body), the Creator, Lord, and names. 8.66 keeps "the Sun" (Celsus's god); 8.68 writes "One king ... the son of Cronus" in lower case, as the body does (Zeus and the earthly king of Iliad 2.205).
- Straight quotes made curly in the text of 28 chapters and in the 8.19, 8.35, 8.45, 8.55, 8.60 and 8.65 titles (the 8.35 reviewer's apostrophe note is resolved); 5 verse ranges written with a hyphen (8.4, 5, 29, 32) changed to the en dash.
- 8.46: "the fourth book of Kingdoms" became "the second book of Kings" (house book names, as Book 4 did; citation 2 Kings 4:8–17 unchanged).
- 8.1, 22, 29, 45, 52, 55, 59, 64, 76: 2 to 7 Greek lemma tags each moved from the Pass A text into `lemmas[]` so the gloss is under the 25% Greek share. No gloss words changed; each record says so in `pass_a_structural_fix`. The staged chunks keep the full tagged gloss. No sentences were split.

Checks run: `pipeline.check_pass_ab` on all 76 justifications (ok=76 fail=0); `--tip-ready` on the pair (ok); `output_guard_errors` with full-stop check (clean); `work_lint` rules on the Book 8 rows with source (0 findings; 1 before the 8.46 book-name fix); TEI comparison (0 mismatches over 76 chapters); site loader `load_origen_contra_celsum` shows "Against Celsus, Book VIII", 76 sections, status available, first_english false.

Not run: `pipeline.verify_translation_qa` packet and the source/English hash receipt (SOP section 3). No `work_receipt.json` was written. Nothing committed.

Open doubts:
- **8.10 (needs owner):** the copy-text reads ὁ μὴ καταπατῶν τὸν λόγον ("the one who does NOT trample the Word"); the TEI (line 18114) has the same μή. The English follows the only sense the argument allows and drops the negation. Check the printed Koetschau page and apparatus (GCS 3, Contra Celsum 8.10) before publication.
- **8.72 (needs owner):** the English reads λόγου ("the Word, who is over all and is God"), but the staged row and the TEI (line 20108, page mark r 214) print λογικοῦ. The emendation fits the sense (the next clause names ὁ λόγος) but departs from the copy-text. Check the printed page.
- **8.76 (needs a second reviewer):** translated from the TEI at assembly and checked clause by clause by the translator only. No Scripture is quoted. ὑγιῶν δογμάτων προτρεπομένων is taken as defining the truth ("the truth of sound doctrines that urge them on to the best life"); ὁ τῆς ἀληθείας πατήρ is capitalised as God.
- Text problems rendered by sense and noted: 8.24 οὐ φονέως χεῖρόν τι πράττει ("nothing short of what a murderer does"; literally "nothing worse than a murderer", may be corrupt); 8.30 the Pythagoras sentence (κἂν ἀπεχώμεθά ποτε ζῴων ...) is awkward; 8.55 θεραπεύειν τὰ εἰκότα τούτων δὲ ἐπιστάτας looks corrupt; 8.57 κριθέντες ὅπως ποτὲ εἶναι is obscure; 8.63 the asyndeton ἐκεῖνα ... ταῦτα may hide a lost ἤ.
- Editorial policy: 8.13 the bracketed ἀρχαγγέλους is left out, as the editor marks it; restore "and archangels" if the policy keeps editor-bracketed words.
- Readings that could go either way, kept and noted: 8.2 διότι as "Therefore"; 8.4 παρὰ ταῦτα "Over against these truths" (or "besides these"); 8.6 τῷ ... κρείττονι as Christ (or "the law greater than every earthly law"); 8.8 μόνον with "the God of the universe" (or "only through His Son"); 8.25 ὁ τοῦ θεοῦ λόγος as Scripture, lower case (or the divine Word); 8.30 masculine αὐτόν with neuter σῶμα, and ἡ γραφή ("this treatise" or Scripture); 8.31 the εἴπερ condition looks forward; 8.32 ἐπιστασία; 8.60 ὁ ἐχθρὸς τῇ τοῦ θεοῦ ἀληθείᾳ μαρτυρεῖ; 8.63 the subject of τὰ ἀγαθὰ δὲ ποιοῦσι; 8.66 who is commanded in κελεύῃ τις, εἰ τύχοι θρησκεύων θεόν; 8.68 θεὸν ἢ πατέρα θεοῦ lower case ("a god ... a father of a god"); 8.73 the subject of ἐπείγῃ (the emperor, or "if need presses").
- House-style calls for the whole work: 8.39 "Son of God" for Celsus's ὁ τοῦ θεοῦ παῖς (loses "child"); 8.48 Celsus's δαιμονίων δυνάμεων as "demonic" (the owner may prefer "daemonic" in Celsus's own words); 8.57 keeps the gloss 'the bread called "Eucharist", that is, "Thanksgiving"' for the double sense of εὐχαριστία.
- Citation notes: 8.11 Celsus's "one Lord" left uncited (only an indirect echo of Matthew 6:24); 8.20 Proverbs 2:5 cited on Origen's reading αἴσθησιν θείαν, which differs from the common LXX (as in 1.48); 8.22 Colossians 3:1 and 8.23 Hebrews 2:1 are borderline inline allusions; 8.21 Thucydides 1.70 rests on a near-verbatim match (Origen names no source); 8.16 Odyssey 9.261 checked from memory of the Greek line; 8.38 echoes of Romans 1:20 and 2 Corinthians 4:4 left uncited; 8.46 2 Maccabees 3:24–28 is the best match for "the books of the Maccabees" (Alcimus, 1 Maccabees 9:54–56, in the notes only), and νοθευθεῖσα read as "bribed" (after Herodotus 5.63, 6.66; "corrupted" is more cautious). LXX Psalm 77:49 is written as Psalm 78:49.

Next: settle 8.10 and 8.72 against the printed Koetschau page (GCS 3); have a second reviewer check 8.76; run the `verify_translation_qa` packet for Book 8.

- 2026-10-24, 4.73 recheck: the source row was not cut. TEI chapter 4.73 (lines 9810–9833) is exactly 1,200 characters (186 Greek words) and ends at λέξειν καὶ τίνα ἐμφανίσειν., the same as the staged and locked rows, letter for letter and character for character, so nothing was missing and the source file was left unchanged. A fresh clause-by-clause check of the English against the whole chapter made one change: the last sentence now reads “and what he promises to make clear” (ἐμφανίσειν depends on ἐπαγγέλλεται). The justification `cels_b4_73.json` was updated (pass_b_english, choices, review). `check_pass_ab` ok=628 fail=0 over all justifications; `--tip-ready` on the cels_b4 pair ok. Backups in `websites/fathers.saneapps.com/outputs/contra-celsum-20261023/backup-4-73/`. No locked source row is now exactly 1,200 characters except 4.73, which is complete. Doubt unchanged: θεοῦ καταστήματι (θεοῦ twice) not checked against the printed page. Nothing committed.
