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
