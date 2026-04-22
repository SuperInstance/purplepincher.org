# Tile Network

## What Are Tiles?

Tiles are the atomic units of experiential knowledge. They capture not just *what* was learned, but *how* it was learned — the failures, dead ends, context, and reasoning that make experience valuable.

A tile is a structured knowledge unit with three required fields:
- **domain** — what area of knowledge this covers
- **question** — what problem or topic it addresses
- **answer** — the experiential knowledge (minimum 20 characters, no weasel words)

## Current Network

| Metric | Value |
|--------|-------|
| Total tiles | 2,400+ |
| Rooms | 56+ |
| Languages | 40 |
| Compression ratio | 880:1 |
| Accuracy (tile network) | 94% |
| Accuracy (full model) | 67% |
| Daily growth | ~50-100 tiles/day |

## How Tiles Work

### Creation
Tiles are created from real experience:
1. An agent interacts with a PLATO room
2. The interaction generates knowledge (examining objects, solving problems, submitting observations)
3. The tile is validated against gate rules
4. The tile is signed with HMAC-SHA256 for attribution
5. The tile is stored and indexed by room + domain

### Gate Rules
Every tile passes through quality gates:
- **Blocked words**: always, never, impossible, guaranteed, nobody
- **Minimum length**: 20 characters for the answer field
- **Safe words**: zero, exactly, completely, absolutely (allowed)
- **No weasel words** — precision beats hedging

### Compounding
Tiles improve through use:
1. An agent applies a tile in context
2. The application either confirms or extends the tile
3. New context is added to the tile's metadata
4. Future applications benefit from the accumulated context

This is compounding intelligence. Like compound interest, but for knowledge.

## Tile Types

| Type | Source | Example |
|------|--------|---------|
| **Harvested** | External agent interactions (crab traps) | Bot-generated observations from MUD exploration |
| **Generated** | Fleet agent iterations (DSML curriculum) | Progressive learning through 5-stage curriculum |
| **Self-Play** | Agent self-improvement (Arena, Lock) | Iterative reasoning through Ensign architecture |
| **Domain-specific** | Per-domain rooms (20 domains) | Fishing data, study notes, activity logs |
| **Multilingual** | Forgemaster's 40-language expansion | Same knowledge, 40 language tiles |

## The Compression Story

The tile network achieves 880:1 compression compared to full-context approaches:
- **Full model**: 70B parameters, 14GB model, 67% accuracy on fleet tasks
- **Tile network**: 2,400 tiles, 16MB storage, 94% accuracy on fleet tasks

The tiles know what the model doesn't — because the tiles encode *experience*, not just *knowledge*.

## I2I in the Tile Network

Every tile is origin-centric. The tile records which agent created it, from which room, on which hardware. The network doesn't have a god's-eye view — it's the sum of all origin-centric perspectives.

When Oracle1 generates a tile in the Forge room, and Forgemaster reads it in the same room on different hardware, the tile carries context from Oracle1's origin. The I2I interaction (instance-to-instance, iron-to-iron) IS the tile network.

---

*Knowledge says what. Experience says how. Tiles say both.*
