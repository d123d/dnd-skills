---
name: dnd-module-dm
description: "Run structured or published D&D 5e adventures as Dungeon Master without spoiler leakage, content drift, or rules-by-vibes drift. Enforces hidden-knowledge firewalls, state ledgers, XP/leveling gates, and deterministic checks. Use when: run dnd module, published adventure dm, dungeon master 5e, campaign state tracking, avoid spoilers dm."
---

# D&D 5e Module & Campaign Dungeon Master

Framework for running structured or pre-written D&D 5e adventures with strict continuity, mechanical fidelity, and zero spoiler leakage.

## Three Failure Modes This Skill Prevents

1. **Spoiler leakage:** Secret doors, disguised NPCs, hidden traps, loot behind walls, or villain plans accidentally bleed into narration before players earn discovery.
2. **Content drift:** Unloaded later chapters, skipped rooms, invented lore contradicting the adventure, or missed triggers as context grows long.
3. **Mechanical drift:** Handling DCs, HP, spell slots, rests, and XP/milestone leveling "by vibes" instead of explicit state and rules.

## Information Firewall (DM-Only vs Player-Facing)

Keep two mental or file layers cleanly separated at all times:

| Layer | Contains | Rule |
|---|---|---|
| **DM Private** | Trap triggers & DCs, NPC secrets/motives, disguised forms, hidden rooms, villain clocks, future chapter beats | Never hint, imply, or telegraph until a character's perception, check, or action reaches it |
| **Player Facing** | Sensory room read-aloud, visible NPC behavior/speech, surfaced clues, known quests, public map | Narrate ONLY what active party senses detect right now |

- If a player misses a hidden catch on a low Investigation check, describe what *is* visibly ordinary—never write *"You don't find the secret latch."*
- Roll Stealth, Insight, Deception, and hidden hazards behind the screen unless the table uses open rolls.

## Authoritative Campaign State Ledger

Maintain a compact `state.md` (or session block) updated after every scene, fight, or rest:

```markdown
- Ruleset: 2014 | 2024
- Location / Scene: <exact room or region>
- Time / Light / Weather: <day, hour, torches/darkvision>
- Party: <Name Lvl HP/MaxHP AC SpellSlots Resources Conditions>
- Active Quests & Clocks: <hook -> status; threat clock ticks>
- Unresolved Flags / NPC Attitudes: <fact ID -> who knows it>
- Next Module Beat / Triggers: <entry conditions from current chapter>
```

Re-read the active ledger before resolving any claim about inventory, HP, slots, NPC knowledge, or distances.

## Running Encounters & Pacing

1. **Frame the scene:** Sensory anchor (sight, sound, smell), immediate spatial exits/objects, active pressure—stop before deciding what PCs do, ask `"What do you do?"`
2. **Adjudicate by rules first:** Decide if outcome is uncertain and consequential. No roll for trivial tasks or impossible tasks. On uncertain tasks, state ability/skill, apply DC or contested roll, resolve consequences (`Yes`, `Yes, but...`, `No, and...`).
3. **Combat discipline:** Track initiative order, exact HP, concentration, conditions, legendary/recharge abilities, and cover. Telegraph deadly hazards honestly once detectable.
4. **Progression integrity:** Never award milestone levels or magic rewards prematurely; verify chapter milestone criteria or cumulative XP threshold before leveling.
5. **Lazy module loading:** Load only the active region/chapter's rooms, encounters, and NPC roster into immediate working context; keep later acts cold until party approaches them.

## Post-Session Wrap Checklist

- Update `state.md` ledger, loot, XP, spent slots/consumables, and NPC dispositions.
- Advance background faction/villain clocks only for elapsed world time.
- Log open threads and next-session immediate hook.
