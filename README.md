# Wedge Book

A single-page golf wedge-yardage tracker with GPS measurement, designed for iPhone Safari.

## What it is

Wedge Book lets you log carry distances for each wedge (full swing and 50% swing), filter by condition (calm / into wind / downwind), and measure shots on the course using your phone's GPS. All data lives in `localStorage` — no server, no account.

## Wind / calm note

The baseline seed data (Session 1, 31 May) is tagged **Into wind**. Session 2 (6 June) is tagged **Calm** as a working assumption — re-tag any shot in-app if conditions were different. Use the condition filter so wind and calm averages never blend together.

## How to use

1. Open the app on your iPhone and tap **Add to Home Screen** for full-screen, offline use.
2. **Tap a wedge column** (Full · Stock or 50% Swing) to select a logging target.
3. Pick a condition (Calm / Into wind / Downwind) in the bottom bar.
4. Type a yardage and tap **ADD** (or press Enter).
5. **◎ Measure a Shot · GPS** — tap to open the GPS panel. Mark Ball at your feet, walk to the ball, tap Mark Landing. The Haversine distance (carry + roll) is computed and saved with `gps: true`.
6. Use the **Scope** toggle (Today / All time) and **Condition filter** to slice the averages.
7. Tap **Edit** to rename wedges, edit lofts, add or remove wedges, or clear shots.

## GPS / HTTPS note

GPS requires the app to be served over **HTTPS**. GitHub Pages provides HTTPS automatically. If you host it elsewhere, self-signed certificates will NOT work on iOS — you need a trusted certificate.

## Deploy

GitHub Pages: push `index.html`, `README.md`, and `.nojekyll` to `main`, then enable Pages under **Settings → Pages → Deploy from branch → main → / (root)**. The app will be live at `https://<user>.github.io/<repo>/`.
