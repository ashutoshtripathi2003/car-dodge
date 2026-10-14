# Car Dodge – 2D Car Dodging Game

A 2D arcade car-dodging game built for the **2D Game Design and System Modeling** (Computer Graphics) project.

**Team:** Atharva Bhosale (24101C0008) · Pranay Upadhyay (24101C0024) · Burhanuddin Lokhandwala (24101C0013) · Ashwin Agarwal (24101C0015)

## How to play

Open `CarDodge_standalone.html` in any modern browser (Chrome, Edge, Firefox). No installation is needed.

| Key | Action |
|---|---|
| ← → or A / D | Steer |
| P or Esc | Pause / resume |
| M | Sound on / off |
| Space / Enter | Start / restart |

On phones, press and hold either half of the road, or use the ◀ ▶ buttons.

## Features

- Scrolling 4-lane road with roadside scenery
- Player car with smooth movement and tilt (rotation transform) while steering
- Random traffic that never blocks every lane
- AABB collision detection, crash sparks and screen shake
- **8 levels** (every 300 points): Suburb, Highway, Desert, Coast, Mountain, City Night, Storm (rain), Endless
- **7 car colours** to choose from (remembered between visits)
- **Coins** (+20 points each) in trails along the lanes
- **Power-ups:** Shield (6 s, smash through traffic for +15), Magnet (8 s, pulls coins), Slow-Mo (5 s)
- Score, best score (saved in the browser) and Game Over / Restart screens
- Background chiptune music and sound effects, all generated in code

## Scoring

| Event | Points |
|---|---|
| Distance driven | continuous |
| Passing a car | +10 |
| Collecting a coin | +20 |
| Smashing a car with the shield | +15 |

## Technologies

- **HTML5** – page structure, HUD and menus
- **CSS3** – layout, styling, responsive design for phones
- **JavaScript** – game logic, game loop, state machine
- **HTML5 Canvas API** – 2D rendering, sprites, transformations (translate / rotate / scale), animation
- **Web Audio API** – synthesised music and sound effects (no audio files)
- **localStorage** – best score, car colour and mute setting

No external libraries or game engine are used.

## Code structure (inside `index.html`)

| Module | Responsibility |
|---|---|
| `Game` | Game manager and state machine (menu → playing ⇄ paused → over) |
| `Player` | Player car movement, tilt and hitbox |
| `ObstacleManager` | Spawning and moving traffic |
| `Collision` | AABB collision checks |
| `Pickups` / `Power` | Coins, power-ups and their timers |
| `Levels` | Level progression, speed and scenery |
| `ScoreManager` | Score, coins and best score |
| `Sound` | Music sequencer, engine sound and sound effects |

## Files

- `index.html` – game source (body content, as published online)
- `CarDodge_standalone.html` – complete page to open offline / submit
