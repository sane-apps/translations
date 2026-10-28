# Cyril of Alexandria, Fragments on 1 Corinthians — production ledger

Canonical path: `~/SaneApps/clients/translations/books/cyril-alexandria-fragmenta-1-corinthios/`

## 2026-10-24 12:51 AM ET — Wave A assembly (Claude, Mini)

What changed (not committed):

- 14 placeholder sections replaced with the reviewed Wave A translations (`outputs/waveA-20261023/cyril-alexandria-fragmenta-1-corinthios/tr0-3.json`): u01-open, u01-rem-early/mid/close, u02-open, u02-rem-early/mid/close, u03-open, u03-rem-early, u04-rem-early, u08-open, u08-rem-mid, u08-rem-close. Title, english and translator notes set; other row fields kept. Workflow wording in notes ("reviewer rv3", "current English", "Wave A") rewritten for readers.
- Reviewer retranslations applied to 15 real rows (english/title): u03-rem-mid, u03-rem-close, u05 (all four), u06 (all four), u07 (all four), u08-rem-early. Where rv3 and rv6 overlap, rv6 wins (it adopts rv3 with fixes). The old machine-draft notes described the replaced English, so these rows got short, accurate notes (u06 rows use the reviewer's own notes).
- No reviewer entry covered u02-open or u04-rem-early. Both checked clause by clause against the Greek during assembly. u02-open was kept as it was. u04-rem-early got three fixes: νοητοῖς is 'spiritual', not 'immaterial'; ἐρρίφθαι is 'cast, as it were, behind', not 'placed after'; γάρ restored ('For woman admittedly came from man').
- 14 justifications rewritten in the book's full shape (reviews/justifications/uNN_*.json): Pass A, Greek lemma tags, choices, bible_refs, edition sha256, review notes. Greek tags were trimmed from the u08-open Pass A, which failed the copied-Greek check.
- All 16 `*_meta.json`: the blurb, first_english_note and text_history.method had "SERIES CLOSEOUT / OET" worksheet wording. Replaced with plain "fresh English translation" wording. Scope added: the surviving fragments of Cyril's commentary, as printed in PG 74. Status was already "available".
- Backups of every changed file: `outputs/waveA-20261023/cyril-alexandria-fragmenta-1-corinthios/backup/`.

Checks:

- `python3 -m pipeline.check_pass_ab reviews/justifications`: ok=32 fail=0.
- `--tip-ready` on all 16 english/source pairs: ok.
- grep -F for "Lemma-led open", "Rem early:", "Rem mid:", "Rem closeout:", "lemma and argument toward the thesis": 0 files.
- `pipeline.work_lint --slug cyril-alexandria-fragmenta-1-corinthios`: 0 errors, 2 warnings (deliberate `[lacuna]` markers in u01-rem-mid and u07-rem-close).

Open (not done in this pass):

- u04-open, u04-rem-mid and u04-rem-close are still the 2 October llama machine drafts, and no review covered them. The rv3 slot in the plan was meant for u04, but rv3 reviewed u07/u08 instead. These drafts have clear errors. In u04-open, 'rose up to play' is said to stand *instead of* fornication, when Cyril means it stands *for* fornication; the title says "Gnosticism", but γνωστική means 'the one with knowledge'. They also miss the seams: u04-open does not pick up the end of u03-rem-close, u04-rem-mid does not render ἑτέρως, and u04-rem-close does not lead into u05-open. Next: retranslate and review all three from the Greek.
- Pronoun capitals for Christ and God are mixed across the book: the Wave A rows use lower case, while u04 and several reviewer rows use He/His.
- book.yml still has the worksheet scope "SERIES CLOSEOUT 59aa136b footer-safe; true OET." This pass did not edit that file.
- The justifications for the 15 retranslated real rows still hold the old machine-draft Pass A and Pass B. Rebuild them when those rows are next certified.

## 2026-10-24 1:06 AM ET — u04-open, u04-rem-mid, u04-rem-close retranslated (Claude, Mini; not committed)

- All three set aside and translated afresh from the Greek (Pass A gloss with lemmas, then Pass B), then reviewed clause by clause in a separate pass; six small fixes from that review. English, title and translator notes replaced; other row fields kept. Justifications rewritten (u04_open, u04_rem_mid, u04_rem_close) in the u04_rem_early shape, source sha256 current. Known errors fixed: "rose up to play" now stands *for* fornication; γνωστική is "the one with knowledge"; ἀφεκτέον is "abstain" (draft had "forgive"); Genesis 9:6 (not 1:27); Isaiah 28:11–12 via 1 Corinthians 14:21 (not Isaiah 66:18); Psalm 45:9 (LXX 44:10); Micah 6:8, Hebrews 3:2/Numbers 12:7, Luke 17:5, Matthew 10:1, 8 added inline. Seams: u04-open opens "…for our very selves", continuing u03-rem-close; its last Greek words are left to u04-rem-early, which gives the full clause (noted); u04-rem-mid opens "…in another way" (ἑτέρως rendered); u04-rem-close ends "…and indeed to Elamites (Acts 2:9)…", leading into u05-open. Pronouns for Christ/God/Spirit in lower case, matching u03-rem-close and u05-open. Checks: check_pass_ab ok=32 fail=0; --tip-ready ok on f1c_u04_open and f1c_u04_rem; work_lint 0 errors (same 2 lacuna warnings). Backups: `outputs/waveA-20261023/cyril-alexandria-fragmenta-1-corinthios/backup-u04/`. Still open: u04-rem-early keeps He/His and "source row" wording in its notes; the internal `claim` ids still end in "-oet".

## 2026-10-24 1:41 AM ET — follow-up cleanup: notes, justifications, book.yml (Claude, Mini; not committed)

No English text changed. Backups of every file before this pass: `outputs/waveA-20261023/cyril-alexandria-fragmenta-1-corinthios/backup-cleanup/` (book.yml, SESSION_HANDOFF.md, all 16 `*_english.json`, all 32 justifications).

- intro.md: none exists for this book (it never had one; the site's About this text has no intro to show, and the work is not yet in the site build under `cyril-fragmenta-1-corinthios`). Nothing to correct. A 3-paragraph intro would come from `scripts/work_pipeline.py intro`, which was not run.
- translator_notes rewritten on 30 rows (u04-open and u04-rem-close were already accurate and kept as they were). Removed: "source row …" ids, internal section ids (now "the previous/next section"), the lower-case-pronoun style line, "kept exact" QA phrases, and wording that described replaced English. Fixed stale notes: u02-rem-early now quotes the next section's real wording ("…and in a spiritual way"); u02-open's μόνος note now quotes "in this way, and in no other"; u01-rem-mid's itacism note quotes the current English; u04-rem-mid's εὐσεβῶς note quotes "will have the fact itself as witness"; u08-rem-mid quotes "with a cry of command" (rv6); u08-rem-close's Hebrews 2:14 note now says Cyril has "Satan" and "sting" where Hebrews has "the devil" and "power". Added reader notes from the rv files where true of the current English: u03-rem-mid (stray ἔχοντος; ἁγνεύσασθαι), u03-rem-close (Hosea 4:14 LXX; Psalm 106:28 = LXX 105:28), u05-open (Psalm 65:9, 36:8 LXX numbering), u05-rem-early (sign "to believers" kept), u05-rem-mid (Psalm 115:13 = LXX 113:21), u07-open (compiler's notes; ἀρπαχή for ἀπαρχή; Job 38:14 LXX), u07-rem-early (ἀναφωνούσης), u07-rem-mid (tree of life as printed; repeated σῶμα ψυχικόν), u07-rem-close ([lacuna]).
- Justifications: the 15 retranslated rows (u03-rem-mid, u03-rem-close, u05 ×4, u06 ×4, u07 ×4, u08-rem-early) still held the 2 October machine-draft Pass A/B. Each now has pass_b_english equal to the current English, a fresh Pass A gloss written from the Greek and checked clause by clause against the English, new lemmas (every form found in the source), choices and bible_refs that match the English, confidence "reviewed", and a review record naming the rv pass; old ai-crosscheck fields and machine-draft revisions removed. All 32 now have pass_b_english == current English.
- book.yml: status available; scope "The surviving Greek fragments of Cyril's commentary on 1 Corinthians, as printed in Migne, PG 74."; description added in "fresh English translation" wording; the worksheet notes (OET, SERIES CLOSEOUT, Melito, densify) replaced with a copy-text line. Author and edition unchanged (the metas agree: Cyril of Alexandria, PG 74).

Checks: `python3 -m pipeline.check_pass_ab books/cyril-alexandria-fragmenta-1-corinthios/reviews/justifications` ok=32 fail=0; `--tip-ready` ok on all 16 english/source pairs; `python3 -m pipeline.work_lint --slug cyril-alexandria-fragmenta-1-corinthios` 0 errors, 2 warnings (the deliberate `[lacuna]` markers in u01-rem-mid and u07-rem-close). A scan of every English row, meta and book.yml for OET, SERIES CLOSEOUT, Melito, densify, tip, Pass A/B, lane, "new English", "source row", reviewer, Wave A, section ids: 0 hits.

Still open (English not touched in this pass):
- Pronoun capitals for God/Christ are still mixed: u04-rem-early, u07 and u08 rows use He/His; most others use lower case.
- Tome headings differ in form: "Tome 4, Discourse 3." (u03-rem-close) vs "Tome Four. Discourse Four." (u04-open) and "Tome Five. Discourse One."; τόμος is "book" in u02-rem-mid but "tome" in u03-rem-early.
- Internal `claim` ids still end in "-oet" (not reader-facing).
- No intro.md; write one through the work_pipeline intro step before the work ships.
