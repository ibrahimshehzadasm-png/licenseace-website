# LicenseAce Website v12 — Florida Web Set + USA Nav Update (18 Nov 2026)

**Push THIS v12 set — it supersedes v11 completely** (v11 is live; v12 contains
everything in v11 plus the Florida pages and the nav/footer updates below).

## What v12 adds

1. **Four new Florida pages** (mirroring the New York pages exactly — same
   layout, CSS, nav, footer, AdSense once per page), built from the verified
   Florida pack (FLHSMV / Official Florida Driver License Handbook,
   rev. 08/2023):
   - `florida-driving-test.html` — hub: the honest test format (Class E
     Knowledge Exam, **50 questions, 40 to pass (80%)**; one form for every
     age; **no published time limit** — stated, never invented; and stated
     plainly: **the real exam is English only since 6 February 2026** — the
     site's translations are study aids) + 6 FAQs with matching FAQ schema.
   - `florida-practice-test.html` — working 40-question quiz drawn from the
     real 420-question Florida bank (Signs 14 with sign pictures / Rules 13 /
     Safety 13), translations in Spanish, Urdu, Bengali and Arabic, labelled
     as study aids.
   - `florida-traffic-signs.html` — all **120** Florida signs with pictures,
     names and meanings in 5 languages (`assets/signs_fl/`, 120 PNGs —
     including the corrected R7-8FL plaque, which reads only "FINE"; the
     unverified $250 figure appears nowhere in this set).
   - `florida-license-fees-guide.html` — 6-step licence guide, the official
     FLHSMV fee table (original Class E **$48** including the learner's
     licence, renewal $48, knowledge retest $10, skills retest $20,
     replacement $25, late fee $15, endorsements $7, ID card $25, and the
     $6.25 County Tax Collector service fee), DETS (under-18) / TLSAE (18+)
     courses, teen GDL rules (50 hours incl. 10 at night; curfews at 16 and
     17), the published skills-test manoeuvre list (parallel parking is NOT
     a Florida test manoeuvre), validity (8 years; 6 years over 79), quick
     questions and the not-affiliated-with-FLHSMV note.
2. **USA nav on all 28 pages**: the country → states menu keeps the grouped
   pattern — the USA dropdown now reads **1620 Questions · 518 Signs ·
   5 Languages** (California + Texas + New York + Florida), and a **Florida**
   region block with its 4 links sits under New York's block, so expanding
   USA shows each state with its pages beneath it.
3. **Homepage**: a **Florida Pack section** (mirroring the New York Pack
   section) after the New York section, and the meta description now ends
   "…Punjab, UK, California, Texas, New York & Florida."
4. **Roadmap lines updated** (homepage roadmap + every page's footer):
   "🇺🇸 Florida, USA — coming soon" replaces "Florida — later", and the only
   remaining later line is "🇺🇸 Illinois (Chicago), USA — later".
5. **Urdu sizes unchanged from v11** (the bigger site-wide sizes: `.ur`
   1.35em, quiz Urdu 20px/22px) — the four new pages use the same sizes.
6. **Sitemap: 28 URLs** (4 Florida pages added, lastmod 2026-11-18).

Verified before delivery: AdSense script exactly once per page, all
internal links resolve, quiz data complete in 5 languages, gallery 120/120
images present, tag balance clean, no "$250" anywhere in the Florida pages.

## Push steps

1. Copy the **contents** of this `licenseace_website_v12` folder into your
   `licenseace-website` repo folder (overwrite everything it asks about).
   Make sure the new `assets\signs_fl` folder copies across with all
   120 PNG files inside it.
2. ⚠️ Run the git commands **inside the `licenseace-website` folder**
   (not the app project root — that was the 16 Nov lesson):
   ```
   cd licenseace-website
   git add -A
   git commit -m "Florida web set + USA nav stats 1620/518 + roadmap update"
   git push
   ```
3. Wait a minute for GitHub Pages to rebuild.

## Post-push live checks

- Open the four Florida pages:
  - https://licenseace.com/florida-driving-test.html — hero stats must read
    420 / 120 / 5 / 40/50, and the format box must state the English-only
    rule and the study-aid wording.
  - https://licenseace.com/florida-practice-test.html — answer 2–3
    questions; the first 14 are sign questions and must show the sign
    picture. Set the translation language to **Urdu** — translations appear
    in the bigger Jameel style (same sizes as the other packs).
  - https://licenseace.com/florida-traffic-signs.html — 120 sign cards;
    switch the language select to Spanish — names/meanings must change.
    Spot-check the R7-8FL card: its plaque must read only "FINE" (no $250).
  - https://licenseace.com/florida-license-fees-guide.html — the fee table
    must show $48 / $48 / $10 / $20 / $25 / $15 / $7 / $25 / $6.25.
- Check the nav USA dropdown on any page: stats line *1620 · 518 · 5*,
  California, Texas and New York blocks, then the Florida block with its
  4 links under it.
- Homepage: the 🇺🇸 Florida Pack section appears after the New York Pack
  section; the footer roadmap shows Florida — coming soon and only
  Illinois (Chicago) — later remaining.
- Open https://licenseace.com/sitemap.xml — it must show **28** `<url>`
  entries.
- In Search Console, resubmit the sitemap with the **full URL**
  `https://licenseace.com/sitemap.xml`.
