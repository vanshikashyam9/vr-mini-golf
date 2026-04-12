# ⛳ VR Mini-Golf

A mobile VR mini-golf game built with [A-Frame](https://aframe.io) for **CMPT 461 — Immersive Computing** at Trinity Western University.

## Quick Start

### Run Locally

```bash
# Option 1: npx serve
npx serve .

# Option 2: Python
python3 -m http.server 8080
```

Then open `http://localhost:3000` (or `http://localhost:8080`) in your browser.

### Run on GitHub Pages

1. Push this repo to GitHub
2. Go to **Settings → Pages → Source: main branch, root folder**
3. Access at `https://<username>.github.io/<repo-name>/`

## How to Play

- **Aim**: Look left/right to point your shot direction
- **Power**: Tilt head forward (Tilt mode) or let it auto-charge (Gaze mode)
- **Swing**: Look at the green SWING button and hold gaze for 1.5 seconds
- **Goal**: Get the ball in the hole in as few strokes as possible

## Game Features

| Feature | Description |
|---------|-------------|
| 2 Levels | Park Course (par 3) and Canyon Course (par 4) |
| Gaze Controls | Aim with head direction, dwell-click to swing |
| Head Tilt | Tilt forward to charge power |
| Scoreboard | Always-visible HUD showing strokes and score |
| Audio | Background music + sound effects (mutable) |
| VR Mode | Stereoscopic split-screen for mobile VR headsets |
| Collisions | Ball bounces off walls and obstacles |
| Setup Menu | Audio, difficulty, and control customization |

## Files

```
vr-mini-golf/
├── index.html          ← Main game
├── manual.html         ← Detailed game manual
├── README.md           ← This file
└── assets/textures/    ← Game textures (turf, desert, brick, wood, ball, sky)
```

## Manual

Open [manual.html](manual.html) for detailed instructions on controls, setup, scoring, and troubleshooting.

## Credits

- **Developer**: Vanshika Shyam
- **Course**: CMPT 461, Simon Fraser University, April 2026
- **Framework**: A-Frame 1.4.2
- **Audio**: Web Audio API (procedural)
- **Textures**: Custom generated
