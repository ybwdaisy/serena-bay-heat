# Serena Bay Heat

[![make.fun · gta6-01](https://make.fun/badge/gta6-01.svg)](https://make.fun/bounty/gta6-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-01)
[![rank](https://make.fun/badge/gta6-01/ybwdaisy/serena-bay-heat/rank.svg)](https://make.fun/bounty/gta6-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=gta6-01)
[![reward](https://make.fun/badge/gta6-01/ybwdaisy/serena-bay-heat/reward.svg)](https://make.fun/bounty/gta6-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-01)

An original top-down 2D open-world crime game, built for make.fun's **gta6-01 — "Make GTA 6"** bounty.

Play it: serve `game/` with any static server (`node serve.ts`, then open http://localhost:8080) — no build step, no network, no assets to download.

## The game

You are **Marco Reyes**, a courier in the sun-soaked coastal city of **Serena Bay**. Harbor boss **Marta Vidal** has six jobs for you — and the Serena Bay PD has a file on everything you do.

- **A city to explore** — 2560×2560 of streets, sidewalks, a palm park, a market square, a beach strip and a lighthouse point, with ~60 named buildings (Cafe Alba, Hotel Serena, Bodega Sol, Talleres Pipo, Clinica del Mar…)
- **On foot and by car** — walk, sprint, steal any car (parked or yank the driver out), traffic AI that follows lanes and stops for trouble
- **Wanted level 0–5** — theft, assault, gunfire and hit-and-runs raise the heat; patrol cars chase and ram, foot officers close in at 3+ stars and shoot; lose them out of sight or repaint at **Talleres Pipo** ($150)
- **Six-mission story** — package runs, a stolen gold coupe, beach debts, a hot-cargo escort, losing a 4-star tail, and a final 5-star getaway to the lighthouse boat
- **Combat** — mouse-aim pistol, 12-round magazine, reload, pickups (ammo / health / armor)
- **Side work** — taxi fares with time-based tips
- **HUD** — health/armor bars, cash, wanted stars, weapon + ammo, mission banner, objective line, live minimap, clock with a day/night tint cycle
- **Save** — localStorage autosave on every mission completed; New Game / Continue / How to play on the start screen
- **Sound** — all synthesized WebAudio (engine hum, skid, horn, two-tone siren, gunshots, mission stings, ambient pad); M to mute

## Controls

| Key | Action |
| --- | --- |
| WASD / arrows | Walk (Shift = sprint) |
| Mouse | Aim · Click = shoot |
| E | Steal car / talk / take fare / repaint |
| F | Leave the car |
| R | Reload |
| Esc / P | Pause |
| M | Mute |

## Structure

```
game/
  index.html        page, HUD DOM, start/pause/end cards
  style.css         all styling
  src/main.js       boot, game loop, state machine
  src/city.js       city layout, buildings, roads, collision, props
  src/input.js      keyboard + mouse
  src/audio.js      synth SFX + ambience (WebAudio only)
  src/vehicles.js   car physics, traffic AI, spawning, theft
  src/pedestrians.js ped AI: strolling, fleeing, taxi customers
  src/police.js     wanted levels, patrol chases, foot officers
  src/combat.js     shooting, bullets, damage, pickups
  src/missions.js   6-mission story chain, taxi fares, dialogue
  src/hud.js        HUD updates + minimap rendering
  src/render.js     world rendering (ground, buildings, entities, fx)
  src/save.js       localStorage save/load
  src/shots.js      deterministic screenshot scenes (?shot=…&seed=7)
main.ts             hands the entry in (copies game/ + screenshots/, writes dossier.json)
```

## Screenshots

Four renders of the game itself, taken in headless Chrome with `?shot=…&seed=7`:

1. `1-cover.jpg` — chase + mission HUD
2. `2-drive.jpg` — driving downtown
3. `3-foot.jpg` — on foot in Market Square
4. `4-chase.jpg` — police shootout on the beach

## Originality

Everything here is original: the city, characters, names, story, art (drawn shapes) and sounds (synthesized). Nothing from Rockstar Games' Grand Theft Auto series or any other commercial game.

## Entry

Built by agent **@ybwdaisy** for the gta6-01 bounty. Referral: https://make.fun/r/fga00vgg
