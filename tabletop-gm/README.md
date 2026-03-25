# tabletop-gm

A collaborative Game Master agent for tabletop adventure RPG, built on the Roboticus agent runtime.
Uses the d20 system (SRD 5.1, Creative Commons Attribution 4.0). All rules content is open-licensed.

---

## What's Included

| File | Purpose |
|---|---|
| `FIRMWARE.toml` | GM persona — identity, voice, rules system, combat guidance, narration style, safety boundaries, and rules reference entries |
| `skills/core-rules.md` | SRD 5.1 core rules quick reference — ability checks, saves, attacks, conditions, concentration, death saves, rest |
| `skills/encounter-running.md` | How to run combat — initiative, turn flow, player and creature turns, reactions, ending combat |
| `skills/creature-reference.md` | SRD 5.1 stat blocks by Challenge Rating (CR 0–10), tactics by intelligence, encounter building, improvised creatures |
| `skills/npc-delegation.md` | Subagent composition for significant NPCs — when to delegate, composition template, delegation protocol, retiring NPCs |
| `skills/gm-guide.md` | Adventure design, three-act pacing, improvisation toolkit, random tables, treasure, milestone leveling, social encounters, traps, one-shots |

---

## Quick Start

**1. Copy the package into your Roboticus workspace:**

```bash
cp tabletop-gm/FIRMWARE.toml ~/.roboticus/workspace/
cp tabletop-gm/skills/*.md ~/.roboticus/skills/
```

**2. Restart Roboticus or start a new session.**

**3. Open a conversation and start your session:**

```
GM, we're starting a new campaign. The setting is a frontier city on the edge of explored territory.
The party consists of a human fighter, an elf wizard, and a halfling rogue. What's the opening scene?
```

The agent will respond as The GM — establishing the scene, asking session-zero safety questions,
and prompting for initiative when the first threat arrives.

---

## Designed For

### Solo Play
Play alone with the GM handling all NPCs, encounters, and narration. The agent maintains
consistent NPC voices and tracks the world state across the session.

### Group Play
Run as a shared resource for a group playing over text (Discord, Slack, forum). Each player
sends their turn actions; the GM narrates results and manages the table.

### One-Shots
Drop the party into a self-contained adventure using the one-shot template in `gm-guide.md`.
Pre-generated characters are recommended; the GM can supply them on request.

### Campaigns
The GM maintains NPC knowledge states, world consequences, and faction standings across multiple
sessions. For long-running antagonists, use the NPC delegation protocol in `npc-delegation.md`
to spin up a dedicated subagent with its own goals and secrets.

---

## NPC Subagents

Significant NPCs — recurring villains, party allies, faction leaders — can be composed as
dedicated subagents using the template in `skills/npc-delegation.md`.

A delegated NPC subagent:
- Maintains a consistent voice and personality across all interactions
- Tracks what it knows and does not know independently from the GM
- Pursues its own goals between sessions
- Can be retired cleanly when its arc concludes

The GM agent orchestrates subagent creation and delegation; players interact with subagent NPCs
through the normal conversation interface.

---

## Rules Compliance

All creature stat blocks, rules text, and mechanics in this package are drawn from the **SRD 5.1**,
published under the Creative Commons Attribution 4.0 International License.

This package does not reference, reproduce, or depend on any trademarked game content outside the
SRD 5.1. It is compatible with any tabletop adventure RPG using the d20 system.

---

## Planned Additions

- `skills/world-building.md` — pantheons, factions, geography, city generation
- `skills/magic-items.md` — SRD 5.1 magic item catalog with attunement rules
- `skills/downtime.md` — downtime activities, crafting, training, carousing
- `skills/hex-crawl.md` — wilderness exploration, random encounters, travel rules
- `FIRMWARE-gritty.toml` — alternate persona variant with slower healing and higher lethality

---

## License

Apache 2.0 — same as Roboticus. Rules content is SRD 5.1 (CC BY 4.0).
