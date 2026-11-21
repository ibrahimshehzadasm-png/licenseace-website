# Website v22 patch — Articles menu link + Articles index fixes (21 Nov 2026)

## User ki teen shikayaten, teen fix
1. **Main menu me Articles nahi tha** — homepage par 'Articles' lafz 0 dafa tha; pillnav me sirf Home + country groups thay. **Fix:** tamam 51 pages ke pillnav me Home ke foran bad **Articles** ka link jod diya (homepage, tamam country pages, Australia ke 12 sub-pages). Har file me sirf 1 insertion, verify shuda.
2. **Articles index ka hissa theek** — counter ab **"2 Articles published"** (ye fix is patch me pakka shamil hai; pichli dafa wali file se azad).
3. **Coming Soon khatam** — 'Next: Hazard Perception' wala teaser card Articles index se hata diya.
4. **Neela card durust** — neeche wala blue CTA card sirf UK ki taraf ishara karta tha; ab dono taraf: **Punjab Practice** (primary) + **UK Practice Test**, aur matan me dono formats (Punjab e-sign 10 sawal/5 pass, UK 40 sawal).

## Patch me kya hai (51 files)
- Repo root ki tamam HTML files (har ek me sirf pillnav ki 1 line ka izafa)
- `australia/` ke 12 pages (../../ wala sahi rasta)
- `articles/index.html` (counter + Coming Soon khatam + neela card)

## Shamil NAHI (wajah ke sath)
- **Qatar ke 4 pages** — ye files user ne khud jodi thin, in ki copies assistant ke pas nahi; in ke menu me Articles link is patch se nahi jure ga. Chahen to un par bhi yehi 1-line pattern lag jayega.
- Dono article pages — un ke header me Articles ka button pehle se mojood hai.

## Push steps
1. Zip khol kar tamam files repo me **usi structure** se copy karen (root wali root me, australia wali australia me, articles wali articles me) — overwrite.
2. `cd C:\projects\licenseace\licenseace-website`
3. `git add -A` → `git commit -m "Website v22 - Articles in main menu, index fixes"` → `git push`
4. Push ke bad batayen — live verify kar dunga (menu link, counter 2, Coming Soon gayeb, neela card).
