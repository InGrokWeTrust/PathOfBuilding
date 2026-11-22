# RF → Aurabot: level-26 Fire Trap snapshot

**Status:** Companion analysis for the user-provided Fire Trap-selected PoB export, 2026-11-23. These are **saved Path of Building PlayerStat fields**, not a new PoB calculation or a full replay of the character. Keep this as an observational snapshot.

**Privacy:** The raw encoded build, account/character identifiers, OAuth data and item unique IDs are not included in this public repository.

## Selected Fire Trap calculation

| PoB saved field | Value |
|---|---:|
| Class / level | Scion / 26 |
| Selected main skill | Fire Trap (inferred from trap-specific selected-skill stats and user's explicit switch) |
| `BurningGroundDPS` | **126.32798678544** |
| `TotalDPS` (hit DPS) | **76.0137** |
| `CombinedDPS` (hit + DoT for selected skill) | **202.34168678544** |
| `TrapThrowingTime` | **0.66666666666667 seconds** |
| `ManaCost` | **16** |
| `ManaPerSecondCost` (PoB model) | **24** |
| `AreaOfEffectRadiusMetres` | **1.6** |

**Interpretation:** Fire Trap has a direct hit and a separate burning-ground damage-over-time effect. The saved combined figure is the selected skill's PoB output, **not** the total combined RF-plus-Fire-Trap boss DPS. The previously recorded RF snapshot had 674.2446 RF DoT DPS; its configuration and build snapshot may differ, so don't treat an exact sum as validated.

## Saved character defense comparison

| Metric | Previous RF snapshot | New selected-Fire-Trap snapshot |
|---|---:|---:|
| Level | 26 | 26 |
| Life | 773 | 833 |
| `LifeRegenRecovery` /sec | 267.1 | 270.3 |
| `TotalBuildDegen` /sec | 181.975 | 195.475 |
| Life regeneration minus degeneration /sec | +85.125 | **+74.825** |
| `NetManaRegen` /sec | not separately noted | +10.0 |
| `TotalNetRegen` (resource aggregate) | not separately noted | +84.825 |
| Total mana | 313 | 313 |
| Unreserved mana | 129 | 129 |
| Fire/cold/lightning/chaos resistance | 75/75/75/0% | 75/75/75/0% |
| Armour | 806 | 806 |
| Attack block | 33% | 33% |

**Metric clarification:** `NetLifeRegen` is **74.825**. The higher `TotalNetRegen` of **84.825** includes +10 mana regeneration and must not be labelled as net *life* regeneration.

## Read-only review / priorities

1. **Keep the existing RF 4-link** for clearing; leveling Fire Trap and comparing its supports are priorities for additional boss damage.
2. At character level 31, evaluate adding Burning Damage Support on a 4-link Fire Trap, only after comparing the calculated burning-ground DPS and practical mana cost. Preserve the RF 4-link if equipment is limited.
3. The same observed `Grand Mana Flask of Damping` removes all burning; activating it may turn RF off. Keep it only if that is an intentional emergency control.
4. The boots observed in the export do not provide movement speed; find movement-speed boots while retaining life and resistance.
5. Fire Trap explicitly allows spell-damage modifiers to affect its burning-ground damage over time. Spell damage on the sceptre does not scale **Righteous Fire** damage over time, but **can scale Fire Trap** burning ground. Verify in PoB when comparing weapons.
6. A more exact RF + Fire Trap combined-boss damage figure requires a consistent build, identical enemy configuration, and explicit handling of the two simultaneous effects.

No source-code changes, tests, or actual PoB engine execution occurred as part of this snapshot.
