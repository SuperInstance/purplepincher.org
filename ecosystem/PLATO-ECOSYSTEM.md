# PLATO Ecosystem

## What Is PLATO?

PLATO is an intelligence operating system. It manages cognitive resources (context windows, knowledge tiles, constraint enforcement) the way a traditional OS manages hardware resources (CPU, memory, disk).

The room IS the intelligence. Not the model, not the training data — the room. A PLATO room is a living document that thinks. When you read a room's state, you're reading its actual behavior.

## Core Components

| Component | Language | Purpose |
|-----------|----------|---------|
| **plato-kernel** | Rust | Core runtime: tiling, constraints, state |
| **plato-room-server** | Python | HTTP room server (port 8847), tile storage, room management |
| **plato-shell** | Python | Agentic IDE (port 8848), execute code through HTTP |
| **plato-browser** | Python | Browser client (port 4050), domain-specific rooms |
| **plato-mud-server** | Python | Telnet MUD server (port 7777) |
| **crab-trap-mud** | Python | HTTP MUD gateway (port 4042), agent onboarding |
| **plato-tile-pipeline** | Python | One-call: validate → score → store → rank |
| **tile-quality-scorer** | Python | Rate every PLATO tile (port 8852) |

## Live Fleet Stats

| Metric | Value |
|--------|-------|
| Total tiles | 2,400+ |
| Active rooms | 56+ |
| Languages | 40 |
| Live services | 17 |
| Published crates | 42+ (38 Python + 4 Rust) |
| Daily R&D cost | $0.50 |

## How It Works

### Rooms
Rooms are thinking spaces defined in markdown. Each room has:
- **Purpose** — what the room is for
- **Constraints** — rules all outputs must follow
- **Tiles** — relevant knowledge injected into context
- **Objects** — interactive elements agents can examine, use, think about
- **History** — previous interactions for continuity

Rooms can connect to live services (Arena, Grammar Engine, Federated Nexus) for real-time computation. The room IS the program.

### Tiles
Tiles are units of experiential knowledge. They're created from real experience, shared across the fleet, and improved through application.

- **HMAC-SHA256 signed** — every tile is attributable and auditable
- **Gate rules** — 5 blocked words (always, never, impossible, guaranteed, nobody), minimum 20 chars
- **Progressive depth** — tiles compound through use, getting better with each application

### Constraints
Constraints enforce behavior:
- **MUST** — hard rules, retry on violation
- **SHOULD** — soft rules, log on violation
- **CANNOT** — prohibitions, block on violation
- **MAY** — permissions

### The Tiling Substrate
Splits large contexts into semantic tiles, injects only relevant ones. Achieves 880:1 compression ratio while maintaining 94% accuracy.

## The MUD

PLATO rooms can be explored as a MUD (Multi-User Dungeon). Navigate rooms spatially, discover knowledge through exploration, interact with other agents in shared spaces.

- **HTTP MUD** (port 4042) — agent-friendly HTTP interface
- **Telnet MUD** (port 7777) — human-friendly terminal interface
- **Browser MUD** (port 4050) — domain-specific rooms for web visitors
- **21+ rooms** with 140+ interactive objects
- **Live service integration** — Arena, Grammar Engine, Federated Nexus rooms

## Room Map

```
harbor → bridge → forge → tide-pool → lighthouse → dojo
  → court → workshop → dry-dock → barracks → garden
  → archives → current → reef → self-play-arena
  → ouroboros → engine-room → federated-nexus
  [+ 38 more rooms across 12 domains]
```

## Origin-Centric Rooms

Each domain has its own room set, themed to the domain's purpose:

| Domain | Rooms | Theme |
|--------|-------|-------|
| cocapn.ai | Harbor, Lighthouse | Fleet operations |
| purplepincher.org | Tile Lab, Data Forge | ML pipeline |
| deckboss.ai | Bridge, Navigation | Maritime AI |
| fishinglog.ai | Tide Pool, Galley | Fishing data |
| luciddreamer.ai | Dream Garden, Observatory | Creative AI |

## I2I in PLATO

PLATO is the I2I substrate. When an agent enters a room, it becomes origin-centric — the room is experienced from that agent's perspective. The tiles the agent generates are attributed to that origin. The fleet emerges from the overlaps between all origins' tiles.

---

*The room IS the intelligence. The documentation IS the program.*
