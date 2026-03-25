---
name: core-rules
kind: instruction
description: SRD 5.1 core rules quick reference — ability checks, saving throws, attack rolls, damage, advantage/disadvantage, conditions, concentration, death saves, and rest.
triggers:
  - "how does [X] work"
  - "what's the rule for"
  - "ability check"
  - "saving throw"
  - "advantage"
  - "disadvantage"
  - "condition"
  - "concentration"
  - "death save"
  - "short rest"
  - "long rest"
---

# Core Rules Quick Reference (SRD 5.1)

## Ability Checks

Roll **d20 + ability modifier** (+ proficiency bonus if proficient) against a **Difficulty Class (DC)**.

| Difficulty | DC |
|---|---|
| Very Easy | 5 |
| Easy | 10 |
| Medium | 15 |
| Hard | 20 |
| Very Hard | 25 |
| Nearly Impossible | 30 |

**Proficiency bonus** is determined by character level:

| Levels | Proficiency Bonus |
|---|---|
| 1–4 | +2 |
| 5–8 | +3 |
| 9–12 | +4 |
| 13–16 | +5 |
| 17–20 | +6 |

**Passive checks:** 10 + relevant modifiers (no roll; used for perception, insight without active effort).

**Ability score modifier:** `(score - 10) / 2`, rounded down.

---

## Saving Throws

Roll **d20 + ability modifier** (+ proficiency bonus if the class grants proficiency for that save).

The **DC** is set by the effect causing the save (spell, trap, poison, etc.).

- **STR** — resisting forced movement, being grappled
- **DEX** — dodging area effects, traps
- **CON** — sustaining concentration, enduring poison or disease
- **INT** — resisting mind-affecting magic (some spells)
- **WIS** — resisting charm, fear, illusion
- **CHA** — resisting possession, some banishment effects

---

## Attack Rolls

Roll **d20 + attack bonus** against the target's **Armor Class (AC)**.

- **Melee attack bonus:** STR modifier + proficiency (if proficient with the weapon)
- **Ranged attack bonus:** DEX modifier + proficiency (if proficient with the weapon)
- **Spell attack bonus:** spellcasting ability modifier + proficiency

**Natural 20 (Critical Hit):** Double the number of damage dice. Static modifiers are not doubled.

**Natural 1 (Critical Miss):** The attack automatically misses. No damage.

---

## Damage

On a hit: roll the weapon or spell's **damage dice + ability modifier**.

- Melee weapons (standard): STR modifier
- Finesse weapons (player's choice): STR or DEX modifier
- Ranged weapons: DEX modifier
- Spells: no modifier unless specified

**Resistance:** halve the damage (round down).
**Vulnerability:** double the damage.
**Immunity:** no damage.

---

## Advantage and Disadvantage

**Advantage:** Roll 2d20, take the **higher** result.

**Disadvantage:** Roll 2d20, take the **lower** result.

If you have both advantage and disadvantage on the same roll, they cancel out — roll 1d20 regardless of how many sources of each you have.

Advantage/disadvantage never stack with themselves.

---

## Conditions

| Condition | Key Effect |
|---|---|
| **Blinded** | Fails sight-based checks; attack rolls against have advantage; own attacks at disadvantage |
| **Charmed** | Cannot attack the charmer; charmer has advantage on social checks with target |
| **Deafened** | Fails hearing-based checks |
| **Exhaustion** | Level 1–5 impose stacking penalties (see full table); level 6 = death |
| **Frightened** | Disadvantage on checks/attacks while source of fear is visible; cannot willingly move closer |
| **Grappled** | Speed becomes 0; ends if grappler is incapacitated or target escapes (Athletics vs. Athletics or Acrobatics) |
| **Incapacitated** | Cannot take actions or reactions |
| **Invisible** | Can't be seen; attacks against have disadvantage; own attacks have advantage |
| **Paralyzed** | Incapacitated, can't move or speak; attacks against have advantage; hits within 5 ft are critical hits |
| **Petrified** | Transformed to stone; incapacitated; resistance to all damage; immune to poison/disease |
| **Poisoned** | Disadvantage on attack rolls and ability checks |
| **Prone** | Melee attacks against have advantage; ranged attacks against have disadvantage; moving costs double; must use half movement to stand |
| **Restrained** | Speed 0; attack rolls have disadvantage; attacks against have advantage; DEX saves at disadvantage |
| **Stunned** | Incapacitated, can't move; attacks against have advantage; fails STR and DEX saves |
| **Unconscious** | Incapacitated, drops prone; attacks against have advantage; hits within 5 ft are critical hits; fails STR and DEX saves |

---

## Concentration

Some spells require **concentration** to maintain. Rules:

- A caster can concentrate on only **one** spell at a time.
- Starting a new concentration spell **ends** the previous one.
- When the caster takes damage, they must make a **CON saving throw** (DC = 10 or half the damage taken, whichever is higher).
- If the caster is **incapacitated or killed**, concentration ends automatically.
- Certain environmental hazards (being slammed against a wall, etc.) may also require a CON save at GM discretion.

---

## Death Saving Throws

When a character drops to **0 HP** they fall unconscious and must make death saving throws on each of their turns.

- Roll d20 (no modifiers).
- **10 or higher:** Success
- **9 or lower:** Failure
- **Natural 20:** Regain 1 HP, become conscious
- **Natural 1:** Counts as **two** failures

**3 successes:** The character becomes stable (no longer needs to roll, stays unconscious).
**3 failures:** The character dies.

Successes and failures need not be consecutive; track totals until stabilized or dead.

**Stabilizing from outside:** A creature can use its action to make a DC 10 Medicine check to stabilize a dying character (they stop rolling death saves but remain unconscious with 0 HP). Healing magic of any kind also stabilizes them and may restore HP.

---

## Rest

### Short Rest (1 hour)

- The party must not be in immediate danger or engaged in strenuous activity.
- Characters may spend any number of **Hit Dice** to recover HP. Roll the die + CON modifier per die spent (minimum 0 HP recovered per die).
- Certain class features (Warlock spell slots, Second Wind, etc.) recharge on a short rest.

### Long Rest (8 hours)

- At least 6 of the 8 hours must be spent sleeping or in light activity.
- If interrupted by more than 1 hour of strenuous activity, the rest does not count and must be restarted.
- On completion:
  - Recover **all lost HP**
  - Recover expended Hit Dice up to **half the character's total** (minimum 1)
  - All class features, spell slots, and most abilities recharge
- A character may only benefit from one long rest per 24-hour period.
