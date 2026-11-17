# LicenseAce Website v9 — Texas Web Set + USA Nav Update (17 Nov 2026)

**Push THIS v9 set — it supersedes v8 completely** (v8 is live; v9 contains
everything in v8 plus the Texas set and the nav/footer updates below).

## What v9 adds

1. **Four new Texas pages** (built from the verified Texas pack — DPS /
   Driver Handbook DL-7, Rev. Jan 2026):
   - `texas-driving-test.html` — hub: honest test-format box (30 questions,
     15 signs + 15 laws, 70% pass standard published in DL-7; DPS does not
     print the question count on its public pages), 6 FAQs with matching
     FAQ schema.
   - `texas-practice-test.html` — working 40-question quiz from the real
     Texas bank (14 sign questions with pictures), translations in Spanish,
     Urdu, Bengali and Arabic.
   - `texas-traffic-signs.html` — all **119** Texas signs with pictures,
     names and meanings in 5 languages (`assets/signs_tx/`, 119 PNGs).
   - `texas-license-fees-guide.html` — 6-step licence guide, the official
     10-row DPS fee table (Class C $33), teen GDL rules, adult driver
     education, Impact Texas Drivers, driving test, renewal, quick
     questions and the not-affiliated note.
2. **USA nav dropdown updated on all 20 pages**: stats line now reads
   *840 Questions · 293 Signs · 5 Languages* (California + Texas combined),
   and a **Texas** region block with its 4 links sits under California's.
3. **Homepage**: a **Texas Pack section** (mirroring the California Pack
   section) after the California section, and the meta description now
   ends "…Punjab, UK, California & Texas."
4. **Roadmap lines updated** (homepage roadmap + every page's footer):
   "🇺🇸 Texas, USA — coming soon" and "🇺🇸 New York & Florida, USA — later"
   replace the old "🇦🇪 UAE & more — later" line.
5. **Sitemap: 20 URLs** (4 Texas pages added, lastmod 2026-11-17).

Verified before delivery: AdSense script exactly once per page, all
internal links resolve, quiz data complete in 5 languages, gallery 119/119
images present, tag balance clean. **Article 2 (Hazard Perception) is
still NOT in this set** — it publishes in its own push, as planned.

## Push steps

1. Copy the **contents** of this `licenseace_website_v9` folder into your
   `licenseace-website` repo folder (overwrite everything it asks about).
2. ⚠️ Run the git commands **inside the `licenseace-website` folder**
   (not the app project root — that was the 16 Nov lesson):
   ```
   cd licenseace-website
   git add -A
   git commit -m "Texas web set + USA nav stats 840/293 + roadmap update"
   git push
   ```
3. Wait a minute for GitHub Pages to rebuild.

## Post-push live checks

- Open the four Texas pages:
  - https://licenseace.com/texas-driving-test.html
  - https://licenseace.com/texas-practice-test.html (answer 2–3 questions;
    a sign question must show its sign picture)
  - https://licenseace.com/texas-traffic-signs.html (switch the language
    select to Spanish — names/meanings must change)
  - https://licenseace.com/texas-license-fees-guide.html
- Check the nav USA dropdown on any page: stats line *840 · 293 · 5*,
  California links, then Texas links.
- Homepage: the 🇺🇸 Texas Pack section appears after the California Pack
  section; the footer roadmap shows Texas / New York & Florida (no UAE).
- Open https://licenseace.com/sitemap.xml — it must show **20** `<url>`
  entries.
- In Search Console, resubmit the sitemap with the **full URL**
  `https://licenseace.com/sitemap.xml`.
