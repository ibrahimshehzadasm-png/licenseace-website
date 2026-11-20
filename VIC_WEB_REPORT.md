# Victoria Web Set — Build Report (v17)

**Built:** 20 Nov 2026 · **Base:** `licenseace_website_v16/` copied to `licenseace_website_v17/` · **Pattern:** New South Wales web set (v16), page-for-page
**Facts used only from:** `licenseace_australia/vic_pack_foundation.md`, `vic_guide_fees.md` (+ `vic_guide_fees_translations.json` for the Urdu honesty label), `vic_questions.json`, `vic_signs_gallery.json`, `signs_vic/` PNGs.

## Pages added (4) — `australia/victoria/`

| Page | Contents |
|---|---|
| `index.html` | Overview: hero (420 · 124 · 4 · 25/32), test-format box (two routes: online course, first attempt FREE, format unpublished + in-person 32 questions / 3 options / 78% pass) with the honest label verbatim in English + Urdu (`.ur`, Jameel Noori), 4 pack cards, app CTA, 6-question FAQ + matching FAQPage JSON-LD |
| `practice-test.html` | 10-question sample quiz (same engine as the NSW page), 3 options each, English + Urdu toggle; honest label verbatim in the lead: *"Practice format: this practice test follows the published in-person format (32 questions, 78% pass). The online course's final assessment format is not published by VicRoads."* |
| `signs.html` | 124-sign gallery in 6 category sections (Warning 48 · Regulatory 49 · Guide 16 · Temporary 6 · Priority 3 · Hazard 2), English/Urdu name-and-meaning toggle, images from `assets/signs_vic/` — including the 4 Victoria-specific signs V01 Hook Turn, V02 No Hook Turn By Bicycles, V03 Tram Lane, V04 Tramway (Regulatory) |
| `fees-and-guide.html` | 9-step licence guide (online/in-person routes), format box with the full honesty label, VicRoads fee table (online first attempt Free · further attempts $28.70 · in-person $50.80 · permit issue Free · HPT $22.10 online further / $44.00 in-person · drive test $75.30; FY 2026-27, 1 July 2026 schedule), eligibility, learner/probationary conditions (zero BAC, VIC phone rule, school zones, trams), demerit points, HPT explainer, 120-hour log book (incl. **20** night hours), hook turn explainer, Academy note, quick questions, not-affiliated note |

Key stats used throughout: **420 questions · 124 signs · 4 languages** (English default; Arabic full translation; Urdu + Bengali study-aid) · **3 options** per question · learner test **32 questions, 78% pass (25/32), untimed** (in-person format) · age **16** (enrol 15y 11m) · **120-hour logbook incl. 20 night hours** (under 21).

## Also changed

- **Navigation:** the Australia group is now a **USA-style accordion with two state entries** — New South Wales and Victoria, each with its own stats line (NSW "420 Questions · 120 Signs · 4 Languages", VIC "420 Questions · 124 Signs · 4 Languages") — on **all 44 pages**. NSW links are byte-identical to v16 (verified); Pakistan/UK/Saudi/USA groups untouched (verified: old pages are byte-identical to v16 once the Australia block and the homepage VIC section are set aside).
- **Homepage (`index.html`):** new "🇦🇺 Victoria pack — free practice online" section immediately after the New South Wales section, mirroring its 4-card layout.
- **`sitemap.xml`:** +4 URLs → **44 total** (VIC entries lastmod 2026-11-20).
- **Assets:** 124 VIC sign PNGs copied to `assets/signs_vic/`.
- VIC pages carry correct `../../` relative links, the Australia accordion with the current page's Victoria link marked active, and VIC canonical/OG URLs (`https://licenseace.com/australia/victoria/…`).

## Sample questions (practice page)

10 questions taken verbatim from `vic_questions.json`, mirroring the NSW page's selection style (3 signs with images, then rules/safety interleaved): VIS001 (P01 Stop), VIS004 (R01 No Entry), VIS049 (W01 Traffic Signals Ahead), VIR001, VIR002, VIA001, VIR090 (hook turn indicator), VIR091 (hook turn intersections), VIA002, VIA003.

## Verification results — ALL PASS (24/24)

- **Internal links:** every `href`/`src` in the 4 new pages resolves to a real file — 0 broken; also 0 broken across all 44 pages site-wide.
- **Nav:** Australia accordion present on **44/44** pages with both states and both stats lines; NSW anchor lines byte-identical to v16 on all 40 pre-existing pages; those pages are otherwise byte-identical to v16 (homepage's added VIC section aside).
- **Sitemap:** exactly **44** `<loc>` entries; every URL resolves to a real file; 4 VIC URLs present.
- **Sample questions:** all 10 match `vic_questions.json` field-for-field (question, Urdu question, options, Urdu options, correct index, explanation, Urdu explanation, topic, sign image) — correct answers verified.
- **Signs:** 124 image references on `signs.html`, all unique, all pointing to existing files in `assets/signs_vic/`; 124 sign cards rendered; section counts 48/49/16/6/3/2 = 124.
- **Labels:** honest label present verbatim on the overview and practice pages; Urdu honest label on the overview; FAQ JSON-LD parses (6 questions) and matches the body FAQ exactly.

## ⚠️ Build incident (resolved — no data lost)

During setup, the workspace's goals-sync created `licenseace_website_v17` in `your_files/` as a **symlink into the v16 folder's real directory**, so the first build pass wrote into the shared v16 directory. This was caught during verification. Recovery, completed before delivery:

1. The finished v17 tree was copied to its own real directory (`goals/driveace-driving-test-prep-app/files/licenseace_website_v17`), and the `your_files/licenseace_website_v17` symlink now points there — the same arrangement as v10–v16.
2. **v16 was restored byte-for-byte from the pristine `licenseace_website_v16.zip`** (40 pages, 40 sitemap URLs, single-state Australia nav, no Victoria content — re-verified after restore).
3. The full verification suite above was then re-run against the separated folders and passes 24/24. The live site (already pushed from v16) was never affected.

**Not pushed** — git/GitHub push is the user's step (follow the v16 `PUSH_GUIDE.md` flow with the v17 folder contents).
