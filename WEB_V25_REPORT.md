# Website v25 patch — GA4 + neela pill chokor + article cards fix (22 Nov 2026)

## Base
GitHub se **fresh clone** (HEAD `8bd4a2d` — v24 wali live halat, Qatar shamil). Patch unhi asal files par bana hai.

## Teen tabdeelian (57 files)
1. **GA4 gtag (G-LWVHX8LW3M)** — tamam 57 pages ke `<head>` me Google tag ki 9 lines. Is se GA4 Realtime me live traffic nazar aye ga.
2. **Homepage Roadmap ka neela pill chokor** — `.step` ki border-radius 999px (gol) se **14px** kar di; ab tamam steps saaf chokor (rounded-rectangle) chips ki shakal me ayenge, neela 'live' wala bhi.
3. **Articles index ke cards** — `.grid .pcard-bot` ko column kar diya: heading upar moti, matan neeche seedhi rows me, phir date aur button. (Hub pages ki asal style ko haath nahi lagaya — override sirf articles page ke andar hai.)

## Qatar ki khaas hifazat (user ki hidayat)
- Qatar ke 4 pages ka diff khol kar verify kiya: **sirf 9 gtag lines judi hen, ek bhi line remove nahi hui** — content, menu, sab kuch bilkul waisa hi.
- Poore patch ki har file ka diff program se gin kar check kiya: manzoor-shuda tabdeelion ke ilawa koi tabdeeli nahi. Problems: **0**.
- Menu ki tarteeb ko is dafa bhi haath nahi lagaya.

## Push steps
1. Zip ki files repo me usi structure se copy karen (overwrite).
2. `cd C:\projects\licenseace\licenseace-website`
3. `git add -A` → `git commit -m "Website v25 - GA4 tag, roadmap pills rectangular, article cards fix"` → `git push`
4. Push ke bad batayen — live verify karunga: GA4 code live hai ya nahi (aur GA4 Realtime me pehla signal), Qatar pages salamat, pill chokor, cards durust.
