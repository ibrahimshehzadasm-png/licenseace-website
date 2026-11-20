# LicenseAce Website v20 — Report

**Scope:** (A) the UAE web set — 4 new pages mirroring the Saudi Arabia set's structure, file layout and styling, built entirely from the verified UAE content package (`licenseace_gulf/uae_questions.json`, `uae_signs_gallery.json`, `uae_guide_fees.md`, `uae_guide_fees_translations.json`, U1 verification); (B) the user-ordered Australia label correction (WEB LABEL RULE: UK/USA/Australia label boxes print English only; Pakistan = Urdu; Saudi/UAE = Arabic).

**Base:** full copy of `licenseace_website_v19`. Symlink trap checked: `your_files/licenseace_website_v20` resolves to a NEW real folder (`goals/driveace-driving-test-prep-app/files/licenseace_website_v20`), not into v19. v19 was not written to — all 1,503 v19 files md5-verified pristine after the build.

## Part A — UAE pages added (4)

1. **uae-driving-test.html** — pack hub. Stats 420 questions · 150 signs · 6 languages · 30/40 pass (RTA Confirmed). Format box: Dubai Knowledge Test, RTA-confirmed **40 questions, 30 to pass, NO time limit** (RTA publishes none — simulator untimed), Abu Dhabi publishes no format, Sharjah 25Q/18/20 min with first attempt free. The honest label is printed in English with its **Arabic** translation underneath in `<span class="ar" lang="ar" dir="rtl">`, taken **verbatim** from `uae_guide_fees_translations.json` (`simulator_honesty_label.ar`, byte-compared equal). Closing line: "…in English with Arabic, Urdu, Hindi, Malayalam and Bengali translations." FAQ section + FAQPage JSON-LD (6 questions, all from the verified guide/U1 facts).
2. **uae-practice-test.html** — 40 sample questions drawn from `uae_questions.json` (14 Signs / 13 Rules / 13 Safety, evenly spaced per topic — the same selection pattern as the Saudi page). Quiz engine byte-identical to the Saudi page's; only the data, LANGMAP and one result message differ. Language toggle: English only (default `let lang = 'none'`) + **ar, ur, hi, bn, ml**; every translation string matched by exact English text against the bank (verified programmatically — nothing invented, no own machine translation). Sign images reference `assets/signs_uae/` (14 image refs, all resolve).
3. **uae-traffic-signs.html** — all **150 signs** with images (`assets/signs_uae/`, 150 PNGs copied from the content package), grouped Warning 52 / Regulatory 32 / Mandatory 14 / Guide 26 / Temporary 26. Names and meanings sit behind the same data-attribute language-toggle pattern as the Saudi gallery, extended to all six languages (en + ar/ur/hi/bn/ml data attributes on every card; toggle script identical to Saudi's). All card translations verified against `uae_signs_gallery.json`.
4. **uae-licence-fees-guide.html** — from `uae_guide_fees.md`: 6-step Dubai path, Knowledge Test format box, the 12-row fee table, One UAE/one licence, eligibility and ages (federal 17; **Dubai file at 17½, licence at 18**), validity/renewal, **Abu Dhabi — TAMM** (publishes **no test format** — stated honestly, no figures), **Sharjah — SDI** (25Q / 18 pass / 20 min, first attempt free, retake AED 50), rules taught, Academy note, quick questions, important note.

**Fee whitelist discipline:** only U1-whitelist figures appear — AED 220 (test, incl. Knowledge & Innovation fee), 420 (interpretation), 320 (earlier slot), 200 (file), 100 (permit), 50 (handbook), 140–180 (eye test), 300/100 (licence), 100 (Abu Dhabi booking), 50 (Sharjah retake). Deliberately NOT printed (present in the guide master but outside the whitelist): the licence-exchange totals (AED 1,050/600), Abu Dhabi's earlier-move AED 300, Abu Dhabi's AED 10/month renewal-delay fee, and the Instant Test line. Automated scan of all AED figures on the UAE pages confirms only whitelist values occur.

**Nav:** a UAE navgroup (420 Questions · 150 Signs · 6 Languages; UAE Test / Practice Test / Traffic Signs / Fees & Guide) was inserted immediately after the Saudi Arabia group on **all 48 existing pages** (root, `../` and `../../` prefixes respected) and is the active group on the 4 UAE pages. **Homepage:** a UAE pack section mirroring the Saudi section (hub / practice / signs / fees cards) was added after the Saudi section, before the Australia sections. **Sitemap:** +4 UAE URLs after the Saudi block (lastmod 2026-11-20), 48 → **52 URLs**.

## Part B — Australia label correction

On `australia/new-south-wales/index.html`, `australia/victoria/index.html` and `australia/queensland/index.html`, the static `<span class="ar" lang="ar" dir="rtl">…</span>` line that v19 added under the English honest label was **removed** — the label box now prints **English only**, per the WEB LABEL RULE. Nothing else on those pages changed: a strip-and-compare check proves each page equals v19 minus exactly that one line, plus the UAE nav insertion. The now-unused `.ar` CSS rule was **left in place** (per instructions: leave the CSS if unsure; it is harmless). No `class="ar"` remains anywhere on the three pages.

## Checks (31/31 PASS — 27 automated + 4 refined after manual review)

- Folder total **52 HTML pages**; sitemap **exactly 52 URLs** (unique), including the 4 UAE URLs.
- Internal link check across all 52 pages: **5,040 internal references, 0 broken** (files and `#anchors` both verified — `#fees`/`#steps` targets exist on the UAE guide page).
- **Diff discipline vs v19:** for every one of the 48 pre-existing pages, removing the inserted UAE navgroup from the v20 file reproduces the v19 file **byte-for-byte** — except the homepage (which additionally carries the UAE section; removing it also reproduces v19 byte-for-byte) and the 3 Australia index pages (which additionally lack exactly the one Arabic span line). Sitemap diff = only the 4 added UAE lines. Saudi/UK/USA/Pakistan pages are otherwise untouched.
- UAE practice page: default `let lang = 'none'` with "English only" selected; LANGMAP contains ar/ur/hi/bn/ml; 40 samples (14/13/13); **translations exact-match the bank** for every sample (question, options, explanation × 5 languages); **digit parity** EN = AR/UR/HI/BN/ML on every sampled string.
- UAE index label box: Arabic span **byte-equal** to `simulator_honesty_label.ar` in the translations JSON; `.ar` CSS present; stats 420/150/6 present.
- Signs page: 150 cards, 150 image refs all resolve, all name/meaning translations match the gallery JSON.
- **No Abu Dhabi format figures:** no 45/35/32 figure appears in any Abu Dhabi-attributed text on any UAE page. The only "35 questions"/"45 questions" strings on the site are distractor options inside one verbatim bank question ("How many questions are there in the Dubai Knowledge Test, as stated by the RTA?" — correct answer "40 questions").
- **No Dubai time limit stated:** all 8 "minutes" mentions on the UAE pages were classified — 6 are Sharjah's published 20 minutes (always attributed), 1 is "Arrive 30 minutes early" (official guide instruction), 1 is "A few minutes stopped…" inside a verbatim bank safety question. Zero time-limit claim patterns; zero Dubai+digit+minutes proximities.
- Quiz engine on the UAE practice page is identical to the Saudi page's (modulo data, LANGMAP, and the result message naming the Dubai Knowledge Test); signs toggle script identical to Saudi's.
- v19 verified pristine after the build (1,503 files, md5).

## Deliverables

- Folder: `licenseace_website_v20/` (this report inside it) — 1,658 files total (1,503 v19 files + 4 UAE pages + 150 sign PNGs + this report).
- Zip: `licenseace_website_v20.zip` — **the zip contains a top-level folder** `licenseace_website_v20/` (same arrangement as the v19 zip). 45,934,336 bytes · 1,659 entries (incl. the folder entry) · CRC clean.

**Push:** replace the site contents with the v20 folder's contents (copy from the unzipped `licenseace_website_v20/` folder, not from the zip's parent), commit e.g. "v20: UAE web set + Australia English-only labels". Sitemap grew to 52 URLs — the 4 new UAE URLs can be submitted to GSC with the sitemap.
