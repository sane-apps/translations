# Martyrdom of Pionius — production ledger

Canonical path: `~/SaneApps/clients/translations/books/pionius/`

## Charter

- Title: Martyrdom of Pionius
- Author: Anonymous (Smyrna, Decian persecution, 250)
- Scope: the complete Martyrdom as printed by Gebhardt VIII (23 chapters), in nightly queue order.
- Why this work: high demand — the Smyrnaean presbyter, the chains, the great apologetic speeches, the nails and the fire.
- Legal: private study; new English from the Greek only. No modern copyrighted English used.
- Sources: Gebhardt 1902 (archive.org actamartyrumsel00gebhgoog), Greek copy-text. See `sources/manifest.json`.

## State (2026-10-19 night, Spark, §§1-2 lock)

- §§1-2 locked (prolog + arrest/chains), queued. Note: II's scan carries Latin-alphabet noise wiworas with no Greek meaning — dropped with explicit note.
- Pionius picks up Polycarp's thread directly: arrested on Polycarp's birthday (γενέθλιος, cf. Polycarp XVIII).

## State (2026-10-19 night, Spark, §§1-2)

- §§1-2 through the lane, both first-try passes, validate ALL_CLEAN (`reviews/audit/pionius_1/2.review.json`), justifications filed. §1: apostolic bidding, keepsake writing. §2: Decian date, Polycarp anniversary, three chains, defiled-meat suspicion answered. Promoted as drafted; lemma notes the feminine ὁμολογήτρια.

## State (2026-10-19 night, Spark, §§3-5 lock)

- §§3-5 locked (III Polemon + market; IV split in two for length — speech i/ii), queued. IV's garbles reconstructed with LXX parallels nailed by printed cf. (Ex 23:5 συναναστήσεις; Νομίζετε; διὰ ὑπογαίου πυρός) — each flagged in ocr_normalizations, never silent.

## State (2026-10-19 night, Spark, §§3-5)

- §§3-5 through the lane, all pass, validate ALL_CLEAN (`reviews/audit/pionius_3/4/5.review.json`), justifications filed. §3: Sabbath arrest, Living God, packed market — draft's unprinted Mt 4:10 dropped. §4: speech i — us→them, questions restored; every citation printed. §5: speech ii — questions restored; 1 Pet 4:18 kept as printed.
- Lesson: §5's source lives in two /tmp parts (pio_4a/4b joined then split) — repair scripts must map 5→pio_4b.txt.

## State (2026-10-19 night, Spark, §§6-9 lock)

- §§6-9 locked (V hush + true light; VI Alexander; VII theatre + Sabina; VIII persuade-or-punish + Creator), queued. Reconstructions flagged: Εἶτα (ZH«Av), ἧς (ὃ), οὐκ (00%).

## State (2026-10-19 night, Spark, §§6-8)

- §§6-8 through the lane, all pass, validate ALL_CLEAN (`reviews/audit/pionius_6/7/8.review.json`), justifications filed. §6: hush, true light, market pleas — draft's unprinted Dan 3:18 dropped; let-us-persuade-you corrected to passive. §7: Alexander — draft inverted Ἐπιλαβοῦ ἀκούειν to holding back; fixed to taking up hearing; feasts→defiled food; surely→perhaps (τάχα). §8: theatre refused, Sabina — tightened the burning line; rest as drafted.
- Lesson: direction errors (active/passive, take-hold/hold-back) are the drafter's weak joint — the critic catches some, the parent must watch voice.

## State (2026-10-19 night, Spark, §§9-12 queue)

- §9 (Creator) + §§10-12 locked (IX examination + Theodota/Politta; X prison road; XI Linus/Macedonia/Phrygian + no-burden rule), queued. XI's Αίμνον read Λίμνον; Phrygian heresy noted neutrally.

## Next

1. Promote §§9-12 drafts — §§9/11/12 pass first re-review; §10 failed on MY misattribution (Ex 20:11 belongs to VIII's catalogue, not Sabina) — dropped, re-reviewed pass. All ALL_CLEAN.

## State (2026-10-19 night, Spark, §§9-12)

- §§9-12 through the lane, all pass, validate ALL_CLEAN (`reviews/audit/pionius_9/10/11/12.review.json`), justifications filed. §9: persuade-or-punish — recitative ὅτι fixed (not causal). §10: examination + Theodota — Genesis cf. dropped, then my Exodus error caught by re-review and dropped. §11: road mockery — weaned not torn; rods literal. §12: Linus enforced over Limnos; Eutychian from the lock.
- Lesson: verify apparatus attribution per-section — a cf. printed for one chapter is unprinted in the next. The re-review critic caught what the first critic and I both missed.

## State (2026-10-19 night, Spark, §§13-15 lock)

- §§13-15 locked (XIIa lament + garble flagged; XIIb salt/sifting/Isaiah; XIII synagogue + βιοθανής + necromancy verb flagged), queued. Cf. notes stripped from source Greek to apparatus only.

## Next

1. Promote §§13-15 drafts — all pass, ALL_CLEAN. §13: lament pictures, Psalm 79 LXX numbering, garble unrendered + noted. §14: chain of printed echoes, Altogether, we-failed kept. §15: necromancy — smooth conjecture failed, marked [verb lost] in the reading, re-reviewed pass.

## State (2026-10-19 night, Spark, §§13-15)

- §§13-15 through the lane, all pass, validate ALL_CLEAN (`reviews/audit/pionius_13/14/15.review.json`), justifications filed.
- Lesson: flagged-unreadable source must surface as marked conjecture IN the English, never as smooth text — the critic enforces this.

## State (2026-10-19 night, Spark, §§16-17 lock)

- §§16-17 locked (XIV Saul proof whole; XV Ephesus lie + headlong), queued. Reconstructions flagged: Οἳ μὲν, Ἢ οὐχ ὅτι, διάκονοι, Ἃ δὲ/ἀντιτιθέναι, Εὐκτήμων forms, πρίγκιψ; kicks clause obscure-but-printed, locked literal.

## Next

1. Promote §§16-17 drafts (repair pass), packet + review + validate each.

## State (2026-10-19 morning, Spark, §§16-17)

- §§16-17 through the lane, both pass, validate ALL_CLEAN (`reviews/audit/pionius_16/17.review.json`), justifications filed (`check_pass_ab ok=1 fail=0`).
- §16: first compare failed on a FALSE completeness claim (the ἔλαττον sentence was plainly rendered; hashes proved the critic saw it — Spark hedge). Parent repair: sentence-paragraph split (Lyons-§4 pattern) + promote, fresh compare pass.
- §17: first compare rightly failed agency (ὀχλάσαι = crouch/kneel not bend; αὐτῶν = their). Parent repair: "went crouching on their own hands and feet"; τί...; given "?" — re-review pass.
- Lesson: the lane has no parent-override for compare fails — a fresh compare pass is the only path; make the repair round genuine (real fix or real re-presentation), never a naked re-roll.
- Lesson: lock scripts must write back ALL touched files — a lock that appends holding rows without saving the english file breaks every later packet structurally.

## State (2026-10-19 morning, Spark, §§18-20 lock)

- §§18-20 locked (XVI altar/Lepidus/punish-not-compel, [Β---] opening garble flagged; XVII Rufinus/Socrates/Aristides/Anaxarchus; XVIII garlands/publicus/Sabina/Asclepiades/Euctemon perjury, ἕτοιμοι + πρὸς Ἀσκληπιάδην + τὸ ἴδιον flags), queued [18,19,20]. Nightly running.
- Next: §§21-23 (XIX trial dialogue/Tῶν καθολικῶν, XX nails, XXI stadium/fire/Amen, XXII-XXIII epilogue + consular date), then Achatius (IX, Latin, text starts Gebhardt end of Pionius) as next high-demand work.

## State (2026-10-19 morning, Spark, §§18-20)

- §§18-20 through the lane, all pass, validate ALL_CLEAN (`reviews/audit/pionius_18/19/20.review.json`), justifications filed (`check_pass_ab ok=1 fail=0`).
- §18: parent skim caught drafter-added unprinted citations (Acts 14:15, John 3:17 — verbatim echoes but unprinted) — dropped; ὁμοιοπαθές fixed (shared mortal nature, not suffer-as-you-do); Euktemon/Lepidos normalized to Euctemon/Lepidus. Re-review pass.
- §19: critic rightly failed negation flip (οὐκ ἔπαθεν rendered positive) — fixed to "never suffered"; plus my own catch: Ἀραί is dismissive "away with", not "a curse upon". Re-review pass.
- §20: three Greek interrogatives (Οἴδατε, ἠδύνω, Τίς) rendered with periods — fixed to "?". Re-review pass.
- §§21-23 locked (XIX-XX trial/Catholics/claws/Latin tablet; XXI stadium/nails/Amen/deposit; XXII-XXIII crown/date/doxology; Οὐ---/πεῖραν/εἰσίν/ἡδέως/ἀπίστους flags), queued [21,22,23]. Nightly running.
- Pionius COMPLETE at 23/23 once §§21-23 pass. Next high-demand: Achatius (Acta disputationis, Latin, Gebhardt IX, text opens right after Pionius).

## State (2026-10-19 morning, Spark, §§21-23 — PIONIUS COMPLETE 23/23)

- §§21-23 through the lane, all pass, validate ALL_CLEAN (`reviews/audit/pionius_21/22/23.review.json`), justifications filed (`check_pass_ab ok=1 fail=0`).
- §21: my parent "renounce" repair of ἀπονενόησαι was WRONG — fresh compare proved madness sense via the σωφρονοῦσιν antithesis (others who sacrificed "live and are sound of mind" implies Pionius unsound). Reverted to drafter's "lost senses", corrected research, pass. Lesson: the blind critic checks the parent too — when it cites internal textual proof (antonym, motif), yield. Also: half-applied reverts are worse than either reading — assert every anchor replacement landed.
- §22: registrar (not jailer) for κομμενταρήσιος; dropped unprinted Luke 23:46 (kept printed Acts 7:59). Pass.
- §23: Quintilianus spelling; printed-only citations — dropped unprinted Gal 1:5; replaced draft's Luke 13:24 with printed Mt 7:13, then dropped printed-but-irrelevant Luke 18:24 after the critic rightly noted it lacks the narrow-door saying. Keep what's both printed AND textually true. Pass.
- Sequencing lesson: sampling packets bind whole files — ANY later book-file edit (even another section) stales earlier receipts. Batch ALL promotions before building packets/reviews; never interleave.
- Tmp lesson: /tmp packets/research vanished mid-turn — rebuild from book files when missing; durable artifacts live under the repo.
- PIONIUS COMPLETE 23/23. Next: Achatius (Acta disputationis, Latin, Gebhardt IX).
