# LicenseAce Website v10 — Jameel Noori Nastaleeq for Urdu on the Web (17 Nov 2026)

**Push THIS v10 set — it supersedes v9 completely** (v9 is live; v10 contains
everything in v9 plus the Urdu webfont change below — no content, page or
sitemap changes).

**User decision (17 Nov 2026):** Urdu on the **website** renders in
**Jameel Noori Nastaleeq**; the **app keeps Noto Nastaliq Urdu** (unchanged).

## What v10 changes

1. **New self-hosted webfont**: `assets/fonts/jameel-noori-nastaleeq.woff2`
   (5.5 MB — the same font file that was inspected and compared on
   17 Nov). Every page declares it with `@font-face` + `font-display: swap`,
   so Urdu first appears in the fallback and swaps to Jameel when loaded.
   Browsers only download it on pages where Urdu text is actually shown,
   and it is cached after the first download.
2. **Urdu font stack updated on all 20 pages**: Urdu text (quiz questions
   and options, sign names/meanings, Urdu lines) now uses
   `'Jameel Noori Nastaleeq','Noto Nastaliq Urdu',serif` — Jameel first,
   Noto as fallback. Until now the site named Noto but never loaded any
   Urdu webfont, so Urdu fell back to whatever the visitor's device had;
   now every visitor gets the same newspaper-style Nastaleeq.
3. **Size compensation**: Jameel renders about 30% smaller than Noto at the
   same size, so Urdu block text is set to `1.22em` and quiz-option Urdu to
   `18px` (was 15px). Line-heights unchanged (2.1 / 2).
4. Nothing else changes: same 20 pages, same sitemap (20 URLs), AdSense
   script still exactly once per page (verified). **Article 2 (Hazard
   Perception) is still NOT in this set** — it publishes in its own push.

## Push steps

1. Copy the **contents** of this `licenseace_website_v10` folder into your
   `licenseace-website` repo folder (overwrite everything it asks about).
   Make sure the new `assets\fonts` folder copies across with the
   `jameel-noori-nastaleeq.woff2` file inside it.
2. ⚠️ Run the git commands **inside the `licenseace-website` folder**
   (not the app project root — that was the 16 Nov lesson):
   ```
   cd licenseace-website
   git add -A
   git commit -m "Urdu webfont: Jameel Noori Nastaleeq (web only)"
   git push
   ```
3. Wait a minute for GitHub Pages to rebuild.

## Post-push live checks

- Open https://licenseace.com/punjab-practice-test.html — start the quiz;
  the Urdu question line and the Urdu under each option must appear in the
  slim newspaper-style Nastaleeq (clearly different from the old round
  Noto look). The first Urdu page on a fresh browser may take a few
  seconds to swap fonts while the 5.5 MB file downloads; after that it is
  cached and instant.
- Open https://licenseace.com/texas-traffic-signs.html (or the California
  one) — set the language select to **Urdu**: sign names and meanings must
  switch to Urdu in the same Jameel style, right-aligned.
- Open https://licenseace.com/uk-traffic-signs.html — Urdu sign names in
  Jameel.
- Direct font check: https://licenseace.com/assets/fonts/jameel-noori-nastaleeq.woff2
  must download (not a 404 page).
- No sitemap resubmission is needed for this push (no URL changes).
