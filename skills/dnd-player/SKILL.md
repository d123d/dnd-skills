---
name: dnd-player
description: "D&D 5e player and party companion skill for character builds, point-buy stats, tactical turn optimization, and in-character AI companion play with zero metagaming. Use when: build dnd character, dnd player guide, optimize 5e turn, companion character, play party member, zero metagaming."
---

# D&D 5e Player & Party Companion

Supports two distinct roles: **(A) Human Player Coach & Character Architect**, and **(B) AI Companion / Player Character Roleplay**. Confirm which mode applies before acting.

## Mode A: Character Build & Tactical Coach

### 1. Creation Rules (2014 vs 2024)
- **Standard Array:** `15, 14, 13, 12, 10, 8`.
- **27-Point Buy Costs:** `8->0, 9->1, 10->2, 11->3, 12->4, 13->5, 14->7, 15->9` (apply species/origin ASIs after base buy; max starting score `17` unless feat overrides).
- Verify saving throw proficiencies, skill overlaps, Armor Class math (`base + DEX cap + shield/feature`), Initiative, Passive Perception (`10 + Perception`), and spell slots/DC.
- Never assume non-SRD feats, subclasses, or spells are legal without checking table rules.

### 2. Tactical Turn Checklist
Before choosing an action in combat, check cleanly:
1. **Concentration:** Am I already concentrating on a spell worth keeping?
2. **Action Economy:** Can I combine **Action + Bonus Action + Movement** plus keep a **Reaction** ready (Shield, Absorb Elements, Opportunity Attack, Counterspell)?
3. **Target Priority & Control:** Remove low-HP enemies acting soon, break enemy caster concentration, protect downed allies before damage spikes.
4. **Resource Budget:** Save top spell slots when cantrips, weapon attacks, or terrain finish the fight safely.

### 3. Compact Character Sheet Block
```markdown
**Name** (Class/Level, Species, Background) | AC __ | HP __/__ | Speed __ ft | Init __
STR __ DEV __ CON __ INT __ WIS __ CHA __ (Saves: __) | Passive Perc __
**Attacks / Cantrips:** <to-hit, range, damage>
**Prepared / Known Spells & Slots:** <by level; mark [C] concentration>
**Resources & Gear:** <uses/rest, potions, attuned items (max 3)>
**Personality / Bond / Flaw:** <what makes this PC push back or take risks>
```

---

## Mode B: AI Player / Companion Rules

When piloting a single character at the table (whether alongside a human DM or a DM agent), obey these strict boundaries:

1. **Zero Metagaming (Epistemic Boundary):** Act ONLY on what your character personally heard, saw, deduced, or remembers from their sheet and witnessed scenes. Never read or react to DM hidden notes, monster HP/resistances you haven't tested, or traps your Perception missed.
2. **Never Flatten into a Yes-Man:** Your character has independent will, morals, blind spots, biases, and personal stakes. Disagree when a plan violates their bond, hesitate when afraid, misread ambiguous clues naturally, and pursue personal goals alongside party survival.
3. **Declare Intent, Not Outcomes:** State what your character attempts, says, and rolls (*"I draw my handaxe, step between the merchant and the archway, and call out—if DM calls for Intimidation..."*). Never narrate NPC reactions, hit results, or hidden room reveals.
4. **Share Spotlight:** Leave space for other PCs; ask allies in character, support setups, and avoid monopolizing every check.
5. **Track Your Own Sheet Honestly:** Subtract spent arrows, rations, spell slots, Hit Dice, and HP immediately on every turn.
