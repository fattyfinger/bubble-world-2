# Bubblegun — Build Status

## Phase 1: Engine Foundation (CURRENT)
The single-player engine must feel good before we add multiplayer.

- [ ] **Player controller** — WASD + mouse look + jump + sprint (port from bubble-world)
- [ ] **Arena map** — symmetrical level with cover, spawn zones, candy theme
- [ ] **Player model** — simple rounded avatar, team-colored
- [ ] **Health system** — HP bar, damage, death, respawn with invulnerability
- [ ] **Lives system** — 5 lives, elimination, spectator mode
- [ ] **Bubble gun** — projectile with arc, hit detection
- [ ] **Bubble trap** — trapped state (float up, can't move, timed pop)
- [ ] **Coin drops** — spawn on death, pickup heals
- [ ] **HUD** — health bar, lives, crosshair, kill feed, team score

## Phase 2: Game Loop & Polish
- [ ] **Win/lose condition** — team elimination check, end screen
- [ ] **Respawn system** — timer, spawn zones, invulnerability blink
- [ ] **AI bots** — basic bots so you can test solo and kids can practice
- [ ] **Sound effects** — bubble pop, gun shoot, coin pickup, death
- [ ] **Visual polish** — particles, screen shake, hit markers, confetti
- [ ] **Map props** — gumball machines, candy canes, lollipop pillars

## Phase 3: Multiplayer
- [ ] **PeerJS integration** — WebRTC peer-to-peer connections
- [ ] **Lobby system** — create room, share code, join room
- [ ] **Team assignment** — pick pink or blue, auto-balance
- [ ] **State sync** — player positions, health, projectiles
- [ ] **Host authority** — host validates hits and deaths
- [ ] **Latency handling** — interpolation, client-side prediction

## Phase 4: Ship It
- [ ] **GitHub Pages deploy** — static hosting, shareable URL
- [ ] **Mobile support** — touch controls (stretch goal)
- [ ] **Leaderboard** — localStorage match history
- [ ] **Final playtest** — kids test, iterate on feedback

## What We Have Now (from bubble-world)
- Three.js scene setup, renderer, camera
- First-person controller (WASD + mouse + fly mode)
- Terrain generation (will replace with arena)
- Bubble placing/removing mechanics (will adapt to projectiles)
- Gun system with raycasting (will adapt to bubble gun)
- Particle effects (will reuse for pops)
- Settings menu with keybinds
- HUD framework

## What Needs to Change
| Bubble World Feature | Bubblegun Adaptation |
|---------------------|---------------------|
| Open terrain | Enclosed symmetrical arena |
| Place bubbles on ground | Shoot bubble projectiles |
| Single player sandbox | Team multiplayer combat |
| Fly mode | Remove (ground combat only) |
| Color palette selection | Team colors only (pink/blue) |
| Score counter | Lives + team elimination |
| Gun pickups | Everyone starts with bubble gun |
