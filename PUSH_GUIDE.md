# LicenseAce Website v13 — Accordion Nav (States Collapse) (18 Nov 2026)

**Push THIS v13 set — it supersedes v12 completely** (v12 is live; v13 contains
everything in v12 plus the one navigation change below — no content changes).

## What v13 changes

1. **Accordion dropdowns in the top nav (all 28 pages)** — the change the user
   asked for after seeing the live v12 USA menu, which listed every state with
   all its pages open and ran very long:
   - **USA dropdown**: the stats line (*1620 Questions · 518 Signs ·
     5 Languages*) stays at the top. Under it there are now only the four
     **state names — California, Texas, New York, Florida — each with a ▾
     arrow**, all collapsed. Clicking a state name expands it to show that
     state's 4 pages (Test / Practice Test / Traffic Signs / License Fees
     Guide) and rotates the arrow; clicking it again collapses it. Opening
     one state closes the others (one open at a time).
   - **Pakistan dropdown**: the same pattern — a single **Punjab** row with
     a ▾ arrow; click to expand its 4 pages.
   - **UK dropdown**: unchanged — the UK has one national test, so its 4
     pages are still listed directly, exactly as in v12.
   - The expanded page links are **identical in text and URL to v12** — only
     the markup around them changed. Works with mouse, touch and keyboard
     (real `<button>` rows with `aria-expanded`).
2. **Nothing else changed**: page content, stats, Urdu sizes (`.ur` 1.35em,
   quiz Urdu 20px/22px), AdSense (once per page), footer roadmap (only
   "🇺🇸 Illinois (Chicago), USA — later" remaining) and the sitemap
   (**28 URLs**) are all exactly as in v12. Verified mechanically: removing
   the accordion markup/CSS/JS from v13 reproduces v12 byte-for-byte on all
   28 pages, and a scripted click test confirmed expand / collapse /
   one-at-a-time behaviour on the homepage, a state page and an articles
   page.

## Push steps

1. Copy the **contents** of this `licenseace_website_v13` folder into your
   `licenseace-website` repo folder (overwrite everything it asks about).
2. ⚠️ Run the git commands **inside the `licenseace-website` folder**
   (not the app project root — that was the 16 Nov lesson):
   ```
   cd licenseace-website
   git add -A
   git commit -m "Accordion nav: states collapse with arrow, click to expand"
   git push
   ```
3. Wait a minute for GitHub Pages to rebuild.

## Post-push live checks

- Open https://licenseace.com/ and open the **USA** menu: you should see
  only the stats line and the four state names with ▾ arrows — no page
  links until you click a state. Click **Texas**: its 4 links appear and
  the arrow flips; click **Florida**: Texas closes and Florida opens.
- Open the **Pakistan** menu: one **Punjab** row with an arrow; click it —
  the 4 Punjab pages appear. The **UK** menu still lists its 4 pages
  directly.
- Spot-check on a phone (or narrow window): the menus still open, and the
  state rows tap-expand the same way.
- Open any state page (e.g. https://licenseace.com/florida-driving-test.html)
  and https://licenseace.com/articles/ — the nav behaves the same there.
- Sitemap is unchanged (28 URLs) — no Search Console resubmission is
  required for this push, though resubmitting does no harm.
