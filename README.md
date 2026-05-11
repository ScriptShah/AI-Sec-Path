# 🛡️ AI Journey Tracker

A focused PWA to track your 26-week journey through Phase 1A of the AI Security roadmap. Pomodoro timer, weekly tasks, streak tracking, notes — all offline-capable, installable on iOS and Android.

![icon](./icon-192.png)

## Features

- ⏱️ **Pomodoro timer** — 25/5 default, customizable
- ✅ **Weekly tasks** — pre-loaded from your roadmap, editable
- 🔥 **Streak counter** — daily consistency tracking
- 📊 **Stats** — hours this week, total hours, sessions completed
- 📝 **Notes per week** — auto-saved journal
- 🌓 **Dark / light mode**
- 📱 **Installable PWA** — works offline, lives on your home screen
- 💾 **All data local** — nothing leaves your device

## Deploy to Vercel

### Option 1 — fastest (drag & drop)

1. Go to [vercel.com/new](https://vercel.com/new)
2. Drag this entire folder onto the page
3. Click **Deploy**
4. Done. You'll get a URL like `ai-journey-tracker.vercel.app`

### Option 2 — via CLI

```bash
npm i -g vercel
cd ai-journey-tracker
vercel
```

Follow the prompts. Accept defaults.

### Option 3 — GitHub + Vercel (recommended for long-term)

```bash
cd ai-journey-tracker
git init
git add .
git commit -m "Initial commit"
gh repo create ai-journey-tracker --public --source=. --push
```

Then on Vercel: **New Project → Import** the GitHub repo. Future `git push` deploys automatically.

## Install on your phone

Once deployed, open the Vercel URL on your phone:

### iPhone (Safari only — Chrome won't work for install)
1. Tap the **Share** button (square with arrow)
2. Scroll down and tap **Add to Home Screen**
3. Tap **Add**
4. The app will appear on your home screen like a native app

### Android (Chrome)
1. Tap the **⋮** menu (top right)
2. Tap **Install app** or **Add to Home screen**
3. Done — it lives in your app drawer

After install, the app works fully offline. Your data stays on the device — nothing syncs to a server.

## Customize

### Change the roadmap
Open `index.html`, find the `ROADMAP` constant near the top of the `<script>` block. Each week has `title`, `subtitle`, `topic`, and `tasks`. Edit freely.

### Change the colors
Edit the `:root` CSS variables at the top of `<style>`. The accent color (`--accent: #E8B547`) controls all amber highlights.

### Change the fonts
Edit the Google Fonts `<link>` tag in `<head>` and the `--serif`, `--sans`, `--mono` CSS variables.

## Files

```
ai-journey-tracker/
├── index.html              # Main app (HTML + CSS + JS)
├── manifest.json           # PWA manifest (install metadata)
├── sw.js                   # Service worker (offline support)
├── icon-192.png            # PWA icon
├── icon-512.png            # PWA icon (large)
├── icon-maskable-512.png   # Android adaptive icon
├── favicon.png             # Browser tab icon
├── vercel.json             # Deploy config (cache headers)
└── README.md               # This file
```

## Reset / backup

- **Reset all data:** Open Settings → "Reset all data"
- **Backup data:** Open browser dev tools → Application → Local Storage → copy the value of `ai_journey_v1`. Paste somewhere safe.
- **Restore data:** Same place, paste the value back into `ai_journey_v1`.

## Privacy

- No analytics, no tracking, no servers, no cookies
- All data lives in your browser's `localStorage`
- The app fetches Google Fonts on first load — that's the only external request

---

Built for someone serious about a 36-month commitment. **Re-read the roadmap reminders monthly.**

🎯 Every day counts.
