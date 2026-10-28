# On the Pascha (Peri Pascha) — production ledger

Canonical path: `~/SaneApps/clients/translations/books/melito-peri-pascha/`

## Charter

- Title: On the Pascha (Peri Pascha)
- Author: Melito of Sardis (c. 180)
- Scope: the whole homily, §§1–105 in the standard section numbering.
- Why this book exists: it is the library's last copyright-walled work and the open
  gap in Timeline dossier answer-pagans-jews (the §96 locus, ὁ θεὸς πεφόνευται).
  Owner directive 2026-10-24: the work is 2nd century and cannot itself be
  copyrighted; find the lawful way in.
- Diagnosis (full record in reviews/RIGHTS_DOSSIER.md): the wall was never
  Melito. The work's text was lost until the 20th century, so every edition and
  translation is modern. The first, Bonner's (Studies and Documents XII,
  Christophers, London / University of Pennsylvania Press, Philadelphia;
  published 18 Oct 1940; US registration A147791), was RENEWED on 10 Sep 1968
  (renewal R442133, Catalog of Copyright Entries, Renewals, 1968 Jul–Dec, PG
  eBook #11838): US copyright in Bonner's edition and translation runs until
  1 Jan 2036. Testuz 1960, Perler SC 123 (1966), Hall OECT (1979), and
  Stewart-Sykes (2001) are likewise in copyright. The full English translations
  circulating on devotional websites are those modern translations posted
  without license; not usable.
- Route: the project's own fresh translation from its own transcription of the
  papyrus witnesses. The Greek words are Melito's and public domain. Transcribe
  from the manuscript images (P. Chester Beatty XII via CSNTM; P. Bodmer XIII
  via the Fondation Martin Bodmer), collate against Hall and Perler in print to
  catch transcription errors only, and translate fresh — the pipeline rule used
  for Gregory of Tours (2026-10-20): transcribe from the images; modern
  editions are finding aids and error checks, never copied text or wording.
  Lacunae are marked, never silently filled from an editor's conjecture; where
  the parallel witness supports a reading, adopt it and note it.
- Legal: private study; new English from allowed sources; no modern
  copyrighted Greek edition text or English copy.

## State

- Book filed 2026-10-24 (Spark) under the owner directive of the same day.
  Untracked in git on arrival: the translations tree carries another lane's
  WIP, so the commit is left to the lane; this file is the record meanwhile.
- Sources: witnesses identified 2026-10-24. PHASE 1 DONE 2026-10-25 (Spark):
  image sets pulled and locked in sources/ with per-image provenance in
  sources/manifest.json. Bodmer: all 107 canvases of codex PB C (barcode
  1072205366, CC BY-NC 4.0 per the IIIF manifest); Melito canvases 056-095
  at full resolution (sources/bodmer-xiii/full/, 40 files), rest of codex at
  50% (codex-context/, 67 files); reassembled-transfer sha256 verified.
  Chester Beatty: only 100 px thumbnails are served anonymously (36 files);
  the high-res viewer requires a free CSNTM account login (not created, not
  bypassed) - see sources/chester-beatty-xii/README.md.
- Transcription: STARTED 2026-10-25. Workspace transcriptions/ (conventions
  in its README). Done: title leaf; pp. Alpha (§§1-3) and Beta (§§3-6),
  diplomatic only (fragmentary leaves, lacunae bracketed); p. Gamma
  (§§6-9 inferred, complete page); pp. Delta-Epsilon (§§9-13, complete).
  Resolved source text filed for §§9-13 (translations/mpp_source.json +
  mpp_meta.json). Flagged unsettled readings are listed inside the
  transcription files (p. Gamma lines 1, 2, 8-10; p. Delta GENNATHR and
  OUTOS EN; p. Epsilon LYSE and DIASQAI) and are the first collation
  questions. Cross-check log: reviews/CROSSCHECK_2026-10-25.md (Grok
  tasked twice, timed out without a verdict; Gemini CLI dead on
  IneligibleTier; Antigravity agy unauthenticated; internal two-pass
  re-read substituted).
- Translations: NOT STARTED. Do not start from Bonner 1940, Hall 1979,
  Stewart-Sykes 2001, or any website-posted translation.
- DOCX: not built. Logos build: not compiled. Bible-link verify: not done.
- Rights dossier: reviews/RIGHTS_DOSSIER.md (renewal evidence verbatim).

## Next

Production lane, in order:
1. DONE 2026-10-25: image sets pulled; receipts and provenance in sources/
   (Chester Beatty high-res still login-blocked, see above).
2. IN PROGRESS: transcribe §§1–105 section by section (transcriptions/
   workspace; §§1-13 done 2026-10-25). Next pages: canvas 064 (§§14-17),
   then in sequence. Resolve §§1-8 only after the collation pass.
3. Collation pass against Hall (1979) and Perler (SC 123) in print; log every
   divergence from our transcription in reviews/.
4. Translate fresh at the pipeline standard; review pass; build; ship. Then
   close the answer-pagans-jews gap with the §96 quote sourced to OUR
   transcription, and hand the finished text to the narration lane (site
   audio + YouTube on the standard flow).

Scope: ~105 sections, on the order of 9,000 Greek words; the English rendering
runs ~13,000 words and the finished narration ~90 minutes. Transcription is
the long pole (uncial papyrus, lacunose in places); translation after
transcription follows standard pipeline pace. Multi-session job; not a
single-sitting one.
