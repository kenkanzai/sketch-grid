# Sketch Grid — handover

## What it is
Phone app (PWA) for drawing: open a photo, put a grid or diagonals over it, and copy it onto paper square by square. Works offline after the first visit.

## Files
- index.html — the whole app (HTML, CSS, JS in one file)
- manifest.json — app name, icons, colours (makes it installable)
- sw.js — offline cache. Current: `sketch-grid-v5`. Change to `v6` etc. after every update, so phones load the new version.
- icon-192.png, icon-512.png, icon-maskable-512.png — home-screen icons

## Features
- Grid tab: guide None / Grid / Diagonal / Both; square size in cm on paper (− / + buttons and 0.5–10 cm slider, 0.5 cm steps); line colour; strength; thickness; A1/B2 labels.
- Paper tab: A5, A4, A3, Letter, Square, Custom (cm); portrait / landscape; Fill the paper / Show whole photo. The white frame is the crop. Drag to move, pinch to resize.
- Image tab: Colour / Greyscale / Tones (3, 4 or 5 steps, Grey or Colour); brightness; contrast; Pick a colour; reset.
- Tones: split by the photo's own light-to-dark spread, so each tone covers a similar share of the photo. Greys run from soft dark (45) to soft light (232), never pure black or white. A numbered legend (1 = lightest) shows above the paper.
- Tone colour (Grey / Colour, default Colour): Colour keeps each area's colour as a flat patch (12 hue groups + one neutral group per step), set to that step's lightness, so the light-to-dark guide is the same as Grey.
- Pick a colour: tap a spot on the photo to see its colour, a mixing guide (pure colour + white + black) and strips of its tints (+ white), shades (+ black) and tones (+ grey). In Tones mode it also shows the tone number. Close with ✕.
- Finished squares: in zoom, tap Done to tick a square; ticks show as a small badge on the main view and the count shows in the Grid tab. Ticks are kept per paper size and square size, cleared by a new photo or Clear ticks (Tools).
- Tools tab: zoom into one square (also double-tap a square; swipe or arrows for next square; exit with the Exit zoom button, a tap outside the square, or the phone back button; a hint shows the first time); keep screen on; mirror; rotate 90°; save with grid or photo only (PNG at 150 dpi, paper size); install button (Android Chrome).
- Lock button (top): stops the photo moving while drawing.
- Picture first: settings close when a photo opens. Tap the photo to close settings; tap again for full view (all controls hidden); tap again to show them.
- Landscape / PC: settings sit on the right side.
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
