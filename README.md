# GameSpark — PWA Deployment Guide

## Files in this folder
- `index.html` — the app
- `manifest.json` — makes it installable as a mobile app
- `sw.js` — service worker (allows offline use)
- `icons/` — place your app icons here (see below)

---

## Step 1 — Add app icons
You need two icon images in the `icons/` folder:
- `icon-192.png` (192×192 pixels)
- `icon-512.png` (512×512 pixels)

**Free icon tools:**
- https://favicon.io — type text like "GS", pick colours, download
- https://realfavicongenerator.net — upload any image, it generates all sizes

---

## Step 2 — Host on GitHub Pages (free)

1. Go to https://github.com and create a free account
2. Click **New repository** — name it `gamespark`
3. Upload all files from this folder (drag and drop)
4. Go to **Settings → Pages**
5. Under "Source" select **main branch**, click Save
6. Your app is live at: `https://YOUR-USERNAME.github.io/gamespark`

---

## Step 3 — Install on phone

### Android (Chrome)
1. Open the URL in Chrome
2. Tap the three-dot menu → **Add to Home screen**
3. Tap **Install** on the banner if it appears

### iPhone (Safari)
1. Open the URL in Safari (must be Safari, not Chrome)
2. Tap the **Share** button (box with arrow)
3. Scroll down → tap **Add to Home Screen**
4. Tap **Add**

The app will now appear on your home screen like any other app!

---

## What makes this a PWA?
- `manifest.json` — gives the app a name, icon, and standalone display
- `sw.js` — caches the app so it works offline
- `<meta name="apple-mobile-web-app-capable">` — enables full-screen on iPhone
- `localStorage` — saves your ideas between sessions

---

## Customising for your students
Open `index.html` and find these arrays near the top of the `<script>` section:

```js
const genres   = ["Platformer","Puzzle", ...]
const settings = ["Underwater City","Space Station", ...]
const mechanics= ["collect coins","swap gravity", ...]
const twists   = ["but you're tiny","but everything is on fire", ...]
```

Students can change these to anything they like — their own genres, favourite games, inside jokes — and redeploy their personalised version!
