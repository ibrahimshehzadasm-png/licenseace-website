# LicenseAce Website v11 — New York Web Set + Bigger Urdu Font (17 Nov 2026)

**Push THIS v11 set — it supersedes v10 completely** (v10 is live; v11 contains
everything in v10 plus the New York pages and the Urdu size increase below).

## What v11 adds

1. **Four new New York pages** (mirroring the Texas pages exactly — same layout,
   CSS, nav, footer, AdSense once per page):
   - `new-york-driving-test.html` — hub: the honest test format (20 questions;
     **dual pass rule** — at least 14/20 overall **AND** at least 2 of the 4
     road-sign questions; **no published time limit** — stated, never invented;
     questions from MV-21 Chapters 4–11 + the 'Road Signs You Must Know' chart;
     DMV office test in 20 languages) + 6 FAQs with matching FAQ schema.
   - `new-york-practice-test.html` — working 40-question quiz drawn from the
     real 360-question NY bank (Signs 14 with sign pictures / Rules 13 /
     Safety 13), all 5 languages complete for every question, option and
     explanation.
   - `new-york-traffic-signs.html` — gallery of **all 105 NY signs** with
     names and meanings in 5 languages; images in `assets/signs_ny/`
     (105 PNGs, new folder in this set).
   - `new-york-license-fees-guide.html` — classes/eligibility/permit steps,
     the full **age table** (7 rows, Standard vs MCTD — totals run
     **$64.25–$102.50**, never a single headline price), replacement $17.50,
     Enhanced +$30, the 5-hour pre-licensing course (MV-278), junior rules
     (6 months, 50 hours incl. 15 after sunset, MV-262, NYC/Long Island/
     Upstate regional note), parallel parking as a real NY road-test skill,
     licence valid 8 years, permit ~5 years, quick questions, and the
     not-affiliated-with-NY-DMV note.
2. **USA nav on all 24 pages**: stats line is now
   **1200 Questions · 398 Signs · 5 Languages** (CA 420 + TX 420 + NY 360;
   signs 174 + 119 + 105), with a New York region block (4 links) under Texas.
3. **Homepage**: a New York Pack section after the Texas Pack section, and the
   meta description now ends "…Punjab, UK, California, Texas & New York".
4. **Roadmap/footer**: New York is now present ("New York, USA — coming soon",
   the same wording Texas got in v9); only **Florida, USA — later** remains.
5. **Sitemap: 24 URLs** (the 4 NY pages added, lastmod 2026-11-17).
6. **Urdu font BIGGER — site-wide, all 24 pages (user note, 17 Nov 21:45)**:
   `.ur` block text **1.22em → 1.35em**; quiz-option Urdu **18px → 20px**;
   quiz question-translation Urdu **20px → 22px**. Line-heights unchanged.
   This is web only — the app keeps Noto Nastaliq as before.

## Push steps

1. Copy the **contents** of this `licenseace_website_v11` folder into your
   `licenseace-website` repo folder (overwrite everything it asks about).
   Make sure the new `assets\signs_ny` folder copies across with all
   105 PNG files inside it.
2. ⚠️ Run the git commands **inside the `licenseace-website` folder**
   (not the app project root — that was the 16 Nov lesson):
   ```
   cd licenseace-website
   git add -A
   git commit -m "New York web set + bigger Urdu font site-wide"
   git push
   ```
3. Wait a minute for GitHub Pages to rebuild.

## Post-push live checks

- Open https://licenseace.com/new-york-driving-test.html — hero stats must
  read 360 / 105 / 5 / 14/20, and the format box must show the dual pass rule.
- Open https://licenseace.com/new-york-practice-test.html — start the quiz;
  the first 14 questions are sign questions and must show the sign picture.
  Set the translation language to **Urdu**: the Urdu question line and the
  Urdu under each option must look **noticeably bigger** than before this
  push (that is the site-wide Urdu size increase — check it here first).
- Open https://licenseace.com/new-york-traffic-signs.html — 105 sign cards;
  set the language select to **Urdu**: names and meanings switch to Urdu in
  the bigger Jameel style. Spot-check one image directly, e.g.
  https://licenseace.com/assets/signs_ny/R1-1.png must load (not a 404).
- Open https://licenseace.com/new-york-license-fees-guide.html — the fee
  table must show all 7 age rows with Standard and MCTD columns
  ($80.00/$90.00 down to $64.25–$67.50/$73.25–$77.50), replacement $17.50
  and Enhanced +$30 — and **no single "New York price"** anywhere.
- Open https://licenseace.com/ — the New York Pack section sits after the
  Texas Pack section, and the USA menu stats read
  **1200 Questions · 398 Signs · 5 Languages** with a New York block.
- Check any older page (e.g. https://licenseace.com/punjab-practice-test.html)
  in Urdu — the bigger Urdu size applies there too (all 24 pages).
- **Resubmit the sitemap** in Google Search Console (Sitemaps →
  https://licenseace.com/sitemap.xml) — it now has **24 URLs**.
