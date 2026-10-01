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

## Cinematic v5
- First-visit intro ≈2.1 s (repeat visits ≈1.45 s, Reduce Motion ≈0.7 s), skippable (button / Esc / Enter / Space).
- Sound: original synthesised sound design (ambient drone, rising whoosh, electronic swell, sub impact, shimmer); no audio files or external URLs. Plays only after the browser allows audio.
- Spoken welcome uses the browser's SpeechSynthesis after a profile tap, once per selection. Toggle with the 🗣 button; stored as `dsa-grind-voice` (sound is `dsa-grind-sound`; both are separate from progress).
- The original profile is displayed as "Vishwas K" (one-time rename in the profile registry; progress data is not touched).
- Replace files in your repo root and push; Vercel redeploys. No build step, same architecture.

## v6 (final cinematic pass)
- Intro: ~6.8 s on first launch (dark ambience -> energy streak -> DSA GRIND emerges blurred->sharp with light rays -> pulse + light sweep -> subtitle -> fade to profiles). Repeat launches play it 1.8x faster (~4.2 s). Skip: button / Esc / Enter / Space (~0.4 s). Reduce Motion: ~1 s fade.
- Intro score is synthesised (Web Audio) on the same timeline: ambience, rising tone, whoosh + swell, sub impact at ~3.5 s, shimmer, fade. Plays only once the browser allows audio.
- Spoken welcome: "Welcome back, <Name>. Your DSA Grind continues. Day <N> is ready." / new profile: "Welcome to DSA Grind, <Name>. Your 100-day journey starts now." Name and day are read from the selected profile. Male English voice is chosen by scoring available voices (no hard-coded name); rate 0.92, pitch 0.82.
- Welcome screen has 🔊 VOICE ON/OFF and ▶ TEST VOICE ("Welcome back, <Name>."). The spoken sentence is also shown as a caption.
