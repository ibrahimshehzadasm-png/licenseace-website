# LicenseAce Website v8 — Grouped Nav with Pack Stats + Meta Fix (16 Nov 2026)

**Push THIS v8 set — it supersedes v7 completely.** The v7 set was never
pushed (the live site is still the older set with the 12-URL sitemap), so do
**not** push v7 separately. One push of v8 brings the whole site current:
the full California web set, the new country-grouped navigation, and the
homepage meta fix.

## What v8 contains

Everything in v7 (v6 pages + Article 1 + the corrected sitemap + the full
California set: hub, 40-question practice test, 174-sign gallery, fees &
guide, homepage California section, sitemap at 16 URLs) — **plus**:

1. **New navigation on every page.** The flat country pills are replaced by
   three dropdown groups — **Pakistan ▾ · UK ▾ · USA ▾** — each opening with
   that pack's stats line, then its page links:
   - Pakistan: *480 Questions · 102 Signs · English / Urdu* → Punjab hub,
     Practice Test, Traffic Signs, Fees & Guide
   - UK: *730 Questions · 167 Signs · 6 Languages* → UK hub, Practice Test,
     Traffic Signs, Fees & Guide
   - USA: *420 Questions · 174 Signs · 5 Languages*, region label
     *California* → California hub, Practice Test, Traffic Signs,
     License Fees Guide
   Desktop: opens on hover or keyboard focus. Mobile/touch: tap the group
   name to open, tap a link to go, tap anywhere else to close. The group for
   the page you are on is highlighted blue. Home and Articles links are
   unchanged.
2. **Homepage meta description fixed.** It used to end "…Punjab & UK"; it now
   reads "Free driving licence test practice: verified question banks, mock
   tests, traffic signs and guides in your own language — Punjab, UK &
   California." (This is the line Google shows under the site name in search
   results.)

## Changed files vs v7 (17)

- **All 16 HTML pages** — header nav replaced with the grouped dropdown nav
  (plus one small CSS block and one small script at the end of each page;
  articles pages use the `../` paths, as their other links do).
- **`index.html`** — additionally: the meta description above.
- **`PUSH_GUIDE.md`** — this file (you can leave it out of the git copy;
  harmless either way).

Nothing else changed vs v7: sitemap (still 16 URLs), ads.txt, robots.txt,
CNAME, all page bodies and content, the quiz and gallery code, and the
AdSense script (still exactly once per page) are identical.
**Article 2 (Hazard Perception) is still NOT in this set** — it publishes
next week in its own push, as planned.

## Push steps

1. Copy the **contents** of this `licenseace_website_v8` folder into your
   `licenseace-website` repo folder (overwrite everything it asks about).
2. In the repo folder, the usual three commands:
   ```
   git add -A
   git commit -m "Grouped nav with pack stats + California web set + homepage meta fix"
   git push
   ```
3. Wait a minute for GitHub Pages to rebuild.

## Post-push live checks

- Open the four California pages (they are new to the live site):
  - https://licenseace.com/california-driving-test.html
  - https://licenseace.com/california-practice-test.html (answer 2–3
    questions; a sign question must show its sign picture)
  - https://licenseace.com/california-traffic-signs.html (switch the language
    select to Spanish — names/meanings must change)
  - https://licenseace.com/california-license-fees-guide.html
- Check the new nav on the homepage and on one inner page: three groups
  (Pakistan · UK · USA); each dropdown shows its stats line; on the
  California pages the **USA** group is highlighted. On your phone, tap a
  group name — the dropdown must open without the page scrolling sideways.
- Homepage: the 🇺🇸 California Pack section appears between the UK Pack
  section and the Roadmap.
- Open https://licenseace.com/sitemap.xml — it must show **16** `<url>`
  entries (the live one still shows 12 until this push lands).
- In Search Console, resubmit the sitemap with the **full URL**
  `https://licenseace.com/sitemap.xml` (bare `sitemap.xml` gives
  "Invalid sitemap address" on a domain property).
