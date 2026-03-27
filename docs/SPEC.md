# Bubblegun — Game Specification

## Concept
Team-based bubble gum shooter. Pink Team (girls) vs Blue Team (boys).
Cute, bubblegum-themed aesthetic. Browser-based, hosted on GitHub Pages.
Kids share a link and play — no downloads.

## Win Condition
Eliminate all lives from the opposing team. Each player has **5 lives**.
Team wins when all opposing players have 0 lives remaining.

## Teams
| Team | Color | Theme |
|------|-------|-------|
| Pink Team | #ff6b9d | Bubblegum pink, sparkles, hearts |
| Blue Team | #51e5ff | Sky blue, stars, lightning bolts |

## Core Mechanics

### Movement
- **WASD** — move (forward, left, back, right)
- **Mouse** — look / aim
- **Space** — jump
- **Shift** — sprint
- Standard FPS control scheme

### Health System
- Each player has a **health bar** (100 HP)
- Health bar displayed above player character and on HUD
- When HP reaches 0: player dies, loses 1 life, respawns after 3 seconds
- **5 lives per player** — displayed on HUD
- When all lives spent: player is eliminated (spectator mode)

### Bubble Gun (Primary Weapon)
- Every player spawns with a bubble gun
- Shoots a **bubble projectile** that travels in an arc
- On hit: target gets **trapped in a bubble**
- Trapped state:
  - Player floats upward slowly
  - Cannot move or shoot
  - Lasts 3 seconds OR until bubble is popped by a teammate
  - If bubble is NOT popped in 3 seconds: **POP — player takes 50 damage**
  - If hit by another bubble while trapped: **instant kill**
- Fire rate: ~2 shots/second
- Ammo: unlimited (it's bubblegum, you always have more)

### Coin Drop / Health Recharge
- On death, player drops **coins** at death location
- Coins persist for 15 seconds
- Any player can pick up coins
- Each coin restores **25 HP**
- Number of coins dropped: 2-4 (based on how much HP killer was missing)

### Respawn
- 3 second respawn timer
- Respawn at team's spawn zone (opposite ends of map)
- Brief invulnerability (2 seconds, player blinks)

## Visual Style
- Bubblegum / candy aesthetic
- Rounded, soft geometry
- Pastel colors with bright accents
- Bubble particles everywhere
- Pop effects with confetti
- Bouncy animations
- Player characters: simple rounded avatars with team colors

## Map
- Symmetrical arena (fair for both teams)
- Bubblegum factory / candy land theme
- Cover objects (gumball machines, candy canes, lollipop pillars)
- Elevated platforms for tactical positioning
- Team spawn zones at opposite ends
- Size: medium — encourages close-range bubble fights

## HUD
- Health bar (bottom center)
- Lives remaining (icons, bottom left)
- Team score / lives remaining (top)
- Crosshair (center, bubblegum themed)
- Kill feed (top right)
- Respawn timer (center, when dead)

## Multiplayer
- **Hosting:** GitHub Pages (static files)
- **Networking:** Peer-to-peer via WebRTC (PeerJS library)
- **Lobby:** One player creates room, gets a code, others join with code
- **Player count:** 2v2, 3v3, or 4v4
- **Authority:** Host player is authoritative (anti-cheat lite)

## Tech Stack
| Layer | Technology |
|-------|-----------|
| Rendering | Three.js (r128+) |
| Physics | Custom (lightweight, from bubble-world base) |
| Networking | PeerJS (WebRTC wrapper) |
| Audio | Web Audio API |
| Hosting | GitHub Pages |
| Build | Single HTML or minimal bundled files |
