# CLAUDE.md — fvtt_mosh_1e_rwc

Module ID: `fvtt_mosh_1e_rwc`

## Format

NeDB compendium packs — one JSON document per line in `.db` files under `packs/`. Edit directly as text.

## Pack contents

| Pack file | Content |
|---|---|
| `items_classes_1e.db` | Class items (`type: "class"`) |
| `items_skills_1e.db` | Skill items (`type: "skill"`) AND psionic ability items (`type: "ability"`) |
| `rolltables_1e.db` | Loadout rolltables per class; shared Trinket and Patch tables |

## Psionic abilities

Items with `"img": "modules/fvtt_mosh_1e_rwc/icons/psionic.png"` use `"type": "ability"`, NOT `"type": "skill"`. This is required for the mosh-fork system to display them on the Psionics tab instead of the Skills tab.

The `ability` item schema (from `module/data/items/ability-data.js` in the system):
```json
{
  "type": "ability",
  "system": {
    "description": "<HTML>",
    "rank": "Trained",
    "bonus": 10,
    "prerequisite_ids": []
  }
}
```

## Adding a new class

See the project-level `CLAUDE.md` at the workspace root for the full schema. Key fields:
- `choose_skill_or` stores groups as nested arrays: `[[opt1, opt2], [opt3]]`. Each group is an array of option objects with `{name, trained, expert, master, expert_full_set, master_full_set, from_list}`.
- The system's TypeDataModel schema for this field is `ArrayField(ArrayField(ObjectField))` — the nesting is essential.

## Skill UUIDs

Full format: `Compendium.fvtt_mosh_1e_rwc.items_skills_1e.Item.<suffix>`

See project-level `CLAUDE.md` for the full PSG skill UUID table. RWC-specific skills follow the same pattern.
