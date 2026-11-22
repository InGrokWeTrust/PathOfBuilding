# RF → Aurabot: anonymized level-26 baseline

**Status:** Corrected PoB export decoded and inspected, 2026-11-23. This is a documentation-only, user-supplied character snapshot — **not** a fresh execution of the PoB calculation engine and **not** a claim that the build has been optimised.

**Privacy:** Only anonymized build facts are recorded below. The original sharing code, character/account identifiers, account hashes, item UUIDs and personal import metadata are **not** stored in this public repository.

## Character and passive tree

- Scion, level **26**, with no ascendancy yet.
- Passive tree: game version **3.30**; 30 stored passive node IDs (including the class start); 2 mastery selections. Names/paths have not yet been independently mapped or assessed.
- Build selected primary skill: **Righteous Fire**.
- PoB's imported calculation settings affect displayed estimates; verify comparisons using consistent configuration.

## Skill groups as exported

| Gear slot | Current gems (exported levels) |
|---|---|
| Body armour, 4-link | Righteous Fire (3), Elemental Focus (3), Efficacy (6), Concentrated Effect (3) |
| Weapon 1, 3-link | Fire Trap (4), Trap and Mine Damage (3), Elemental Focus (3) |
| Weapon 2, 3-link | Shield Charge (7), Faster Attacks (6), Lifetap (6) |
| Helmet | Purity of Fire (1), Vitality (5) |
| Boots | Frostblink (1) |

PoB selected RF for its saved DPS results, so a separate Fire Trap burning-ground damage number is **not available** from this export's saved player stats. Change PoB's selected main skill to Fire Trap and record its burning-ground DPS for a comparable second reading.

## Exported PoB calculated statistics

| Stat | Saved value |
|---|---:|
| Righteous Fire damage over time | 674.2446 DPS |
| Maximum life | 773 |
| Life regeneration | 267.1/sec |
| Total build degeneration | 181.975/sec |
| Net life regeneration | **+85.125/sec** |
| Total mana | 313 |
| Unreserved mana | 129 (41.21%) |
| Armour | 806 |
| Energy shield | 46 |
| Attack block chance | 33% |
| Fire / cold / lightning resistance | 75% / 75% / 75% |
| Chaos resistance | 0% |

**Interpretation:** Saved net life regeneration is positive with the selected PoB setup; it does not guarantee sustain under all temporary debuffs, map modifiers or missing buffs.

## Equipment observations and recommended actions

1. **High priority — burning-removal mana flask.** An equipped `Grand Mana Flask of Damping` has `Removes all Burning when used`. Using it can switch off Righteous Fire. Replace its suffix if unintended.
2. **Next mobility upgrade — boots.** Exported `Steel Greaves` have life and resistances but no movement-speed suffix. Seek movement speed on a replacement pair while retaining enough life and resistances.
3. **Weapon scaling.** The exported sceptre's elemental-damage implicit helps RF, but its increased **spell damage** does not scale RF burning damage. Prefer increased fire/burning/damage-over-time modifiers when upgrading for RF.
4. **Existing RF links are functional.** Concentrated Effect boosts damage but makes RF radius smaller. For general clearing at level 31+, evaluate replacing Concentrated Effect with Burning Damage Support, retaining Elemental Focus and Efficacy. Compare in PoB, not by guessed DPS.
5. **Aura reservation:** Purity of Fire and Vitality are represented and use roughly 184 of 313 mana. Malevolence's 50% additional reservation does not presently fit without changing reservation efficiency or other auras.
6. **Lifetap correction:** Lifetap is level 6. Its cost multiplier remains 300% across levels; keeping level 1 is **not** inherently necessary to lower the supported skill's life cost. Lower levels mainly change the Lifetap buff acquisition threshold and damage bonus. Do not reset the gem just because of the earlier guidance.

Sources for game interactions:
- https://www.poewiki.net/wiki/Righteous_Fire
- https://www.poewiki.net/wiki/List_of_modifiers_for_mana_flasks
- https://poedb.tw/us/Lifetap_Support
- https://www.poewiki.net/wiki/Burning_Damage_Support

## Next checkpoint

- Replace (or intentionally retain as an emergency RF-off switch) the burning-removal flask.
- Add movement-speed boots when available.
- On character level 31, compare the 4-link RF alternatives in PoB.
- Record Fire Trap's own calculated burning-ground damage by selecting Fire Trap as the main skill.
- Create a separate level-75 aurabot target PoB configuration; no transition decision should be made on character level alone.
- No PoB game-calculation Lua code has been changed or tested in this checkpoint.
