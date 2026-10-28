# Hesychius, On Lazarus and the Palm Branches — session handoff

## 2026-10-23 — wave A assembly (Claude, no external model)

What changed (not committed):

- `translations/hilr_u02_rem_english.json` u02-rem-early: the placeholder row ("Rem early: ...") is replaced by the reviewed translation from `outputs/waveA-20261023/hesychius-in-lazarum-ramos/tr0.json` (title "The Infants' Praise and Christ's Mount"). Other row fields kept.
- Reviewer fixes (english and title only) applied from rv0/rv1/rv2 to u01-open, u01-rem-early, u01-rem-mid, u01-rem-close, u02-open, u02-rem-mid, u02-rem-close. Main errors fixed: first person "I saw" for the angels, "peace on earth" for "peace in heaven" (Luke 19:38), the Phoenicians misreading of the palm branches, the imperative misread of the purpose clause in the closing prayer, dropped clauses and Scripture, and Psalm 148:13 corrected to Psalm 147:12.
- Join fix at u01-open / u01-rem-early: both reviewers rendered the split words "ἐδιδάχθησαν καὶ | εἰς τοῦτο" as "this as well", so the joined text said it twice. u01-open now ends "they were also taught…" and u01-rem-early starts "…this: that He will raise even the foreign nations."
- `reviews/justifications/u02_rem_early.json` rewritten from the placeholder into the book's justification shape (Pass A English gloss, Greek lemmas, Scripture with LXX numbers, review notes, current source sha256).
- All four `*_meta.json`: blurb was worksheet text ("SERIES CLOSEOUT on this page"); now plain reader copy with "fresh English translation". Status stays "available". No scope set: the homily is complete (title line to Amen).
- Backups of every changed file: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/hesychius-in-lazarum-ramos/backup/`.

Checks run:

- `python3 -m pipeline.check_pass_ab books/hesychius-in-lazarum-ramos/reviews/justifications` → ok=8 fail=0.
- `--tip-ready` on all four english/source pairs → ok.
- grep -F for "Lemma-led open", "Rem early:", "Rem mid:", "Rem closeout:", "lemma and argument toward the thesis" in `translations/*_english.json` → none. Section titles carry no worksheet marks.

Open follow-ups (outside this pass's english/title scope):

- `translator_notes` are stale or wrong in several rows. u02-rem-early still carries worksheet notes (True OET, Melito skipped, densify); u01-open has the wrong ὁρμήματα claim and old edge-cut notes; u01-rem-close has "Greek text includes: ..." debris. The DOCX builder drops shop-talk notes, but not the wrong claims. The reviewers ask to cut these back to the boundary note and the Scripture list.
- The other seven justification files still hold the old machine-draft Pass B, not the reviewed English.
- `book.yml` still has `status: series-closeout`, `scope: "SERIES CLOSEOUT 65ed7e2e; true OET."` and "New English" in the description.
- Rebuild the DOCX and Logos book after the notes are cleaned.

## 2026-10-24 — follow-up cleanup (Claude, no external model)

What changed (not committed). English text and titles are unchanged (checked against the backups).

- `intro.md` (About this text): the old text said the hearers "follow him as the palm trees do" (the Phoenicians misreading) and read the closing purpose clause as a prayer. It now matches the reviewed English: Lazarus as the sign that Christ will raise all humanity, why men and angels hailed Him King, Zechariah 9:9 read phrase by phrase, and the close (palms of faith, hope, love; follow Him into the temple so that He may make us a holy temple instead of a den of robbers). It adds the source heading facts: the heading names Hesychius, priest of Jerusalem; the homily was once credited to Titus of Bostra.
- `translator_notes` on all eight rows replaced. Gone: the wrong ὁρμήματα claim, the OCR edge-cut notes, "Greek text includes: ..." debris, the generic "fragment / literal" notes, the u02-rem-early worksheet notes, and the reviewer-directed lines from tr0.json. Kept or added: boundary notes, Septuagint Psalm numbers, the editor's bracketed deletions, Bethphage pun, Titus of Bostra heading, centurion's servant counted among the raised. u02-rem-early uses tr0.json's notes, trimmed.
- Justifications `u01_open`, `u01_rem_early`, `u01_rem_mid`, `u01_rem_close`, `u02_open`, `u02_rem_mid`, `u02_rem_close`: `pass_b_english` now equals the current English; `pass_a_gloss` rewritten from `source_text` as a full clause-by-clause gloss that agrees with it (old A had "I saw", "peace on earth", "Phoenicians", imperative close, dropped clauses and debris lines); `choices`, `lemmas` (every form checked to occur in the source) and `bible_refs` (taken from the inline citations, with LXX numbers) rebuilt; `anf_compare` set as in u02_rem_early; a `review` block names the rv file. `confidence` and `checks.lemma_constraint` left as they were. The old ai-crosscheck stamps in these files describe the replaced machine English; the review block says so.
- `book.yml`: `status: available`; worksheet `scope` removed (the homily is complete); `notes` and `description` rewritten in plain words ("fresh English translation"). Author and edition unchanged; metas agree (Hesychius of Jerusalem).
- All four `*_meta.json`: `first_english_note` and `text_history.method` still carried worksheet words (OET, Melito, densify, SERIES CLOSEOUT); now plain "Fresh English translation ... from the Greek text of PG 93". Status, blurb and `claim` ids unchanged.
- Backups of every changed file: `~/SaneApps/websites/fathers.saneapps.com/outputs/waveA-20261023/hesychius-in-lazarum-ramos/backup-cleanup/`.

Checks run:

- `python3 -m pipeline.check_pass_ab books/hesychius-in-lazarum-ramos/reviews/justifications` → ok=8 fail=0.
- `--tip-ready` on all four english/source pairs → ok.
- `python3 -m pipeline.work_lint --slug hesychius-in-lazarum-ramos` → findings=0.

Still open:

- Rebuild the DOCX and Logos book (notes and book.yml changed).
- `claim` ids end in "-oet"; internal keys, left alone.
