# TAG! 🏃

> A fast-paced local multiplayer tag game for 2–4 players. Race across platforms, grab power-ups, and avoid being the tagger when time runs out.

![TAG! Game Banner](https://img.shields.io/badge/version-1.4.0-ff4455?style=for-the-badge&labelColor=111)
![Players](https://img.shields.io/badge/players-2--4-00e5cc?style=for-the-badge&labelColor=111)
![Platform](https://img.shields.io/badge/platform-browser-ffd600?style=for-the-badge&labelColor=111)
![No dependencies](https://img.shields.io/badge/dependencies-none-b388ff?style=for-the-badge&labelColor=111)

---

## 🚀 Play Now

**[▶ tagisfunforall.vercel.app](https://tagisfunforall.vercel.app)**

No download, no install — just open and play.

---

## 📖 Overview

TAG! is a single-file browser game — no install, no server, no dependencies. Open the HTML file and play instantly. Up to 4 players share a keyboard across 4 unique maps, collecting power-ups and trying not to be "it" when the clock hits zero.

The tagger loses. Everyone else scores a point every second they stay untagged.

---

## 🎮 How to Play

1. Go to **[tagisfunforall.vercel.app](https://tagisfunforall.vercel.app)**
2. Set each player slot to **Human** or **Bot** (minimum 2 active players)
3. Pick a map, configure settings, and hit **START**
4. Avoid being the tagger — the player who is "it" at game end **loses**

### Controls

| Player | Move | Jump | Duck |
|--------|------|------|------|
| P1 | `A` / `D` | `W` | `S` |
| P2 | `←` / `→` | `↑` | `↓` |
| P3 | `J` / `L` | `I` | `K` |
| P4 | `4` / `6` (Numpad) | `8` | `5` |

**`Escape`** — Pause / unpause during a game.

---

## 🗺️ Maps

| Map | Difficulty | Description |
|-----|-----------|-------------|
| 🌲 **Forest** | Easy | Layered grass platforms with trees and flowers |
| ❄️ **Snowland** | Easy | Icy blue platforms, snowman decorations, pine trees |
| 🏜️ **Desert** | Easy | Sandy dunes, pyramids, cacti, and a tall palm tree |
| 🌌 **The Void** | Hard | Floating platforms in deep space — fall off and become the tagger |

---

## ⚡ Power-Ups

Power-ups spawn on platforms during the match (max 3 on the map at once). Walk into one to collect it — effects apply instantly.

| Icon | Power | Effect | Cooldown |
|------|-------|--------|----------|
| ★ | **Speed Boost** | Move at 2× speed for ~4 seconds | 5s |
| 👁 | **Invisible** | Become invisible to other players for ~6 seconds | 8s |
| ✦ | **Teleport** | Instantly warp to a random platform | 6s |
| ⬇ | **Shrink Tagger** | Makes the tagger tiny and very slow; non-taggers grow slightly | 10s |
| ⬆ | **Grow** | You become huge — harder for the tagger to reach around you | 9s |
| ❄ | **Freeze Tagger** | Freezes the tagger solid for ~3 seconds | 11s |

You can toggle which power-ups are active in **Game Settings** before starting.

---

## 🤖 Bot AI

Set any player slot to **Bot** for AI-controlled opponents. Bots have full intelligence:

- **Tagger bots** chase the nearest visible target, use step-platform routing to climb toward elevated players, and grab speed boosts when far away
- **Runner bots** score escape routes to the platform furthest from the tagger, use double-jumps to evade at close range, and wander toward uncollected power-ups when safe
- All bots respect the warp cooldown and avoid falling off the void map

---

## ⚙️ Game Settings

| Setting | Options | Default |
|---------|---------|---------|
| Game Time | 1 / 2 / 3 / 5 min, or custom MM:SS | 2 min |
| Speed | Slow / Normal / Fast | Normal |
| Double Jump | On / Off | On |
| Pickups | On / Off | On |
| Tagger Speed Boost | On / Off | On |
| Power-ups | Toggle each individually | All on |

### ⚡ Presets

Jump straight into play with one-click configurations:

| Preset | Description |
|--------|-------------|
| 😊 Casual | 2 min, all pickups, normal speed |
| 🧹 No Pickups | 2 min, clean gameplay, no powers |
| 💥 Chaos Mode | 3 min, all powers, fast speed |
| ⚖️ Fair Play | No tagger speed boost, no pickups |
| ⚡ Speed Run | 1 min, fast, no double jump |
| 🏃 Marathon | 5 min, all powers |

---

## 🕹️ Gameplay Mechanics

**Warp cooldown** — Running off the left or right edge warps you to the other side, but triggers a 1.5-second cooldown. If the cooldown is active you'll be stopped at the wall instead — no spamming the edge to escape bots.

**Platform phasing** — Hold `Duck` while moving over a platform to drop through it.

**Squish animation** — Hold `Duck` while standing on solid ground to flatten your character.

**Double jump** — Press `Jump` again mid-air to get a second jump (if enabled). A ring flash effect plays on the double-jump frame.

**Tag immunity** — After a successful tag, both players receive a brief immunity window so the tag can't be immediately reversed.

---

## 🏆 Scoring & End Screen

Every second a player is **not** the tagger, they earn 1 point. At game end:

- Rankings are displayed with time-survived scores
- The current tagger (the loser) is shown on the right panel with their character model
- Hit **Rematch** to replay the same settings instantly

---

## 📁 File Structure

```
tag-game.html   ← The entire game. One file. That's it.
README.md       ← This file
```

Everything — game logic, rendering, UI, maps, AI, and animations — lives inside a single self-contained HTML file. No build step, no npm, no server required.

---

## 🌐 Browser Compatibility

Works in any modern browser with Canvas 2D support.

| Browser | Support |
|---------|---------|
| Chrome / Edge | ✅ Full |
| Firefox | ✅ Full |
| Safari | ✅ Full |
| Mobile browsers | ⚠️ Keyboard required |

---

## 📋 Changelog

### v1.4.0 — March 2026
- Added 3 new power-ups: Shrink Tagger, Grow, Freeze Tagger
- All power-up pickups now have unique canvas-drawn icons
- Warp cooldown prevents edge-spam exploits
- Pickup cap: max 3 power-ups on map at once, slower spawn rate
- Redesigned Game Over screen with large LOSER label and full player model
- HUD timer enlarged

### v1.3.0 — March 2026
- Animated crowd on title screen
- Changelog billboard on title screen
- Screen pop-in transitions
- Redesigned GET READY screen (fullscreen map preview)
- Countdown camera now tracks players correctly

### v1.2.0 — February 2026
- Added The Void map
- Teleport power-up with warp animation
- Speed boost duration increased to 4s

### v1.1.0 — January 2026
- 4-player support with numpad controls
- Invisible power-up
- Custom game time input (MM:SS)
- Tagger speed bonus increased to 28%

### v1.0.0 — December 2025
- Initial release: Forest, Snowland, Desert maps
- Speed Boost power-up
- 2-player local multiplayer
- Dynamic camera tracking all players

---

## 📜 License

MIT — do whatever you want with it.

---

<div align="center">
  <strong>Made with zero dependencies. Just vibes and canvas.</strong>
</div>
