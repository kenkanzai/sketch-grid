# Sketch Grid — handover

## What it is
Phone app (PWA) for drawing: open a photo, put a grid or diagonals over it, and copy it onto paper square by square. Works offline after the first visit.

## Files
- index.html — the whole app (HTML, CSS, JS in one file)
- manifest.json — app name, icons, colours (makes it installable)
- sw.js — offline cache. Change `sketch-grid-v1` to `v2` etc. after every update, so phones load the new version.
- icon-192.png, icon-512.png, icon-maskable-512.png — home-screen icons

## Features
- Grid tab: guide None / Grid / Diagonal / Both; square size in cm on paper (1–5 cm chips, 0.5–10 cm slider); line colour; strength; thickness; A1/B2 labels.
- Paper tab: A5, A4, A3, Letter, Square, Custom (cm); portrait / landscape; Fill the paper / Show whole photo. The white frame is the crop. Drag to move, pinch to resize.
- Image tab: Colour / Black and white / Tones (3, 4 or 5 greys); brightness; contrast; reset.
- Tools tab: zoom into one square (also double-tap a square; swipe or arrows for next square); keep screen on; mirror; rotate 90°; save with grid or photo only (PNG at 150 dpi, paper size); install button (Android Chrome).
- Lock button (top): stops the photo moving while drawing.
- Remembers settings and the last photo on the phone.

## Rules
- Grid always starts at the top-left corner of the paper, so squares match the paper when you rule them from the corner.
- Square size is in real cm on the chosen paper.
- Image changes (tones, brightness, contrast) never change the saved original file.

## Install on Samsung / Android
1. Create a GitHub repo, upload all files in this folder (not the zip).
2. Settings > Pages > Deploy from branch > main > / (root) > Save.
3. Open the Pages link in Chrome on the phone.
4. Tap Install app in the Tools tab, or Chrome menu > Add to home screen > Install.
