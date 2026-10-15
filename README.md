# Sudoku — Setup Guide

## What's inside
- **Easy / Medium / Hard** difficulty — every puzzle is generated fresh on-device with a guaranteed unique solution (not pulled from any server).
- **Timer**, **Mistake counter**, **Notes/pencil marks**, **Hints (3 per game)**.
- Tapping a cell highlights its row/column/box and any other cell with the same number.
- **Light/Dark theme toggle** (🌙/☀️ button, top right) — remembered for next time.
- **Auto-saves progress** — closing the app and reopening resumes exactly where you left off (paused, tap Resume).
- Completely **offline, no ads, no account, no server** — just like your Finance Vault app.

## APK build steps (same process as your other apps)

### Step 1: Host on GitHub Pages (free)
1. Create a new public GitHub repo (e.g. `sudoku`)
2. Upload all 6 files: `index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`, `README.md`
3. Repo Settings → Pages → Source: "Deploy from a branch" → Branch: main, folder: / (root) → Save
4. Your live URL: `https://<username>.github.io/sudoku/`

### Step 2: Package with PWABuilder
1. Go to https://www.pwabuilder.com, paste your GitHub Pages URL, click Start
2. "Package for Stores" → Android
3. Signing key: choose **"New"** the first time (this is a brand-new app, separate from Finance Vault) — save the downloaded `signing.keystore` + passwords safely for future updates
4. Download Package

### Step 3: Install & test
- Transfer the `.apk` to your phone, install it directly (not via Chrome's "Install" prompt — always the real signed APK)
- Play a puzzle, test Notes mode, Hints, pausing, and switching theme

## Updating later
Same rule as your Finance Vault: keep the same package name and reuse the same signing key ("Use mine") every time you rebuild, so updates install cleanly.
