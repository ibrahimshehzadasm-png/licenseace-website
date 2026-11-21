# Website v24 patch — 'Coming soon' safai (21 Nov 2026)

## Base
Live repo ki current halat (v23 shamil) — clone par v23 laga kar banaya gaya. Menu ko is patch me **haath hi nahi lagaya** (user ki shart: main menu isi tarteeb se rahe) — diff se verify hai ke nav har file me byte-identical hai.

## Kya khatam hua (232 jagah, 57 files)
- **Har page ke footer ka neela 'Countries & Roadmap' card** (roadmap ke neeche wala hissa): Texas / New York / Florida / Illinois ke agay se '— coming soon' khatam — ab sirf naam reh gaye (Punjab — v1.0, UK — v1.1, California — v1.2 waisa hi).
- **Homepage ka Roadmap section:** unhi chaar entries se '— coming soon' khatam.

## Kya NAHI chhua (user ki hidayat ke mutabiq)
- **App wale 'Coming soon to Google Play' badges** — tamam pack pages aur homepage par waisay ke waisay (ye app ke launch ki baat hai, user ne inhen rehne ko kaha).
- Main menu / pillnav — ek harf nahi badla.
- Sitemap, articles, content — sab waisa hi.

## Diff verify
Tamam 57 files ka line-by-line diff: tabdeel shuda lines sirf foot-road wali line aur homepage ki roadmap step line hen. Unexpected tabdeeli: **0**.

## Push steps
1. Zip ki files repo me usi structure se copy karen (overwrite).
2. `cd C:\projects\licenseace\licenseace-website`
3. `git add -A` → `git commit -m "Website v24 - Remove coming soon from roadmaps"` → `git push`
