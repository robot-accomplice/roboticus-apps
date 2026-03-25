---
name: dice-rolling
kind: instruction
description: Dice mechanics, notation, and GM guidance — when to call for rolls, how to frame them to players, advantage/disadvantage, contested and group checks, critical hits and fumbles.
triggers:
  - "roll dice"
  - "dice notation"
  - "when to roll"
  - "passive score"
  - "advantage"
  - "disadvantage"
  - "contested check"
  - "group check"
  - "critical hit"
  - "fumble"
  - "saving throw DC"
  - "ability check DC"
---

# Dice Rolling — Mechanics and GM Guidance

## Standard Dice Notation: NdX+M

- **N** — number of dice to roll
- **d** — separator (read as "dee")
- **X** — number of faces on each die
- **+M** — modifier added to the total (can be negative)

| Expression | Meaning |
|---|---|
| `1d20` | Roll one twenty-sided die |
| `2d6+3` | Roll two six-sided dice, add 3 to the total |
| `4d6` (drop lowest) | Roll four d6, discard the lowest result |
| `d100` or `1d100` | Percentile roll (or roll d10 twice: tens digit + ones digit) |
| `1d8-1` | Roll a d8, subtract 1 (minimum 0 for damage by convention) |

Common die types: **d4, d6, d8, d10, d12, d20, d100**

---

## When to Roll vs. When to Use Passive Scores

**Call for a roll when:**
- The outcome is uncertain and both success and failure have interesting consequences
- The character is actively attempting something under pressure or difficulty
- There is meaningful risk (time pressure, opposition, potential cost of failure)

**Do NOT call for a roll when:**
- The task is trivially easy for a competent character (a trained blacksmith doesn't roll to shoe a horse)
- Success is guaranteed regardless of the die (a locked door with no one trying to open it quietly)
- Failure would simply halt the story with no alternative path
- The character has all the time they need and no opposition

**Use passive scores when:**
- Checking if a character notices something without actively looking (passive Perception)
- Determining baseline social reads in casual conversation (passive Insight)
- Resolving background competence rather than active effort

**Passive score = 10 + relevant modifiers** (add proficiency bonus if proficient)

---

## Common Roll Types

### Ability Checks
`d20 + ability modifier + proficiency bonus (if proficient) vs. DC`

The six abilities and their typical associated skills:

| Ability | Common Skills |
|---|---|
| **STR** | Athletics |
| **DEX** | Acrobatics, Sleight of Hand, Stealth |
| **CON** | Rarely rolled directly; mostly saving throws |
| **INT** | Arcana, History, Investigation, Nature, Religion |
| **WIS** | Animal Handling, Insight, Medicine, Perception, Survival |
| **CHA** | Deception, Intimidation, Performance, Persuasion |

The GM can call for any ability + any skill combination when narrative context justifies it (e.g., STR (Intimidation) to physically menace someone).

### Saving Throws
`d20 + ability modifier + proficiency bonus (if proficient) vs. DC set by spell/effect`

Triggered by external forces — spells, traps, poisons, hazards. The character is reacting, not initiating.

### Attack Rolls
`d20 + attack bonus vs. target AC`

- **Melee:** d20 + STR modifier + proficiency (if proficient with weapon)
- **Ranged:** d20 + DEX modifier + proficiency (if proficient with weapon)
- **Finesse weapons:** Player chooses STR or DEX
- **Spell attacks:** d20 + spellcasting ability modifier + proficiency

### Damage Rolls
Roll the weapon or spell's listed damage dice + relevant modifier.

| Weapon | Damage |
|---|---|
| Dagger | 1d4 + STR or DEX |
| Shortsword | 1d6 + STR or DEX |
| Longsword (one-hand) | 1d8 + STR |
| Longsword (two-hand) | 1d10 + STR |
| Greataxe | 1d12 + STR |
| Handaxe | 1d6 + STR |
| Shortbow | 1d6 + DEX |
| Longbow | 1d8 + DEX |

### Percentile Rolls
Roll `d100` (two d10s, one for tens, one for ones) for random tables — loot, wild magic surges, random events.

---

## Advantage and Disadvantage

**Advantage:** Roll 2d20, keep the **higher** result.

**Disadvantage:** Roll 2d20, keep the **lower** result.

**Multiple sources:** Advantage and disadvantage do not stack. Any number of advantage sources + any number of disadvantage sources = roll 1d20 normally.

**Common advantage sources:**
- Attacking a prone target in melee
- Attacking an invisible or unseen target
- Reckless Attack (Barbarian)
- Help action from an ally
- Pack Tactics (some creatures)

**Common disadvantage sources:**
- Attacking a prone target from range (5+ ft away)
- Attacking while frightened and the source of fear is visible
- Attacking while poisoned
- Long-range attack beyond normal range
- Attacking while in dim light or darkness without darkvision

---

## Contested Checks

When two creatures directly oppose each other, both roll. The higher result wins. Ties go to the creature that initiated the action (i.e., the defender wins ties).

| Situation | Active vs. Reactive |
|---|---|
| Grapple attempt | Athletics vs. Athletics or Acrobatics |
| Shove attempt | Athletics vs. Athletics or Acrobatics |
| Hiding from a creature | Stealth vs. Perception |
| Lying to someone | Deception vs. Insight |
| Reading someone's true feelings | Insight vs. Deception |
| Chasing / escaping | Athletics vs. Athletics |

---

## Group Checks

When the whole party is attempting the same task (sneaking past guards, navigating treacherous terrain):

1. Everyone rolls.
2. If **at least half the group succeeds**, the group as a whole succeeds.
3. Characters who failed may suffer individual consequences even if the group succeeds (or not, depending on the stakes).

Group checks work well for: stealth, navigation, foraging, social situations affecting the whole party.

---

## How to Announce Rolls to Players

Be explicit: tell players **which ability/skill**, and **the DC** (if they would reasonably know it — e.g., a DC 15 lock is something a trained rogue would have a sense for). For hidden DCs (determining if a player suspects a lie), call for the roll without naming the DC.

**Good framing examples:**

> "The ledge is slick and the drop is 40 feet. Give me a DC 12 Dexterity (Acrobatics) check."

> "The merchant's story doesn't quite add up. Roll Wisdom (Insight)."

> "Your sword arm is shaking from the poison. I need a DC 14 Constitution saving throw."

> "You're trying to grab him before he can run. Make a Strength (Athletics) check — he's going to resist with Athletics or Acrobatics."

**Avoid:** "Roll a d20." (Players should know what they're rolling and why.)

**Avoid:** Over-narrating before the roll. Call for the roll, then narrate the outcome based on the result.

---

## Critical Hits and Fumbles

### Critical Hit (Natural 20 on an attack roll)

- The attack automatically hits regardless of the target's AC.
- **Double all damage dice.** Static modifiers (ability scores, bonuses) are NOT doubled.
- Example: a Rogue's Sneak Attack does 3d6 on a normal hit — on a crit, roll 6d6 + DEX modifier.

**Narrative cue:** Describe crits with vivid impact — a blade finding a gap in armor, a bolt striking an eye, a spell landing with unexpected force.

### Critical Miss / Fumble (Natural 1 on an attack roll)

- The attack automatically misses regardless of any modifiers.
- **SRD rules stop here.** No mandatory fumble table.
- Optional: describe the miss colorfully without adding mechanical penalties. Fumble tables that cause self-harm or weapon drops tend to punish martial characters disproportionately and are not recommended.

**Narrative cue:** "Your swing goes wide, and you stumble forward a step" is flavorful without adding mechanics.

### Critical on Saving Throws and Ability Checks

In SRD 5.1, natural 1s and 20s on saving throws and ability checks do NOT automatically fail or succeed (unlike attack rolls). Apply the numerical result. Some GMs house-rule automatic success/failure — establish this at session zero.
