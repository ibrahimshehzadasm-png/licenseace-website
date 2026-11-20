# LicenseAce Website v19 — Report

**Scope:** surgical patch on v18. Fixes the static (non-toggle) Urdu honest-label text on non-Pakistan pack pages, caught live by the user on the Saudi index page: the label translation printed under the English was Urdu; for Saudi (and the Australia packs) it must be Arabic. The label box is static HTML, not connected to the quiz translation toggles — which is how v18 missed it.

**Base:** full copy of `licenseace_website_v18`. Symlink trap checked: `your_files/licenseace_website_v19` resolves to a NEW real folder (`goals/driveace-driving-test-prep-app/files/licenseace_website_v19`), not into v18. v18 was not written to (no v18 file modified during this build; final `diff -rq` shows exactly the 4 intended files differ).

## Changes (4 files)

On each page below, the label box printed `<span class="ur">…Urdu label…</span>` under the English honest label. The Urdu text was replaced with the pack's **Arabic** label, taken **verbatim** from that pack's `simulator_honesty_label.ar` in its guide-translations JSON (byte-compared after the edit — identical on all 4 pages). The span is now `<span class="ar" lang="ar" dir="rtl">`, and one CSS rule was added beside the existing `.ur` rule on those 4 pages only: `.ar{display:block;direction:rtl;text-align:right;line-height:1.9;color:var(--slate)}`. (No Arabic class existed anywhere on the site; quiz Arabic uses the same RTL-without-Urdu-font pattern. The `.ur` class applies the Urdu Nastaleeq font, which is wrong for Arabic text, so it was not reused.)

1. **saudi-arabia-driving-test.html** — label span Urdu → Arabic (source: `licenseace_gulf/sa_guide_fees_translations.json`). Plus the two practice-test translation claims on the same page, which v18's practice-page fix had left stale:
   - Format-box closing line: "…in English with an Urdu translation." → "…in English with Arabic and Urdu translations."
   - Practice-test card text: "…explanations in English and Urdu." → "…explanations in English with Arabic and Urdu translations."
2. **australia/new-south-wales/index.html** — label span Urdu → Arabic (source: `nsw_guide_fees_translations.json`).
3. **australia/victoria/index.html** — label span Urdu → Arabic (source: `vic_guide_fees_translations.json`).
4. **australia/queensland/index.html** — label span Urdu → Arabic (source: `qld_guide_fees_translations.json`).

**Checked and deliberately left unchanged:**
- saudi-arabia-licence-fees-guide.html — carries the label box in English only; no translation is printed under it, so there was nothing to swap.
- australia/*/fees-and-guide.html (NSW/VIC/QLD) — no label translation printed; unchanged.
- All other Urdu mentions on the changed pages are factual English statements (e.g. FAQ: "Urdu is not a DKT language") — correct as they stand.

## Sweep — static Urdu-script text on remaining non-Pakistan pages (REPORT ONLY, nothing changed)

- **uk-traffic-signs.html — the one real finding.** All **167** sign cards print the Urdu sign name as visible static text (`<span class="ur urname">`) directly under the English name, shown by default. This page has **no language toggle** at all. Every other pack's gallery (Saudi, California, Texas, New York, Florida, Illinois, NSW, VIC, QLD) keeps its translations in `data-mur` attributes behind a `langsel` language toggle, so nothing is printed by default there — the UK gallery is the odd one out. Left for a later user decision: give the UK gallery the same toggle treatment, or keep the bilingual names as a deliberate UK-Pakistani-audience design.
- **All other non-Pakistan pages are clean:** UK index/fees/practice, all USA index/fees/practice pages, articles, homepage and privacy contain **zero** static Arabic-script text blocks outside toggles.
- Note (unchanged from v18's observation): the Saudi/NSW/VIC/QLD signs galleries' toggles still offer EN/UR only (no Arabic in the gallery toggle), and their Urdu sits in toggle data attributes, not in default print. The label-box defect fixed in this version was a different mechanism (static HTML).
- Punjab/Pakistan pages excluded from the sweep by design (Urdu-first).

## Checks (all PASS)

- Page count: **48** HTML pages; sitemap.xml **byte-identical to v18, exactly 48 URLs** (incl. the 4 QLD URLs).
- `diff -rq` v18 ↔ v19: **only the 4 intended files differ** — every quiz/practice page is byte-identical to v18; LANGMAP contents and defaults unchanged (all 10 practice pages: `let lang = 'none'` in both versions).
- Arabic label text on each changed page **byte-compared equal** to its source JSON value; the old Urdu label string no longer appears on any of the 4 pages.
- Per-file diffs contain only the intended blocks (Saudi +4/−3 lines; each Australia index +2/−1 lines: the `.ar` CSS rule and the label span, plus Saudi's two claim lines).
- Internal link check across all 48 pages: **4,343 internal references, 0 broken**.
- v18 verified pristine after the build.

## Deliverables

- Folder: `licenseace_website_v19/` (this report inside it)
- Zip: `licenseace_website_v19.zip` (full folder, top-level `licenseace_website_v19/`)

**Push:** replace the site contents with the v19 folder's contents (same as v18's push), commit e.g. "v19: Arabic honest labels on Saudi + Australia index pages". No sitemap change, so nothing new to submit to GSC.
