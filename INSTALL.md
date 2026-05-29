# Anchor — Install Guide

Anchor is a **PWA (Progressive Web App)**. That means it installs to your phone's
home screen with its own icon, runs offline, and behaves like a real app — without
needing the App Store or Play Store, and without costing anything.

To install it, the files need to live on a web address (HTTPS). Below are two easy
routes. **Route A (Netlify Drop)** is the simplest — no account-coding, drag-and-drop,
about 2 minutes.

---

## What's in this folder

- `index.html` — the app itself
- `manifest.json` — tells the phone it's installable
- `sw.js` — service worker, makes it work offline
- `icon.svg`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` — app icons

Keep all of these together in the same folder. Don't rename them.

---

## Route A — Netlify Drop (easiest, free, no terminal)

1. On a computer, go to **https://app.netlify.com/drop**
2. Drag the **whole folder** (the one containing `index.html`) onto the page.
3. Wait a few seconds. Netlify gives you a live HTTPS link like
   `https://random-name-1234.netlify.app`.
4. Open that link **on your phone**.
5. Install it (see "Installing on your phone" below).

> Optional: make a free Netlify account to keep the link permanent and give it a
> nicer name. Without an account the link still works but may expire.

---

## Route B — GitHub Pages (free, permanent, a little more setup)

1. Make a free account at **https://github.com**
2. Create a new repository (e.g. `anchor`), set it to Public.
3. Upload all the files in this folder into the repo (Add file → Upload files).
4. Go to the repo's **Settings → Pages**.
5. Under "Build and deployment", set Source = "Deploy from a branch", branch = `main`,
   folder = `/ (root)`. Save.
6. After a minute, your app is live at
   `https://YOURNAME.github.io/anchor/`
7. Open that link on your phone and install it.

---

## Installing on your phone

**iPhone / iPad (Safari):**
1. Open the link in **Safari** (must be Safari, not Chrome).
2. Tap the **Share** button (the square with an up-arrow).
3. Scroll down, tap **Add to Home Screen**.
4. Tap **Add**. The Anchor icon now sits on your home screen like any app.

**Android (Chrome):**
1. Open the link in **Chrome**.
2. Tap the **⋮** menu (top right).
3. Tap **Install app** (or "Add to Home screen").
4. Confirm. Done.

---

## Turning on the AI features

The "Break it down" and "AI coach" features need your own Anthropic API key once the
app runs on your phone (they're free to set up; usage is pay-as-you-go and very cheap
for this kind of light use).

1. Go to **https://console.anthropic.com/** and sign in.
2. Open **API Keys**, create a key (starts with `sk-ant-…`), copy it.
3. In Anchor, go to the **More** tab → **AI settings**, paste the key, tap Save.

The key is stored only on your device. Every other feature — habits, insights,
timers, routines, mood, capture, points — works fully **without** a key.

---

## Your data

Anchor stores everything locally on your device. Use **More → Export backup** now and
then to save a copy, and **Import** to restore it (or move it to a new phone).

---

## Notes & limits

- A PWA is the practical best option for a personal tool. A true native App Store /
  Play Store app would require Apple's $99/yr developer program, store review, and a
  native build — overkill here, and not something that can be handed to you as a
  ready-to-run file.
- If you open `index.html` directly from your files (a `file://` address) instead of
  hosting it, the app will still run but **offline mode and home-screen install won't
  work** — those need the HTTPS hosting from Route A or B.
- This is a personal wellbeing tool, not medical advice or a substitute for care from
  a clinician.
