# Website v27 patch — AdSense 'Low value content' fix batch (26 Nov 2026)

AdSense Sites page ki asal wajah **'Low value content'** thi — ye batch usi ka jawab hai: site par gehra, asal content barhana.

## Is batch me kya hai (60 HTML files + sitemap)
1. **Article 4 — 'Hazard Perception, Explained'** (articles/hazard-perception-explained.html): 15 Nov wala tayyar draft current theme me port kiya. Facts GOV.UK/DVSA ke mutabiq dobara verify (50 sawal/57 min/43 pass, hazard 14 clips/15 hazards/44 of 75, £23, certificate 2 saal). Apni canonical, og tags aur FAQ schema ke sath.
2. **Naya About page** (about.html): LicenseAce kya hai, content kese banta hai (har bank official authority se check), bilkul free + no-backend wali baat, aur contact support@licenseace.com. Reviewers ke liye ye trust page lazmi hota hai.
3. **Har page ke footer me About ka link** — 58 pages me Privacy Policy ke bilkul bad sirf **ek line** judi hai (har file ka diff verify shuda). Sirf keymind-privacy.html is se bahir hai (us ka footer alag saakht ka hai; use haath nahi lagaya).
4. **13 practice pages par asal guide section** — har region ke apne verified bank ke sath (Punjab 480, UK 730, baqi 420/360): sawalat kese bane, tayyari ka tareeqa, signs/fees pages ke links. Ek bhi line remove nahi hui, sirf izafa hai.
5. **Articles index:** counter 3 → 4, hazard card sab se upar.
6. **Sitemap: 60 URLs** (hazard article + about page shamil).

## Qatar ki hifazat
Qatar ke pages ka diff khol kar dekha: **sirf footer wali ek About line** judi hai, is ke ilawa kuch nahi badla.

## Push steps
1. Zip ki files repo me usi structure se copy karen (overwrite) — is dafa files zyada hen (60), sab copy karni hen.
2. `cd C:\projects\licenseace\licenseace-website`
3. `git pull --no-edit` (agar repo peeche ho to pehle ye)
4. `git add -A` → `git commit -m "Website v27 - AdSense fix: hazard article, about page, practice guides"` → `git push`
5. Push ke bad batayen — live verify karunga (Article 4, About page, counter 4, sitemap 60).

## Push ke bad (mere zimme yad-dihani)
- Hazard article ki Search Console me Request Indexing (L-Shape wala tareeqa).
- **Phir** AdSense Sites page se **Request review** — lekin pehle ye batch live ho, tab hi review mangna hai; bina tabdeeli ke review bekaar hota hai.
