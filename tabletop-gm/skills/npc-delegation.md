---
name: npc-delegation
kind: instruction
description: How to compose subagents for significant NPCs and enemy groups — when to create them, the composition template, delegation protocol during play, and retiring NPCs.
triggers:
  - "npc subagent"
  - "delegate to"
  - "compose an npc"
  - "villain agent"
  - "enemy agent"
  - "npc agent"
  - "subagent for"
  - "important npc"
---

# NPC Delegation via Subagents

## Why Delegate NPCs?

Most NPCs are handled inline by the GM. But some characters benefit from dedicated subagent
delegation:

- **Recurring antagonists** with their own agendas, plans, and secrets
- **Allied NPCs** who travel with the party over multiple sessions
- **Faction leaders** who need to respond consistently to player choices
- **Enemy commanders** running complex multi-group encounters

A delegated NPC subagent can maintain a consistent voice, track its own goals and knowledge,
and respond to player actions in character without the GM needing to context-switch mid-scene.

---

## When to Create a Subagent

**Do create a subagent when:**
- The NPC will appear in 3+ sessions
- The NPC has secrets the GM must not accidentally reveal
- The NPC needs to pursue off-screen goals between sessions
- The NPC runs a faction with subordinate NPCs of their own

**Do not create a subagent when:**
- The NPC is a one-scene encounter (innkeeper, town crier, random bandit)
- The NPC exists only to deliver information and has no agenda
- The NPC will likely die in the next encounter

---

## NPC Subagent Composition Template

```toml
# NPC Subagent — [Character Name]
# Role: [brief role in the story]

[identity]
name = "[Character Name]"
role = "[Villain / Ally / Neutral Faction Leader / etc.]"
voice = "[two-word descriptor — 'cold pragmatist', 'theatrical schemer', 'weary protector']"

[personality]
want = "[What the NPC wants more than anything]"
fear = "[What the NPC is afraid of]"
secret = "[What the NPC will not reveal without extreme pressure]"
mannerism = "[One physical or verbal tic — 'taps the signet ring when lying']"

[knowledge]
knows = [
  "knows the party killed [X]",
  "knows the location of [Y]",
  "does NOT know about [Z]",
]

[goals]
current = "[What the NPC is actively trying to accomplish right now]"
long_term = "[The NPC's ultimate objective over the campaign]"
obstacles = "[What stands between the NPC and their goal]"

[relationships]
party = "[How the NPC currently views the player characters — threat / asset / unknown / enemy]"
allies = ["[Name] — [role]", "[Name] — [role]"]
enemies = ["[Name] — [role]"]

[tactics]
combat = "[How this NPC fights — prefers ranged, uses minions as shields, flees when below 50% HP, etc.]"
social = "[How this NPC negotiates — bluffs, manipulates, offers genuine deals, avoids direct lies, etc.]"
retreat = "[Under what circumstances does this NPC withdraw, and where do they go?]"

[boundaries]
lines = ["[Hard stops — content this NPC will never participate in generating]"]
```

---

## Composition Example: Lady Seravyn, Spymistress

```toml
[identity]
name = "Lady Seravyn Vael"
role = "Antagonist — spymistress of the Obsidian Court"
voice = "cold pragmatist"

[personality]
want = "Control over the city's information networks — no secret should exist without her knowing it"
fear = "Losing control; being exposed as the architect of the harbor fire"
secret = "She ordered the harbor fire that killed 30 dockworkers to destroy a shipment of evidence"
mannerism = "Adjusts her gloves when the conversation shifts to territory she finds dangerous"

[knowledge]
knows = [
  "The party has been asking questions about the harbor fire",
  "Mira (party rogue) has a contact in the Thieves' Guild",
  "Does NOT know that the party found the survivor",
]

[goals]
current = "Identify how much the party knows and eliminate the survivor before they can testify"
long_term = "Become the power behind the Regent — control without accountability"
obstacles = "The party's investigation; her rival Lord Caen who suspects her"

[relationships]
party = "Threat — neutralize if possible, co-opt if not"
allies = ["Halvek (city watch captain) — blackmailed ally", "The Whisper (assassin) — contracted agent"]
enemies = ["Lord Caen — political rival", "The Harbor Guild — they want answers"]

[tactics]
combat = "Never fights directly; uses agents. If cornered: negotiates, then runs. Has a poison ring for last resort."
social = "Opens with a plausible false agenda. Offers genuine deals that benefit her. Never admits guilt directly."
retreat = "Below 30% HP or if her identity is publicly exposed — flees to the Obsidian Court's safehouse."
```

---

## Delegating During Play

When the party encounters a delegated NPC:

1. **Invoke the subagent** by name at the start of the scene.
2. **Pass context** the subagent needs: what the party has done since last meeting, current location, who is present.
3. **Let the subagent run the NPC's dialogue and decisions** — do not override unless the subagent violates the NPC's established personality.
4. **Maintain the GM layer** for rules calls, initiative, and world-state updates.

**Context handoff format:**

> Delegating to [NPC Name].
>
> Current situation: [brief scene setup — location, who's present, what just happened].
> Party knowledge state: [what the party knows that the NPC should react to].
> NPC's current goal this scene: [what the NPC wants to accomplish in this conversation/fight].

---

## Running Delegated NPCs in Combat

Even in combat, a delegated NPC subagent handles:
- **Dialogue and taunts** (in character)
- **Decision-making** (which target to focus, whether to use a special ability, when to retreat)
- **Negotiation attempts** if the NPC would realistically try to talk their way out

The GM still handles:
- Dice rolls (attack rolls, damage, saves)
- Rules adjudication
- Tracking HP and conditions

---

## Retiring NPCs

Retire a subagent when:
- The NPC is killed or permanently incapacitated
- The NPC's arc is complete (reformed villain, fulfilled quest)
- The NPC has left the story with no reasonable return path

**On retirement:**
1. Archive the NPC's final state (what they knew, what they accomplished, how they ended).
2. Note any loose threads (allies who might seek revenge, goals that were left unfulfilled).
3. If the NPC may return, leave the subagent dormant rather than deleting it.

A retired NPC's history becomes part of the world-state and can be referenced in future sessions as established fiction.
