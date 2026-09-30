# DSA GRIND — 100 Day Java + DSA (PWA)
Static site, no build step. Files: index.html, manifest.json, sw.js, icon-*.png, vercel.json.

## Deploy on Vercel
1. Put this folder in a GitHub repo (or run `npx vercel` inside the folder).
2. vercel.com → Add New → Project → import the repo → Framework: "Other" → Deploy.
3. Open https://<your-name>.vercel.app in Chrome → ⋮ → Add to Home screen / Install app.

## Deploy on GitHub Pages
1. Create a repo, upload all files to the root (index.html at top level).
2. Settings → Pages → Source: "Deploy from a branch" → main / (root) → Save.
3. Open https://<username>.github.io/<repo>/ → Chrome ⋮ → Install app.

## Notes
- Progress is stored in the browser (localStorage) per device and per URL. Keep using ONE URL.
- Use Settings → Export Progress once a week; hourly auto-backups are kept in the browser too.
- Certificate verification link: `<your-url>/#verify/CERT-XXXXXXX/Name/YYYY-MM-DD`.

## Profiles (v3)
- Up to 5 profiles; each has its own progress stored under `dsa-grind-p-<id>` (registry: `dsa-grind-profiles`).
- First load after this upgrade: your existing `dsa-grind-v1` data is COPIED to profile VISHWAS. The original key is left untouched as a safety copy.
- Export now contains all profiles; importing an all-profiles backup replaces all profiles (a safety copy is kept under `dsa-grind-prebackup`).
- Deleted profiles are kept once in `dsa-grind-trash` (last deletion only).

## Cinematic entry (v4)
- Intro (~2.3 s first visit, ~1.1 s afterwards, skippable, shorter with Reduce Motion) → profile screen → welcome → dashboard.
- Sounds are generated with Web Audio (no audio files, no external URLs) and only play after the first tap (browser autoplay rules). Toggle in Settings or the speaker button; the preference is saved separately from progress (`dsa-grind-sound`).
- Achievements already earned before this update are treated as seen, so they won't pop up again.
