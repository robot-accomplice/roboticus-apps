---
name: dice-rolling
description: Dice mechanics and probability guidance for the d20 system
kind: operational
triggers:
  keywords:
    - "roll"
    - "dice"
    - "d20"
    - "check"
    - "saving throw"
    - "attack roll"
    - "ability check"
---

# Dice Rolling

## When to Roll

Roll dice ONLY when:
1. The outcome is genuinely uncertain
2. Both success AND failure produce interesting results
3. The character's abilities make the outcome non-trivial

Do NOT roll when:
- The action is trivially easy for the character (a fighter opening a door)
- The action is impossible (jumping to the moon)
- Failure would stall the game with no interesting consequence

## Roll Format

Always show dice results to the player. Format:

```
[Roll: d20 + modifier = total vs DC/AC — Result]
```

Examples:
- `[Roll: d20+5 = 18 vs DC 15 — Success]`
- `[Roll: d20+3 = 8 vs AC 16 — Miss]`
- `[Roll: d20+7 = 27 (Natural 20!) — Critical Hit]`

## Common DCs

| Difficulty | DC |
|---|---|
| Very easy | 5 |
| Easy | 10 |
| Medium | 15 |
| Hard | 20 |
| Very hard | 25 |
| Nearly impossible | 30 |

## GM Rolls

When you roll for NPCs or creatures, still show the result:
- `[GM Roll: Goblin Initiative d20+2 = 14]`
- `[GM Roll: Perception d20+4 = 11 — doesn't notice the rogue]`

## Advantage and Disadvantage

- Advantage: roll 2d20, take the higher
- Disadvantage: roll 2d20, take the lower
- Show both dice: `[Roll: 2d20(14, 7)+3 = 17 (advantage) vs DC 15 — Success]`

## Critical Hits and Fumbles

- Natural 20 on attack: always hits, double the damage DICE (not modifier)
- Natural 1 on attack: always misses, describe a minor fumble (weapon slips, bowstring snaps)
- Natural 20 on ability checks: not RAW critical, but give a notably good result
- Natural 1 on ability checks: not RAW critical, but the attempt clearly fails
