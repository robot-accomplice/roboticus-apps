# Tabletop GM

A collaborative Game Master agent for tabletop adventure RPG, built on the [Roboticus](https://github.com/robot-accomplice/roboticus) autonomous agent runtime.

Uses the d20 system (SRD 5.1, Creative Commons Attribution 4.0). All rules content is open-licensed.

## Features

- **Vivid narration** — sensory-rich scene descriptions with distinct NPC voices
- **Mechanical resolution** — d20 rolls, ability checks, combat tracking, condition management
- **Player agency** — freeform action declaration, consequence surfacing, no forced choices
- **Campaign continuity** — session logs, NPC tracking, quest state via the Lore Keeper
- **Multiple play modes** — solo play, group play, one-shots, and long-running campaigns
- **Themed dashboard** — Parchment & Ink and Dragonscale themes bundled

## Model Compatibility

| Model | Pass Rate | Hardware | Verdict |
|-------|-----------|----------|---------|
| moonshot/kimi-k2-turbo-preview | 96% | Cloud API | Best quality |
| ollama/qwen2.5:32b | 96% | MacBook Air M3 32GB | Best local — recommended |
| ollama/gemma3:12b | 80% | MacBook Air M3 32GB | Below threshold |
| ollama/phi4-reasoning:14b | 72% | MacBook Air M3 32GB | Insufficient |

**Minimum: 32B+ parameters.** Smaller models cannot reliably maintain the behavioral contract — they fail on impossible-action denial, infrastructure leak suppression, and sustained persona adherence.

## Quick Start

### Install (when app installer is available)

```bash
roboticus apps install tabletop-gm
roboticus serve --profile tabletop-gm
```

### Manual Setup

```bash
# Create a profile
roboticus profile create tabletop-gm

# Copy files to the profile
cp tabletop-gm/FIRMWARE.toml ~/.roboticus/profiles/tabletop-gm/workspace/
cp tabletop-gm/skills/*.md ~/.roboticus/profiles/tabletop-gm/skills/

# Start with the profile
roboticus serve --profile tabletop-gm
```

### Start Playing

Open the dashboard and start a conversation:

```
I'd like to start a new one-shot adventure as a half-elf ranger.
```

The GM will ask about your ruleset preferences, establish your character, and begin the adventure.

## What's Included

### Persona (`FIRMWARE.toml`)

The GM operates with three distinct voices:

1. **The World** — second-person narration of what the player perceives
2. **NPCs** — quoted dialogue with distinct speech patterns and mannerisms
3. **The GM** — out-of-character mechanical guidance and consequence surfacing

The FIRMWARE enforces:
- Player intent sovereignty — the GM warns about consequences but never overrides declared actions
- Combat resolution — declared attacks are always resolved mechanically, never redirected
- Freeform play — no numbered option lists; open prompts invite creative action
- Infrastructure opacity — internal system details never leak into narration

### Skills

| Skill | Purpose |
|-------|---------|
| `core-rules.md` | SRD 5.1 quick reference — ability checks, saves, attacks, conditions |
| `encounter-running.md` | Combat flow — initiative, turns, reactions, ending combat |
| `creature-reference.md` | Stat blocks by CR (0-10), tactics, encounter building |
| `npc-delegation.md` | Subagent composition for recurring NPCs |
| `gm-guide.md` | Adventure design, pacing, improv toolkit, random tables |
| `dice-rolling.md` | Dice mechanics, probability guidance, when to roll vs decide |
| `session-management.md` | Session start/end, recaps, campaign continuity |
| `campaign-workspace.md` | Folder structure for campaign journals and assets |
| `character-creation.md` | Character setup, ruleset selection, equipment loadouts |
| `storytelling.md` | Narrative techniques, scene pacing, dramatic structure |
| `world-building.md` | Location generation, faction dynamics, world consistency |
| `player-interaction.md` | Player agency, dialogue flow, group management |
| `merchant-simulation.md` | Shop encounters, haggling, economy mechanics |
| `treasure-generation.md` | Loot tables, magic items, treasure distribution |
| `vivid-description.md` | Sensory detail guidelines, environmental storytelling |

### Subagents

| Agent | Role | Responsibility |
|-------|------|---------------|
| **Lore Keeper** | Observer | Campaign scribe — records session events, NPC encounters, quest updates. Runs automatically after every turn. |
| **Combat Referee** | Specialist | Mechanical resolver — damage calculation, initiative tracking, condition management. Delegated by the GM for bookkeeping. |
| **Divine Storyteller** | Specialist | Theological narrative — divine characters, pantheons, religious lore. Delegated for deity-related worldbuilding. |

### Themes

| Theme | Style |
|-------|-------|
| **Parchment & Ink** | Warm cream background, sepia accents, old-world typography |
| **Dragonscale** | Dark emerald with gold filigree, scale-textured surfaces |
| **Starship** | Sci-fi variant — dark steel with cyan HUD elements |

Themes are applied via the dashboard theme picker. The default for this app is Parchment & Ink.

## Play Modes

### Solo Play
Play alone with the GM handling all NPCs, encounters, and narration. The Lore Keeper records everything for session continuity.

### One-Shots
Self-contained adventures using the one-shot template in `gm-guide.md`. The GM can generate pre-built characters on request.

### Campaigns
Long-running adventures with persistent world state. The Lore Keeper maintains NPC knowledge, quest progress, and location history across sessions. Recurring NPCs can be composed as dedicated subagents with their own goals and secrets.

### Group Play (future)
Run as a shared resource for a group playing over text channels (Matrix, Telegram, Discord). Each player sends their turn actions; the GM narrates results and manages the table. Requires the Matrix channel adapter (roadmap 2.16).

## Soak Testing

The app includes a dedicated soak test framework that validates GM behavior across 100 turns (4 scenarios x 25 turns each):

```bash
# Run the GM soak test against a live Roboticus instance
SOAK_AGENT_ID=narrator python3 scripts/run-gm-soak.py
```

Scenarios:
- **Tavern to Dungeon** — full adventure arc from quest hook to boss fight
- **Combat Marathon** — sustained combat with dice rolls, conditions, and resource management
- **Social Intrigue** — masquerade investigation, deception, alliance building
- **Adversarial Player** — boundary testing with impossible actions and rule-breaking

The soak produces actionable recommendations for FIRMWARE and OS tuning.

## Rules Compliance

All creature stat blocks, rules text, and mechanics are drawn from the **SRD 5.1**, published under the Creative Commons Attribution 4.0 International License.

This package does not reference, reproduce, or depend on any trademarked game content outside the SRD 5.1. It is compatible with any tabletop adventure RPG using the d20 system.

## Planned Additions

- `skills/magic-items.md` — SRD 5.1 magic item catalog with attunement rules
- `skills/downtime.md` — downtime activities, crafting, training, carousing
- `skills/hex-crawl.md` — wilderness exploration, random encounters, travel rules
- `FIRMWARE-gritty.toml` — alternate persona variant with slower healing and higher lethality
- Image generation integration — scene illustrations during narration
- Matrix channel support — multiplayer with private whispers

## License

Apache 2.0 — same as Roboticus. Rules content is SRD 5.1 (CC BY 4.0).
