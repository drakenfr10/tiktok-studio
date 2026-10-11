# Clipwonk Studio

A mobile-first, local creator workspace for clipping workflows, designed to run on a phone with Termux or on a personal computer.

## Features
- Multi-file video uploads (up to 10 files per batch, 500 MB per file)
- Local video library with in-browser previews and downloads
- Caption Lab with hook starters, saved drafts, copy-to-clipboard and CTA/hashtag helper
- Content planner / queue with dates and notes
- Local workflow analytics (uploaded videos, draft count, queue count, local storage size)
- Curated general-audience idea prompts with search and links to TikTok Creative Center and Google Trends
- Responsive desktop sidebar and mobile bottom navigation
- Health endpoint at `/health`

## Run in Termux
```bash
pkg update
pkg install git nodejs
git clone https://github.com/drakenfr10/tiktok-studio.git
cd tiktok-studio
npm install
npm run check
npm start
``
Open `http://localhost:3000` in the phone browser.

If you already cloned the repository, update it first:
```bash
git pull
npm install
npm run check
npm start
``

## Storage and limits
- Videos are stored in `uploads/`; workspace data is stored in `studio-data.json`.
- Both are local and should not be committed or publicly hosted.
- Each upload is limited to 500 MB and 10 files per batch. Actual available storage depends on your device.
- By default the server binds to `127.0.0.1`, so it is only reachable from the same device. Set `HOST=0.0.0.0` only if you understand the network exposure and add authentication/firewall controls.

## Important limitations
This is a local workflow dashboard, not an official TikTok integration. It does **not** upload or publish videos to TikTok, schedule posts on TikTok, or fetch real TikTok views, comments, followers or liker identities. Those features require supported TikTok developer APIs, app approval, OAuth, and the relevant permissions. The analytics shown here are local workspace statistics only.

## Safety
Do not expose this app directly to the public internet without authentication and upload controls. Keep personal videos and `studio-data.json` private.
