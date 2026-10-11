# TikTok Studio (Termux starter)

Mobile-first local dashboard with overview, analytics, curated general-audience video ideas, search, persistent drafts, and a caption preparation page.

## Run on Android / Termux

```bash
pkg update
pkg install git nodejs
git clone https://github.com/drakenfr10/tiktok-studio.git
cd tiktok-studio
npm install
npm start
```

Open http://localhost:3000 in your phone browser.

## Limitations

This is a local dashboard starter, not an official TikTok client. It does not publish videos or fetch live TikTok views, comments, or individual liker identities. Those require supported, authorized APIs and any necessary app review. Trending ideas are curated examples, not live rankings. Drafts are stored locally in `studio-data.json`. The server binds to `127.0.0.1` by default; do not expose it publicly without authentication and security controls.
