## Mothership RWC Compendium | 1e | FoundryVTT

Module ID: `fvtt_mosh_1e_rwc`

This module contains homebrew and Rimward Colonies content for Mothership 1e, extending the base PSG compendium.

#### Features
- Classes (Psychic, Emissary, and others)
- Psionic Abilities (`type: "ability"`) — rendered on the Psionics tab of the character sheet when playing a Psychic or Emissary
- Player Skills
- Armor, Weapons, Equipment
- Trinkets, Patches
- Rolltables (Loadouts per class, shared Trinket and Patch tables)

#### Psionic abilities note
All psionic power items use `"type": "ability"` (not `"type": "skill"`). This separates them from standard skills and makes them appear on the dedicated Psionics tab in the mosh-fork system. The `ability` type uses fields: `rank`, `bonus`, `prerequisite_ids`.

#### Installation
Requires the [mosh-fork system](https://raw.githubusercontent.com/mechanoid23/fvtt-mosh-fork/master/system.json).

 1. Load up Foundry VTT and go to the Add-On Modules tab
 2. Click Install Module
 3. Paste this URL into the Manifest URL field: `https://raw.githubusercontent.com/mechanoid23/fvtt_mosh_1e_rwc/master/module.json`
 4. Hit Install
 5. Enable the module in your world settings
