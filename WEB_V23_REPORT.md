# Website v23 patch — Articles menu link (SAHI base par) + Articles index fixes (21 Nov 2026)

## Is dafa buniyad mukammal mukhtalif hai
Ye patch purani local copies par NAHI bana. Assistant ne pehle GitHub se repo ki **current halat clone** ki (HEAD `e3bd8fa` — 'Restore Qatar menus' wali halat, jis me Qatar menus + Article 2 + counter 2 sab mojood thay), phir patch unhi asal files par banaya.

## Har file ka diff check (v22 wali ghalti ka paband hal)
Patch ki har nav file ka base se diff gin kar verify kiya gaya: **har file me sirf +1 line** (Articles wala link) — is ke ilawa ek harf bhi idhar udhar nahi. BAD diffs: **0**.

## Patch me kya hai (55 files)
1. **Articles link tamam menus me** — repo root ke 42 pages (**Qatar ke 4 pages shamil**) + Australia ke 12 pages: pillnav me Home ke foran bad 'Articles'.
2. **articles/index.html** — Coming Soon card khatam; neela CTA card durust (Punjab Practice primary + UK Practice); counter pehle se 2 tha, waisa hi rakha.

## Shamil nahi
- Dono article pages (un ke header me Articles ka button pehle se hai; un ka layout mukhtalif hai).
- Sitemap — koi tabdeeli nahi (57 URLs waisi ki waisi).

## Push steps
1. Zip ki files repo me usi structure se copy karen (overwrite).
2. `cd C:\projects\licenseace\licenseace-website`
3. `git add -A` → `git commit -m "Website v23 - Articles in main menu (on restored base), index fixes"` → `git push`
4. Push ke bad batayen — live verify kar dunga: menu me Articles + Qatar dono, counter 2, Coming Soon gayeb.
