# CMPT 461 — VR Mini-Golf: AI Prompts Log

**Student:** Vanshika Shyam  
**Course:** CMPT 461 — Immersive Computing, Trinity Western University  
**Date:** April 2026  
**AI Tool Used:** Google Gemini (Antigravity Coding Assistant)

---

## Summary

I used an AI coding assistant to help build my VR Mini-Golf game. Below is a complete log of all prompts I gave and what each one accomplished.

---

## Prompt 1 — Initial Game Concept & Planning
**Prompt:**  
> "Build me a VR mini-golf game for my CMPT 461 class using A-Frame..."  
*(Included full project requirements from the assignment)*

**Result:** AI created an implementation plan covering the project structure, file layout, levels, controls, textures, and audio approach.

---

## Prompt 2 — Generating Textures
**Prompt (implicit):** AI generated 6 custom textures for the game using image generation:
- Grass turf (Level 1 ground)
- Desert sand (Level 2 ground)
- Brick wall (obstacle texture)
- Wood plank (wall/ramp texture)
- Sky panorama (skybox)
- Golf ball (ball texture)

**Result:** 6 PNG texture files created and placed in `assets/textures/`.

---

## Prompt 3 — Building the Core Game
**Prompt (implicit):** AI built `index.html` containing:
- A-Frame scene with camera, lighting, sky
- Flashscreen overlay with name/credentials
- Setup screen with BGM, SFX, difficulty, and control options
- Two level definitions (Park Course, Canyon Course)
- Golf ball, hole, flag, obstacles, walls
- Gaze cursor with fuse-based dwell interaction
- HUD scoreboard attached to camera
- Power gauge display
- Web Audio API sound manager

**Result:** Complete game HTML file created.

---

## Prompt 4 — Documentation
**Prompt (implicit):** AI created:
- `manual.html` — Full game manual with setup, controls, levels, scoring, VR mode, and troubleshooting
- `README.md` — Quick-start guide with feature overview

**Result:** Two documentation files created.

---

## Prompt 5 — University Name Fix
**Prompt:**  
> "also i am in trinity western university not simon fraser university"

**Result:** Updated university name across all files.

---

## Prompt 6 — Fixing Blank Page / Rendering Issues
**Prompt:**  
> "this is what i see when i play the game" *(screenshot of blank white page)*

**Result:** Fixed three bugs:
1. A-Frame's loading screen was covering the game overlays (z-index conflict)
2. Removed `embedded` attribute that caused layout issues
3. Fixed A-Frame component registration order

---

## Prompt 7 — Fixing Invalid A-Frame Element
**Prompt:**  
> "no working"

**Result:** Discovered `a-circle` is not a valid A-Frame primitive. Replaced with `a-entity` using `geometry="primitive: circle"`. Also moved component registration to run before scene parsing.

---

## Prompt 8 — Fixing Physics and Multi-Swing
**Prompt:**  
> "in the game it just let me hit the ball once and the physics are also very weird fix it please"

**Result:** Complete rewrite of physics system:
- Frame-rate independent physics (delta-time based)
- Proper friction using `Math.pow(friction, dt)`
- Realistic gravity (9.8 m/s²)
- Swing button now hides during ball movement, reappears at ball's new position
- Added spacebar and screen-tap as alternative swing controls
- Power gauge now oscillates (like a real golf game power meter)

---

## Prompt 9 — Increasing Ball Speed
**Prompt:**  
> "ok now power has reduced very much its barely moving with any power"

**Result:** Increased ball velocity from 0.18 to 15 units/second and adjusted friction — the frame-independent physics needed much higher velocity values.

---

## Prompt 10 — Camera Follow
**Prompt:**  
> "the camera should also follow the ball"

**Result:** Added smooth camera follow system — camera lerps behind the ball during movement and settles at the ball's position for the next shot.

---

## Prompt 11 — Hard Mode Differences
**Prompt:**  
> "in the starting, when it shows the menu for sound there is this option of easy and hard but I don't see any changes when I switch to hard can you check what the difference"

**Result:** Made Hard mode have 4 noticeable differences:
- 3x stronger wind
- 40% more friction (ball stops sooner, needs precision)
- 2x faster power oscillation (harder to time shots)
- 2x faster moving obstacles

---

## Prompt 12 — Submission Preparation
**Prompt:**  
> "check [assignment requirements] and help me with the document"

**Result:** Created this AI prompts log and verified all 12 requirements are met.

---

## Requirements Checklist

| # | Requirement | Points | Status | Implementation |
|---|-------------|--------|--------|----------------|
| 1 | Unique game ideas | 5 | ✅ | Mini-golf with gaze-aim + head-tilt power |
| 2 | Manual | 5 | ✅ | `manual.html` with full docs |
| 3 | Flashscreen | 10 | ✅ | Animated overlay with name, course, university, date |
| 4 | Setup option | 10 | ✅ | BGM/SFX on-off, Easy/Hard difficulty, Gaze/Tilt controls |
| 5 | At least two levels | 10 | ✅ | Park Course (par 3) + Canyon Course (par 4, moving obstacle) |
| 6 | Sound effects + BGM | 10 | ✅ | Web Audio API: looping BGM, swing/hit/bounce/hole-in SFX |
| 7 | Scoreboard | 10 | ✅ | Always-visible HUD: hole, strokes, total, par |
| 8 | Gaze/head-tilt controls | 10 | ✅ | Gaze aiming, dwell-to-swing, head-tilt power charging |
| 9 | Stereoscopic view | 5 | ✅ | A-Frame VR mode for Google Cardboard |
| 10 | Own objects with textures | 10 | ✅ | 6 custom textures on ball, ground, walls, obstacles, sky |
| 11 | Collision detection | 5 | ✅ | AABB collision with walls + obstacles + boundaries |
| 12 | Extra work | 10 | ✅ | Wind system, moving obstacles, camera follow, difficulty scaling, power meter, multiple control schemes |

**Total possible: 100 points**

---

## Submission Links

- **GitHub Pages (play the game):** https://vanshikashyam9.github.io/vr-mini-golf/
- **GitHub Repository:** https://github.com/vanshikashyam9/vr-mini-golf
- **Manual:** https://vanshikashyam9.github.io/vr-mini-golf/manual.html
