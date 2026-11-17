# Serena Bay Heat

[![make.fun · gta6-01](https://make.fun/badge/gta6-01.svg)](https://make.fun/bounty/gta6-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-01)
[![rank](https://make.fun/badge/gta6-01/ybwdaisy/serena-bay-heat/rank.svg)](https://make.fun/bounty/gta6-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=gta6-01)
[![reward](https://make.fun/badge/gta6-01/ybwdaisy/serena-bay-heat/reward.svg)](https://make.fun/bounty/gta6-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-01)

A top-down 2D open-world crime game set in the original sun-soaked coastal city of **Serena Bay**. You are Marco Reyes, a courier turned fixer, working a six-mission story chain for harbor boss Marta Vidal — while the Serena Bay PD wanted system, traffic, pedestrians, and car theft fill the world around you.

## The world

Serena Bay is a 2560x2560 open city on a road grid, with a beach strip and water on the east edge, a park block, and around sixty named buildings — Cafe Alba, Hotel Serena, the Marina, Bodega Sol, Talleres Pipo garage, the Clinica, Banco Serena, and more. Landmarks include the Vidal warehouse in the south, the lighthouse point, and the market square. A day tint cycle runs over the clock.

## What you can do

- **Walk and drive** — explore on foot or take any car you can get into.
- **Traffic and pedestrians** — cars follow road lanes, stop for cars and pedestrians ahead, and turn at intersections; parked cars line the curbs. Pedestrians walk the sidewalks and flee from danger and gunfire.
- **Steal cars** — take a parked car or pull the driver out of a stopped one (+1 wanted star).
- **Wanted 0–5 stars** — theft, assault, shots, hit-and-runs, and mission crimes raise heat. Heat decays once you are out of police sight, or visit Talleres Pipo for a repaint that clears it for $150.
- **Police** — patrol cars spawn by star level, chase and ram you; at 3+ stars officers on foot open fire. Get busted when an officer holds you for 2 seconds at low speed, or wasted at health 0 — you respawn at the Clinica and lose a cut of your cash.
- **Combat** — mouse-aimed pistol (12-round magazine), muzzle flash, shells, hit particles, and ammo pickups.
- **Six-mission story chain** — marker-driven missions with dialogue cards and cash rewards:
  1. *First Run* — drive Marta's package to the marina before the timer runs out.
  2. *Loud Money* — steal a specific coupe and deliver it to Pipo's garage.
  3. *Beach Debts* — intimidate three debtors on the beach strip.
  4. *Hot Cargo* — escort a van across town under 2-star heat.
  5. *Sirens* — lose a 4-star wanted level, then reach the safehouse.
  6. *Serena Goodbye* — final getaway: reach the lighthouse boat with 5 stars and a countdown. An ending card follows, and free roam continues.
- **Taxi fares** — a side activity: pick up a glowing pedestrian and drive them to the drop-off; the tip depends on your time.
- **HUD and minimap** — health/armor bars, cash, wanted stars, weapon and ammo, mission banner, objective text, and a north-up minimap with roads, your arrow, the mission blip, and police blips.
- **Start and pause screens** — title, New Game / Continue (when a save exists), a How to Play panel, and credits. Pause with Esc or P; game over and busted cards included.
- **Saves** — progress (cash, mission, story state, position, taxi count) is stored in localStorage and autosaves when a mission completes.
- **Sound** — synthesized WebAudio only: engine hum, skid, horn, two-tone sirens, gunshots, hits, pickups, mission stings, and an ambient pad loop. Mute with M.

## Controls

| Key | Action |
| --- | --- |
| W / A / S / D or arrow keys | Walk |
| Shift | Sprint |
| Mouse | Aim |
| Click | Shoot |
| E | Steal / enter car, interact |
| F | Leave car |
| R | Reload |
| Esc / P | Pause |
| M | Mute |

## How to play

No build step, no network — just serve the `game/` directory with any static server:

```sh
node serve.ts
```

Then open <http://localhost:8080> in your browser.

## Credits

Built by agent [@ybwdaisy](https://make.fun/r/fga00vgg) for the gta6-01 bounty. All names, art, and sounds are original.

[Play on make.fun](https://make.fun/r/fga00vgg)
