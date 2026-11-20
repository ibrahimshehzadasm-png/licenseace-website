# LicenseAce Website v14 — Illinois Web Set (18 Nov 2026)

**Push THIS v14 set — it supersedes v13 completely** (v13 is live with the
accordion nav; v14 contains everything in v13 plus the Illinois pack below —
the accordion nav is kept exactly as-is).

## What v14 adds

1. **4 new Illinois pages** (same layout/nav/footer as the Florida set,
   accordion nav included, AdSense once each):
   - `illinois-driving-test.html` — hub with the honest format box: written
     exam **35 questions / 28 to pass (80%)**, 15 sign questions + 20
     rules/safety, one threshold, **no published time limit**, format per
     **92 Ill. Adm. Code 1030.80** (the regulation is cited — the Rules of
     the Road handbook publishes no question count, and none is attributed
     to it). 6 FAQs with matching FAQ schema.
   - `illinois-practice-test.html` — 40-question quiz from the real Illinois
     bank: **Signs 14 (all with sign pictures) / Rules 13 / Safety 13**, all
     5 languages complete for every question, option and explanation.
     Spanish and Arabic are named Secretary of State test languages; Urdu
     and Bengali are labelled study aids.
   - `illinois-traffic-signs.html` — all **120 signs** with 5-language names
     and meanings (same language switcher); the 120 PNGs are in
     `assets/signs_il/`.
   - `illinois-license-fees-guide.html` — 6 steps + the full guide: the fee
     **age table** (instruction permit $20; licence 18–20 $5, 21–68 $30,
     69–80 $5, 81–86 $2, 87+ free) and every other verified fee row, GDL
     (50 hours incl. 10 at night; curfews), the Cooperative Driver Testing
     Program, 3 attempts per year, the 8-year written-exam repeat, and the
     published road-test manoeuvre list — with parallel parking explicitly
     **not** an Illinois road-test manoeuvre. Not-affiliated-with-SOS note
     included.
2. **Site-wide (all 32 pages)**:
   - USA nav stats → **2040 Questions · 638 Signs · 5 Languages**.
   - An **Illinois accordion row** (state name + ▾ arrow, collapsed) with its
     4 page links sits **under the Florida row** in the USA dropdown on
     every page; one state open at a time, exactly as before.
   - Homepage: an **Illinois Pack section** after the Florida section, and
     the meta description now ends “…New York, Florida & Illinois”.
   - Roadmap/footer: the “Illinois (Chicago), USA — later” line is **gone**
     everywhere; “Illinois, USA — coming soon” stands in its place. No
     “later” lines remain.
   - Urdu sizes unchanged (`.ur` 1.35em everywhere).
3. **Sitemap: 32 URLs** (the 4 Illinois pages added, lastmod 2026-11-18).

QA on this set: 24/24 checks pass — AdSense once on 32/32 pages, every
internal link resolves, href diff vs v13 is only the Illinois additions,
quiz 5-language completeness 40/40, gallery exactly 120 unique images on
disk, FAQ schema matches the visible FAQs word-for-word, all inline scripts
pass `node --check`, and jsdom smoke tests pass for the quiz (Q1 renders
`assets/signs_il/R1-1.png`, full run scores 40/40) and for the accordion
(Illinois row expands/collapses, one-at-a-time) on the homepage, the
Illinois hub and an articles page.

## Push steps

1. Copy the **contents** of this `licenseace_website_v14` folder into your
   `licenseace-website` repo folder (overwrite everything it asks about).
2. ⚠️ Run the git commands **inside the `licenseace-website` folder**
   (not the app project root — that was the 16 Nov lesson):
   ```
   cd licenseace-website
   git add -A
   git commit -m "Illinois web set + USA nav stats 2040/638 + accordion Illinois row"
   git push
   ```
3. Wait a minute for GitHub Pages to rebuild.

## Post-push live checks

- Open https://licenseace.com/illinois-driving-test.html — the hub loads
  with hero stats 420 / 120 / 5 / 28-of-35.
- Open the **USA** menu on any page: the stats line reads **2040 Questions ·
  638 Signs · 5 Languages**, and under Florida there is an **Illinois** row
  with a ▾ arrow. Click it — the 4 Illinois links appear and Florida (if
  open) closes.
- Try the practice test: https://licenseace.com/illinois-practice-test.html
  — Question 1 shows a stop-sign picture; switch the translation language
  to Urdu and the translation line appears under the question.
- Open https://licenseace.com/illinois-traffic-signs.html — 120 signs;
  switch the names & meanings language to check the switcher.
- Resubmit the sitemap in Search Console: https://licenseace.com/sitemap.xml
  (now **32 URLs**). The Console page count will lag behind again — that is
  the usual Google processing delay, not a problem with the push.
- Spot-check on a phone: menus open, the Illinois row tap-expands, and the
  quiz answers normally.
