# Rubik

A single-file 3D Rubik's Cube simulator built with Three.js.

## Overview

This project renders a fully interactive 3x3x3 Rubik's Cube in the browser with smooth animated face turns, orbit camera controls, scramble/reset actions, and keyboard shortcuts. The app is implemented entirely in `index.html` (HTML, CSS, and JavaScript module code in one file).

## Features

- Real-time 3D rendering with Three.js
- 27-cubie cube model with standard face colors
- Animated quarter-turn moves (`U D L R F B` and inverses)
- Move queue for sequential turn playback
- Clickable move controls in a HUD panel
- Keyboard controls (`Shift` for inverse moves)
- One-click 24-move random scramble
- Reset to solved state
- Responsive fullscreen canvas with orbit + zoom camera controls

## Tech Stack

- HTML5 / CSS3
- JavaScript (ES modules)
- [Three.js](https://threejs.org/) via import map + unpkg CDN

## Project Structure

```text
Rubik/
  index.html   # complete app (UI + styles + renderer + cube logic)
  README.md
```

## Getting Started

### Option 1: Open directly

Open `index.html` in a modern browser.

### Option 2: Serve locally (recommended)

Some browsers are stricter with module imports from local files. Running a local server is more reliable:

```powershell
cd C:\Users\pebsn\Documents\GITHUBprojects\Rubik
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Controls

- Mouse drag: orbit camera
- Mouse wheel: zoom
- Buttons: click any move (`U U' D D' L L' R R' F F' B B'`)
- Keyboard: `U D L R F B`
- Inverse move: hold `Shift` while pressing a move key
- `Scramble`: enqueue random moves
- `Reset`: clear state and rebuild solved cube

## Notes

- Three.js modules are loaded from CDN (`unpkg.com`), so internet access is required at runtime unless you vendor dependencies locally.
- The renderer uses tone mapping, sRGB output, and multi-light setup for a polished look.

## Future Improvements

- Move history / undo
- Timer + solve session tracking
- Notation parser for algorithm input
- Touch-optimized mobile controls
- Basic auto-solver integration

## License

No license file is currently included. Add one (for example MIT) if you want to define usage terms.
