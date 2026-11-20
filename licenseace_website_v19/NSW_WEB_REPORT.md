# NSW Web Set — Build Report (v16)

**Built:** 19 Nov 2026 · **Base:** `licenseace_website_v15/` copied to `licenseace_website_v16/` · **Pattern:** Saudi Arabia web set (v15), page-for-page
**Facts used only from:** `licenseace_australia/au_pack_foundation.md`, `nsw_guide_fees.md` (+ its translations file for the Urdu honesty label), `nsw_questions.json`, `nsw_signs_gallery.json`, `signs_nsw/` PNGs.

## Pages added (4) — `australia/new-south-wales/`

| Page | Contents |
|---|---|
| `index.html` | Overview: hero (420 · 120 · 4 · 12/15 + 29/30), DKT format box with the dual-gate honest label + Urdu label (`.ur`, Jameel Noori), 4 pack cards, app CTA, 6-question FAQ + FAQPage JSON-LD |
| `practice-test.html` | 10-question sample quiz (same engine as the Saudi page), 3 options each, English + Urdu toggle; dual-gate label verbatim in the lead: *"Practice format based on the official DKT structure: 45 questions, pass both sections — 12/15 General Knowledge and 29/30 Road Safety"* |
| `signs.html` | 120-sign gallery in 6 category sections (Warning 48 · Regulatory 45 · Guide 16 · Temporary 6 · Priority 3 · Hazard 2), English/Urdu name-and-meaning toggle, images from `assets/signs_nsw/` |
| `fees-and-guide.html` | 9-step licence guide, dual-pass fmtbox with the full honesty label, Service NSW fee table (DKT $58 · learner $32 · HPT $58 · driving test $72; 1 July 2026 schedule), eligibility, L/P conditions, demerit points, HPT explainer, 120-hour log book, Academy note, quick questions, not-affiliated note |

Key stats used throughout: **420 questions · 120 signs · 4 languages** (English default; Arabic full translation; Urdu + Bengali study-aid) · **3 options** per question · DKT **45 questions, dual pass 12/15 GK + 29/30 RS, untimed** · age **16** (enrol 15y 11m) · **120-hour logbook incl. 10 night hours** · HPT 15 clips.

## Also changed

- **Navigation:** 'Australia' group (Saudi single-country pattern; stats "420 Questions · 120 Signs · 4 Languages"; links: New South Wales Test / Practice Test / Traffic Signs / Fees & Guide) added to **all 40 pages**, inserted between the Saudi Arabia and USA groups. Existing groups and accordions untouched — verified by diff: existing pages are byte-identical to v15 once the inserted block is removed.
- **Homepage (`index.html`):** new "🇦🇺 New South Wales pack — free practice online" section after the Saudi Arabia section, mirroring its 4-card layout.
- **`sitemap.xml`:** +4 URLs → **40 total**.
- **Assets:** 120 NSW sign PNGs copied to `assets/signs_nsw/`.
- NSW pages carry correct `../../` relative links, Australia nav toggle + current-page link marked active, and NSW canonical/OG URLs (`https://licenseace.com/australia/new-south-wales/…`).

## Sample questions (practice page)

10 questions taken verbatim from `nsw_questions.json`: NSS001, NSS004, NSS049 (Signs — Priority/Regulatory/Warning, with sign images), NSR001, NSR002 (Rules GK), NSR090, NSR091 (Rules RS), NSA001, NSA002, NSA003 (Safety).

## Verification results — ALL PASS

- **Internal links:** every `href`/`src` in the 4 new pages resolves to a real file — 0 broken.
- **Nav:** Australia group present exactly once on all **40/40** pages.
- **Sitemap:** exactly **40** `<loc>` entries; every URL resolves to a real file.
- **Sample questions:** all 10 match `nsw_questions.json` field-for-field in order (question, Urdu question, options, Urdu options, correct index, explanation, Urdu explanation, topic, sign image) — correct answers verified.
- **Signs:** 120 image references on `signs.html`, all 120 unique, all pointing to existing files in `assets/signs_nsw/`; 120 sign cards rendered.
- **Labels:** dual-gate honest label present verbatim on the overview and practice pages; FAQ JSON-LD parses (6 questions).
- **Cleanliness:** no leftover placeholders, no Saudi content in NSW page bodies, no unprefixed root links.

**Not pushed** — git/GitHub push is the user's step (follow the v15 `PUSH_GUIDE.md` flow with the v16 folder contents).
