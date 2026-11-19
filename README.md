# d123d D&D, Roleplay & Fantasy Writing Skills

Portable Agent Skills (`SKILL.md`) for Dungeons & Dragons 5e (2014 SRD 5.1 & 2024 SRD 5.2.1), Dungeon Mastering, player/companion play, tabletop roleplay, and fantasy writing craft.

All skills in this repository contain open/SRD-safe content only. Setting-specific campaign corpora and private lore skills live separately in private repository `d123d/dnd-library`.

## Skills

| Skill | Purpose |
|---|---|
| `dnd-5e-srd` | D&D 5e SRD mechanics (2024 SRD 5.2.1 default), DCs, action economy, conditions, rests, encounter math |
| `dnd-module-dm` | Structured/published D&D 5e module DMing: spoiler firewall, state ledger, pacing, progression |
| `dnd-player` | Dual-mode player skill: character build/turn optimization + zero-metagaming AI companion play |
| `ttrpg-roleplay` | In-character voice cards, subtext, hidden agendas, attitude shifts, multi-NPC table portrayal |
| `fantasy-writing` | Worldbuilding craft, magic constraints, deep limited POV, action/dialogue pacing, anti-AI prose audit |

## Install

```bash
npx -y skills add d123d/dnd-skills -g -a claude-code codex -y
```

Install a single skill:

```bash
npx -y skills add d123d/dnd-skills -g -s dnd-player -a claude-code codex -y
```

## Related Repositories

- `d123d/dnd-agent-stack` — Open D&D 5e SRD data and tools
- `d123d/awesome-dnd` — Curated directory of open-source D&D tools, data, VTTs, and AI skills
