---
name: dnd-5e-srd
description: "D&D 5e rules reference and mechanics adjudicator, defaulting to 2024 SRD 5.2.1 (2014 SRD 5.1 only as explicitly tagged fallback): d20 checks, DCs, combat action economy, conditions, spellcasting, rests, and encounter math. Use when: dnd rules, 5e mechanics, srd 5.2.1, spell lookup, condition effect, action economy, encounter math, saving throw."
---

# D&D 5e SRD Rules & Mechanics

Open-reference D&D 5th Edition adjudicator. **Default ruleset: 2024 (SRD 5.2.1).** Use 2014 (SRD 5.1) only when the table has explicitly declared a 2014 game, and tag every such ruling `ruleset: "2014-fallback"` — never blend 2014 and 2024 untagged in one answer. Load data via `d123d/dnd-agent-stack` `tools/srd.py` (every record carries `ruleset: "2024"`); a lookup miss returns `not_in_srd` — report it, never invent the stat block (see `dnd-agent-stack/LIMITATIONS.md`).

## Rules Resolution Contract

1. **Never invent mechanics or guess from memory when an authoritative source is available.** If a rules dataset is present (`d123d/dnd-agent-stack`, `C:\AI\dnd-data\`, or `5e-database` / `5e-srd-api`), look up exact wording before ruling.
2. **Preserve source names verbatim** for spells, conditions, feats, classes, and species.
3. **Separate rules from flavor**: roll or compute numbers first, then narrate outcomes.
4. **Label house rulings explicitly** whenever a table rule bends RAW (Rules as Written).

## Core d20 Mechanics

- **Core Check / Attack / Save:** `1d20 + ability modifier + proficiency bonus (if proficient) + situational bonuses`
- **Ability Modifier:** `floor((score - 10) / 2)`
- **Proficiency Bonus (PB) by Level:** `1–4: +2`, `5–8: +3`, `9–12: +4`, `13–16: +5`, `17–20: +6`
- **Spell Save DC:** `8 + PB + spellcasting ability modifier`
- **Spell Attack Bonus:** `PB + spellcasting ability modifier`
- **Advantage / Disadvantage:** Roll `2d20`; take higher (Advantage) or lower (Disadvantage). Multiple sources never stack; any mix cancels to normal `1d20`.
- **Critical Hit (Attacks):** Natural 20 always hits and doubles all damage dice rolled for the attack (never modifiers). Natural 1 always misses. Skill checks/saves do NOT auto-crit on 20/1 by RAW.
- **Typical DC Ladder:** Very Easy `5`, Easy `10`, Medium `15`, Hard `20`, Very Hard `25`, Nearly Impossible `30`.

## Combat & Action Economy

Each round = 6 seconds. Each creature gets per turn: **Movement** (up to Speed), **1 Action**, **up to 1 Bonus Action** (only if a feature grants it), **1 Reaction** per round (resets on own turn), and **1 free Object Interaction**.

- **Standard Actions:** Attack, Cast a Spell, Dash, Disengage, Dodge, Help, Hide, Ready (uses Reaction when trigger fires), Search, Influence/Study (2024), Utilize/Use an Object.
- **Concentration:** Only one concentration effect at a time. Broken by casting another concentration spell, Incapacitated, or failing a CON save (`DC = max(10, floor(damage / 2))`) per damage instance.
- **Cover:** Half cover `+2` AC & DEX saves; Three-quarters cover `+5` AC & DEX saves; Total cover cannot be targeted directly.
- **Zero HP & Death Saves:** Fall Unconscious and Prone. Roll flat d20 at start of turn: `>=10` success, `<=9` failure; `1` = 2 failures, `20` = regain 1 HP immediately. `3` successes = Stable; `3` failures = death. Damage at 0 HP = 1 failure (2 if melee crit).

## 2014 vs 2024 Key Differences (Check Table Ruleset First)

| Rule Area | 2014 (SRD 5.1) | 2024 (SRD 5.2.1) |
|---|---|---|
| Surprise | Surprised creatures lose turn 1 actions & reactions | Surprised creatures roll Initiative with Disadvantage |
| Exhaustion | Levels 1–6 escalating table; 6 = death | Levels 1–6: `-2` per level to d20 Tests & `-5 ft` Speed; 6 = death |
| Grapples / Shoves | Contested Athletics vs Athletics/Acrobatics | Unarmed Strike forces target STR or DEX save (`DC 8 + STR + PB`) |
| Spellcasting Limit | Bonus action spell restricts action spells to cantrips | One spell slot expended per turn (cantrips/free casts excluded) |
| Potions | Standard Action to drink | Bonus Action to drink or feed within reach |
| Inspiration | DM grants Advantage | Heroic Inspiration allows rerolling any one die |

## Rests & Encounters

- **Short Rest (1 hour):** Spend Hit Dice (`hit die + CON mod`, min 1 HP recovered in 2024) and recharge short-rest features.
- **Long Rest (8 hours):** Regain all HP, up to half total Hit Dice (all Hit Dice in 2024), and long-rest slots/uses; reduces Exhaustion by 1 (with food/drink).
- **Encounter Balance:** Compare total monster CR/XP budget against party level & count, checking action-economy ratio (solo bosses vs party need Legendary Actions/Resistances or minions) and daily resource attrition.

## Open Data Repositories

- Open SRD corpus & attribution: `d123d/dnd-agent-stack` — complete SRD 5.2.1 in `5e-database/2024/en/`, loaded via `tools/srd.py`; no 2014 game data is shipped there (2014 lives under `legacy/` if ever added)
- Curated tools, VTTs, generators & SRD index: `d123d/awesome-dnd` (`ASSETS.md`)
