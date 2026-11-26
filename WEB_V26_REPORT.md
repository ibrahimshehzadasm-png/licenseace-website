# Website v26 patch — Article 3: L-Shape Driving Test (25 Nov 2026)

## Research pehle hua
Competitor sites (signtest.pk, tigertest.io, sumartech/LaneWise, thelicensedesk.com, theorymock.co.uk) ko deeply parh kar un ke titles/headings/FAQ se keywords nikale gaye. Sab se bara khala (gap): **L-shape practical test** — SignTest is par guide + simulator + video, teen cheezen chala raha hai; hamari site par is ka zikr tak nahi tha. Article 3 isi keyword par hai: `L-shape driving test Pakistan`.

## Naya article
**articles/punjab-l-shape-driving-test.html** — "How to Pass the L-Shape Driving Test in Pakistan: Technique & Tips"
- Sections: test kya hai aur kahan fit hota hai (42 din + e-sign ke bad) · test ka poora tareeqa (forward, phir reverse, ek correction ki ijazat) · seat/belt/mirror setup · forward run · reverse run ki technique (corner par full lock hold) · fail karne wali 5 ghaltiyan · motorcycle figure-8 · practice ka tareeqa · 4 FAQ (apni FAQ schema ke sath)
- Facts ki hifazat: tamam buniyadi baten kai sources se milti hain (PakWheels ki test-centre recording samet). Track ki exact lambai sources me mukhtalif thi, is liye article me sirf "aam tor par ~10 feet chora corridor, layout centre ke hisab se badal sakta hai" likha hai — koi ghair-mustanad number dawa nahi kiya.
- Article ki apni canonical, og tags aur FAQ JSON-LD schema — UK article ki koi cheez is me nahi ayi (verify shuda).

## Sath ki tabdeelian
- **articles/index.html:** counter 2 → 3, naya card sab se upar (Punjab Practical). Diff sirf yehi do cheezen.
- **sitemap.xml:** naya URL shamil — kul **58 URLs**; articles index ki lastmod 25 Nov.

## Base ki hifazat
Patch **live repo ki taaza halat (HEAD 35b69e9)** par bana hai — is me wo KeyMind privacy page wala commit bhi shamil hai jo isi darmiyan push hua tha. Qatar samet kisi page ko haath nahi laga.

## Push steps
1. Zip ki files repo me usi structure se copy karen (overwrite).
2. `cd C:\projects\licenseace\licenseace-website`
3. `git add -A` → `git commit -m "Website v26 - Article 3: L-Shape driving test"` → `git push`
4. Push ke bad batayen — live verify karunga. Phir Search Console me naye article ki **Request Indexing** karna faida de gi (wo aap ke account se hota hai, steps de dunga).
