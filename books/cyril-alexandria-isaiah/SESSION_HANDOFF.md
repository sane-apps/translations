# Cyril of Alexandria, Commentary on Isaiah: session handoff

## 2026-10-24 (follow-up cleanup, Claude, Mac Mini; not committed)

What changed (English reading text untouched; only notes, front matter and receipts):

- `intro.md` rewritten short and plain. The old last line said the volume holds "the prologue and Books 2 through 5"; the rows include Book I (Logoi 1 to 5), so it now says "passages from the prologue and from each of the five books", as the metas do. The "evangelist of the Old Testament" phrase is gone: the prologue calls Isaiah "both prophet and apostle", and the intro now says that.
- `book.yml`: `status: available` (matches the metas); `scope` is one reader line; `description` uses "fresh English translation"; `notes` no longer carries worksheet text (it now records that Hill's 2008 English is in copyright and was not used). Author and edition unchanged. Note: `scripts/build_corpus_catalog.py` counts only series-closeout/series-closed/done/verified as complete, so this book now reads as not complete there.
- `translator_notes` on all 89 rows. Rows whose reviewer file supplied notes keep them, with "the row" changed to "the section", section ids and PDF/font-encoding wording removed, and one quotation corrected to match the English ('For since, with God defending them, …'). Other rows lost the old draft notes (OCR/[p6] remarks, "aims to preserve", "per instructions", "previous draft", notes that described replaced English or were false, such as the ἱδρώτων "correction" and Isaiah 3:12 for 3:10). They now carry only: where the section opens or breaks off, a few checked readings (Μεωδάχ/Merodach, the dotted gap shown as [lacuna], Septuagint Isaiah 3:10), and Septuagint Psalm numbers for the Psalms cited inline (chapter only).
- `reviews/justifications`: the 88 files for rows changed on 2026-10-23 were rebuilt. `pass_b_english` is the published English; `source_text` is the current source row (this fixes the stale reuse footer in `book2_rem_early`, the font-encoded text in `book5-part2_rem_close` and the 20 truncated opening rows); new English Pass A glosses written from the Greek clause by clause; new lemmas (forms copied from the source) and choices that match the English; `bible_refs` from the inline citations; edition sha256 refreshed. The old ai-crosscheck stamps judged the earlier English and are recorded as superseded in `review_notes`, not carried forward; old `variants`, `notes` and `repair_notes` dropped. `confidence` stays `machine_draft`. `book5-part2_rem_mid.json` was already current and is unchanged.

Checks (Mini):

- `python3 -m pipeline.check_pass_ab books/cyril-alexandria-isaiah/reviews/justifications`: ok=89 fail=0 (was 63/26).
- `--tip-ready` on all 45 English/source pairs: 45 ok.
- `python3 -m pipeline.work_lint --slug cyril-alexandria-isaiah`: one warning, "[lacuna]" in `logos1-rem-mid` (allowed).

Backups of every file changed in this pass: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-isaiah/backup-cleanup/`.

Still open:

- The receipts are machine drafts. No independent source-backed review has been run on the new Pass A glosses, so nothing here is `source_verified`.
- Row and meta `claim` ids still end in "-oet" (for example `cyril-isaiah-logos1-open-oet`); the site does not show them, and they were left alone so the claims ledger still matches. Source-row `title` fields still carry "CLOSEOUT" labels; they were left alone because changing the source files would change the edition hashes.
- The DOCX (`cyril-isaiah.docx`) was not rebuilt.

## 2026-10-23 (Wave A assembly, Claude, Mac Mini; not committed)

What changed:

- `book5-part2-rem-mid` was a placeholder ("Rem mid: …"). It now holds the reviewed translation from `outputs/waveA-20261023/cyril-alexandria-isaiah/tr0.json` (site repo), title "Christ the Everlasting Light", with the translation's own notes.
- Reviewer fixes rv0 to rv14 applied to 88 real rows in all 45 English files (english and title; translator notes too where the reviewer supplied them). The rv10 staged row for `book5-part2-rem-mid` matched tr0 exactly.
- On the 64 reviewed rows that came with no new notes, 67 note lines were dropped: worksheet text ("Condensed lemma-led tip", "densify", "Earliest-forward", "True OET") and notes that quoted English the reviewers replaced.
- Book names: "Fourth Book of Kingdoms" became "Second Book of Kings" (3 rows) and "Second Book of Kingdoms" became "Second Book of Samuel" (1 row), as `work_lint` asks.
- English section id `book2-open-open` renamed `book2-open` to match its source row and justification.
- Source repairs, with the meaning unchanged: the modern PDF reuse footer ("Επιτρέπεται η ελεύθερη χρήση …") was removed from `book2-open` and `book2-rem-early`. `book5-part2-rem-mid` and `book5-part2-rem-close` were in the PDF's Latin-letter Greek font encoding. They were decoded character by character to Unicode Greek; spacing, line breaks, 6/9 markers and column numbers were left as they were.
- New justification: `reviews/justifications/book5-part2_rem_mid.json` (Pass A gloss, 44 Greek lemmas, choices, Scripture refs, review notes).
- All 45 `*_meta.json`: status "available", plain blurb ("fresh English translation"), scope "Selected passages from the prologue and from each of the five books", `first_english` set to false (Hill's 2008 English exists, per `book.yml`), and worksheet wording removed from the note and method.

Checks:

- `python3 -m pipeline.check_pass_ab reviews/justifications/book5-part2_rem_mid.json`: ok=1 fail=0.
- `--tip-ready` on all 45 English and source pairs: 45 ok. Before this session three failed: `book2_open`, `book2_rem` and `book5-part2_rem`.
- `grep -F` for "Lemma-led open", "Rem early:", "Rem mid:", "Rem closeout:" and "lemma and argument toward the thesis" in `translations/*_english.json`: none.
- `python3 -m pipeline.work_lint --slug cyril-alexandria-isaiah`: one warning left, "[lacuna]" in `logos1-rem-mid`, which the QA rules allow.

Backups of every changed file: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/cyril-alexandria-isaiah/backup/`.

Still open:

- 88 old justification files no longer match the reviewed English in their `pass_b_english`. 26 of them also fail `check_pass_ab` for older reasons (Greek-heavy Pass A, missing lemmas). They need new receipts before anyone claims `source_verified`.
- On reviewed rows that got no new notes, the notes that remain were not each checked against the new English.
- `book.yml` `scope` and `notes` still carry worksheet wording ("SERIES CLOSEOUT tip", "True OET"). They were outside this task.
- The DOCX (`cyril-isaiah.docx`) was not rebuilt.
