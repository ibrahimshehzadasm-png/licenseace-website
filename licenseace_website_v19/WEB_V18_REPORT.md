# LicenseAce Website v18 — Build Report (Queensland Web Set + Translation Fixes)

**Built:** 20 Nov 2026 · **Base:** `licenseace_website_v17/` copied to a new real folder `licenseace_website_v18/` (v17 left pristine — re-verified MD5-identical to `licenseace_website_v17.zip` after the build; the only extra file in v17 is its own `VIC_WEB_REPORT.md`, which was added after that zip was made)
**Deliverables:** this folder + `licenseace_website_v18.zip` (1,520 entries, 48 HTML pages, CRC clean, 45,469,691 bytes; this report was written after zipping, mirroring the v17 arrangement, so it is in the folder but not in the zip)
**Facts used only from:** `licenseace_australia/qld_pack_foundation.md`, `qld_guide_fees.md` (incl. the verbatim simulator honesty labels), `qld_questions.json`, `qld_signs_gallery.json`, `signs_qld/` PNGs, and the app banks `licenseace_gulf/sa_questions.json`, `licenseace_australia/nsw_questions.json`, `vic_questions.json` for the Arabic additions.

## Part A — Queensland web set (4 new pages, mirroring the VIC set page-for-page)

| Page | Contents |
|---|---|
| `australia/queensland/index.html` | Overview: hero (420 · 127 · 4 · **9 + 18** written-test pass), format box covering **both routes** — PrepL online course (30 questions, pass 27/30, no section gates, enrol 15y 11m, 12 months, free retakes after 24h) and the written test (30 questions in 2 sections: 10 giving way ≥9 + 20 road rules ≥18, both sections must pass) — with the honesty label **verbatim** in English + Urdu (`.ur`, Jameel Noori), an explicit "the real test is English only; Arabic/Urdu/Bengali are study aids" paragraph, 4 pack cards, app CTA, 6-question FAQ + matching FAQPage JSON-LD (verified to parse and match the body FAQ exactly) |
| `australia/queensland/practice-test.html` | 10-question sample quiz (same engine as the VIC page): QLS001 (P01 Stop), QLS004 (R01), QLS049 (W01), QLR060 (GW), QLR011 (the dual-gate signature question: 27/30 but GW 8/10 = fail), QLA035 (floodway, Q01 image), QLR063 (GW roundabout), QLR029 (100-hour logbook), QLA057 (cane train, Q02 image), QLR004 (PrepL format). **3 of the 10 are GW-tagged.** Every field verified **field-for-field** against `qld_questions.json` in EN + AR + UR (question, options, correct index, explanations, topic, sign image). LANGMAP has `ar` + `ur`, **default `none`** (English first, translations on toggle). The lead carries the full dual-gate honesty label plus the PrepL 27/30 difference and the English-only note |
| `australia/queensland/signs.html` | All **127 signs** generated from `qld_signs_gallery.json` in 6 sections (Warning 51 · Regulatory 49 · Guide 16 · Temporary 6 · Priority 3 · Hazard 2), EN/UR name-and-meaning toggle (same mechanism as the VIC page), images from `assets/signs_qld/` — including the 3 Queensland-specific signs Q01 Floodway, Q02 Cane Train Crossing, Q03 Stock Grid (last in the Warning section). Every card's EN/UR name and meaning verified against the gallery JSON |
| `australia/queensland/fees-and-guide.html` | 8-step licence guide (both test routes → learner licence → supervision → logbook → HPT → Q-SAFE practical → P1/P2 → open), format box with the honesty label, TMR fee table (PrepL $29.70 one fee · written test $29.70/attempt · learner licence $80.15/3 years · HPT $42.70 · practical $69.40; FY 2026-27), eligibility + interpreter arrangements, learner conditions (zero BAC, under-25 total phone ban, L plates 14.6cm/20m/2 points, **no reduced learner speed limit**, school zones 40 km/h 7–9am & 2–4pm, no towing, P1 late-night passenger rule), demerit points (4 in 12 months = 3-month suspension), HPT explainer (25 clips, after 6 months), 100-hour logbook (10 night hours, trainer 3-for-1 up to 10→30, approval ≥12 business days before the test), a flooding section built on TMR's **"If it's flooded, forget it"**, Academy card list (Q-SAFE set), 5 quick questions, not-affiliated note. **Fee-whitelist scan: the only dollar amounts on any QLD page are $29.70 / $80.15 / $42.70 / $69.40** |

**Navigation:** the Australia accordion gained a **Queensland** entry (stats "420 Questions · 127 Signs · 4 Languages") on **all 48 pages**, inserted immediately after the Victoria block with the correct relative prefix per page location (root / `articles/` / state folders). NSW and VIC accordion entries are **byte-identical** to v17 on all 44 pre-existing pages (verified block-by-block). On the QLD pages themselves, the NSW block is byte-identical to the VIC pages' NSW block, the VIC block uses sibling `../victoria/` links, and the QLD block carries `class="active"` on the current page.
**Homepage:** new "🇦🇺 Queensland pack — free practice online" section immediately after the Victoria section, mirroring its 4-card layout (hub / practice / 127 signs / fees & guide). Removing the QLD nav block and the QLD section from the v18 homepage reproduces the v17 homepage **byte-for-byte** (verified).
**Sitemap:** +4 URLs → **48 total** (QLD entries lastmod 2026-11-20).
**Assets:** 127 QLD sign PNGs at `assets/signs_qld/`.

## Part B — Translation fixes (user-verified live defects)

1. **UK practice page default:** `uk-practice-test.html` was the only page on the site whose quiz defaulted to a translation (`let lang = 'ur'`). Changed to `let lang = 'none'`, and the dropdown's `selected` marker moved from the Urdu option to "English only" so the control matches the rendered default — together these are the entire default change; a byte-level check confirms the v18 UK page minus the inserted QLD nav block equals the v17 page with **only** that default change applied. English now shows first; Urdu (and BN/PL/AR/RO) remain on the toggle.
2. **Saudi practice page — Arabic added (40 questions):** every embedded question object gained `qa`/`oa`/`ea` fields taken from the matching question in `licenseace_gulf/sa_questions.json` (matched by exact English question text + options; **40/40 matched uniquely** — no Arabic was invented). LANGMAP gained `ar: {q: 'qa', o: 'oa', e: 'ea', rtl: true, urdu: false}` (the California page's entry shape — RTL, no Urdu font class), the language select gained **Arabic before Urdu**, and the intro/meta now read "…a translation underneath in Arabic or Urdu" / "in English, Arabic and Urdu".
3. **NSW + VIC practice pages — Arabic added (10 + 10 questions):** same treatment from `nsw_questions.json` / `vic_questions.json` (**10/10 matched uniquely** on each page; Arabic is a full test language in both banks). Arabic option added before Urdu; intros and meta descriptions updated to mention Arabic alongside Urdu.

**Arabic parity (all 70 fixed samples):** for every question, `qa`/`oa`/`ea` are non-empty and the digit sequences of EN and AR match exactly (question, every option, explanation) — **PASS**.

## Part C — Sweep of all 48 pages (post-build scan)

- **Defaults:** every quiz page on the site now defaults to `none` (English only): CA, FL, IL, NY, TX, Saudi, UK, NSW, VIC, QLD — **no non-Pakistan practice page defaults to Urdu (or any translation)**. Punjab/Pakistan pages carry no `langsel`/LANGMAP mechanism at all (static bilingual presentation — Urdu-first by design, untouched).
- **Urdu-only LANGMAPs:** none remain on non-Pakistan quiz pages (Saudi/NSW/VIC fixed above; USA pages already had ES/UR/BN/AR; UK already had UR/BN/PL/AR/RO; QLD built with AR+UR).
- **Observation (not changed — outside this build's scope):** the three **signs galleries** for Saudi Arabia, NSW and VIC still offer only an EN/UR name-and-meaning toggle, while the USA signs galleries offer five languages. The QLD signs gallery mirrors the VIC pattern (EN/UR). If Arabic sign names are wanted on those four galleries, the data already exists in the app banks' gallery JSONs — a small follow-up build.
- **Observation:** the homepage NSW/VIC section cards still describe their practice tests as "in English with an Urdu translation" — the practice pages themselves now offer Arabic too. Cosmetic wording only; left for a future tidy-up.

## Verification — 17/17 PASS

1. 48 HTML pages in the v18 folder.
2. `sitemap.xml` = exactly 48 `<loc>` entries, including the 4 Queensland URLs; every sitemap URL resolves to a real file.
3. Every internal `href`/`src` in all 48 pages resolves to a file in the folder — **0 broken**.
4. Arabic parity on all 70 fixed samples (non-empty + EN=AR digit parity) — PASS.
5. Defaults scan — no practice page defaults to a translation language (table of all 10 defaults, all `none`).
6. QLD samples field-for-field vs `qld_questions.json` (EN+AR+UR, correct index, topic, image) — PASS; 3 GW-tagged samples.
7. UK page diff = only the default change (byte-level reconstruction check) — PASS.
8. NSW/VIC accordion entries byte-identical to v17 on all 44 pre-existing pages — PASS.
9. The other 39 pre-existing pages differ from v17 **only** by the inserted QLD nav block (byte-level check) — PASS; homepage differs only by nav block + QLD section — PASS.
10. Arabic pages: all non-question diffs limited to the LANGMAP entry, the select option, the lead sentence and the two description strings — PASS.
11. QLD signs page: 127 cards in gallery order (51/49/16/6/3/2), all 127 images resolve — PASS; card data matches the gallery JSON — PASS.
12. QLD pages: nav blocks, active states and canonical/OG URLs correct — PASS.
13. QLD index FAQ JSON-LD parses and matches the body FAQ (6 questions) — PASS.
14. QLD practice page: LANGMAP `ar`+`ur`, default `none`, Arabic option present, honesty label in the lead — PASS.
15. v17 folder still pristine (MD5 vs `licenseace_website_v17.zip`) — PASS.

## ⚠️ Setup incident (resolved — no data lost)

The workspace sync had pre-created `your_files/licenseace_website_v18` as a **symlink into the v17 folder** (the same trap as the v17 build). The first copy commands therefore wrote an empty `australia/queensland/` folder and `assets/signs_qld/` into the v17 tree. This was caught before any page work: the two additions were removed, v17 was verified **MD5-identical to the pristine v17.zip** (1,368 files), and v18 was then set up the established way — a real folder at `goals/driveace-driving-test-prep-app/files/licenseace_website_v18` with the `your_files` symlink repointed to it. All build work happened in the real v18 folder, and check 15 above re-confirms v17 is untouched. The live site was never affected.

**Not pushed** — git/GitHub push is the user's step (follow the v17 `PUSH_GUIDE.md` flow with the v18 folder contents).
