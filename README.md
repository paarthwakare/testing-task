# Overview
This is a small, self-contained web app that renders a glass bottle filled with water. You can increase or decrease the water level using buttons, a slider, the keyboard, the mouse wheel, or by dragging vertically. The fill level is displayed as a percentage and as milliliters (assuming a 1000 ml capacity).

Under the hood, the bottle silhouette is an SVG path. The water is drawn within that shape and additionally clipped by a dynamic rectangle to represent the current level. Gentle wave and bubble animations make the water feel alive.

Public JavaScript functions are exposed:
- increaseLevel(amount = 5)
- decreaseLevel(amount = 5)

These can be called from the console or other scripts to control the fill programmatically.

# Setup
No build tools or servers are required.

- Option 1: Double-click index.html to open it in any modern browser.
- Option 2: Serve the folder with a static server (optional) if your environment restricts file URLs.

Tested on recent versions of Chrome, Edge, Firefox, and Safari.

# Usage
- Buttons:
  - “+5%” to increase, “-5%” to decrease.
  - “Fill” sets to 100%, “Empty” sets to 0%.
  - Press and hold +/− buttons for continuous “pour”.
- Slider: Drag to any percentage from 0 to 100.
- Keyboard: Up/Down arrows or W/S adjust by 1%. Home sets to 0%, End sets to 100%.
- Mouse: Scroll over the bottle to adjust by 2% per notch.
- Drag: Click or touch the bottle and drag up/down to change the level.
- Programmatically: Open DevTools and run:
  - increaseLevel() or increaseLevel(12)
  - decreaseLevel() or decreaseLevel(20)

The app persists the last level in localStorage and restores it on the next visit.

If Round 2, describe improvements made from previous version.