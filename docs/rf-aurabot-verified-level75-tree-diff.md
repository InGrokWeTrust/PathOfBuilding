# VERIFIED RF level-27 → Luminary level-75 passive tree comparison (3.30)

Date: 2026-11-23. Source files privately inspected:
- **Current:** user-supplied `RF-Scion-Level27.xml.xml`, one `Tree/Spec` of 28 node IDs (including Scion start).
- **Target:** user-supplied `Luminary Aurabot_75.xml`, **`Tree activeSpec="13"`**, whose 13th `Spec` is explicitly titled `Level 75 - Aurabot Swap {1}` (not the later Level 90/endgame variants).

**Privacy:** No raw XML, PoB build-sharing codes, account hashes, character names, item unique IDs or imported account metadata were committed. Skill tree node IDs, generic class and anonymous calculated results only.

## Exact set comparison

| Item | Count |
|---|---:|
| Current node entries (including Scion start) | 28 |
| Target node entries (including Scion + Luminary starts) | 108 |
| Shared node IDs | **20** |
| Current entries not in target | **8** |
| Target entries missing from current | **88** |
| Target ascendancy entries (including Luminary start) | 9 |
| Target ordinary passive entries (including Scion start) | 99 |
| Target ordinary passive points spent (excluding start) | **98** |
| Target ascendancy points spent (excluding Luminary start) | **8** |
| Ordinary passive IDs to add | **79** |
| Target mastery selections | **11** |

**Exactly 8 current passive points must be refunded if the user matches this exact target tree and allocates no other non-target nodes.** Eight is a *set-difference count for existing allocations*, not a promise about additional future temporary points or extra swapping transactions. All eight are ordinary passive entries (one is a Fire Mastery).

The level-75 target allocates 98 ordinary passive points. At character level 75 there are 74 level-up passive points; the target therefore requires **24 additional campaign/bandit passive rewards**. Eight ascendancy points implies all **four Labyrinth completions**, including Uber Lab, for the exact exported tree. Without all of these, treat some nodes as deferrable rather than claiming the build can match the export at 75.

## Allocated nodes already on the target (KEEP)

20 IDs: `2913,10221,13714,15405,19144,26866,28330,33508,33740,35503,36881,44908,46578,46910,48828,50422,50862,55485,58833,65034`.

Significant shared notables: **Constitution**, **Sanctity**, **Sentinel**. Keep the associated life, elemental-resistance and travel path unless the intended target itself changes.

## Existing nodes NOT on the target (8 refunds, at conversion)

| Node ID | Name |
|---:|---|
| 2550 | Arsonist |
| 54396 | Burning Damage Multiplier |
| 48267 | Fire Mastery (selected effect 55308, uncapped Fire Resistance → Life Regeneration) |
| 3167 | Life Regeneration |
| 7335 | Armour and Life Regeneration |
| 21413 | Combat Stamina |
| 16775 | Strength (connector to Shaper) |
| 63976 | Shaper |

These nodes currently contribute to sustaining RF or connect its temporary branches. **DO NOT refund them while leveling RF.** At the conversion, verify sufficient replacement defenses and remove the branches in connectivity-safe order.

## Sustain-first next 12 points, all in EXACT target

Source paths were checked against the 3.30 tree graph, restricted to nodes already allocated or present in target `Spec 13`. This is an intentionally *sustain-first* proposed order, not an independently re-run PoB DPS/sustain simulation.

**First four — +2% max all elemental resistances: Nomadic Teachings**
1. `6446` Strength
2. `27166` Fire Resistance
3. `48929` Maximum Fire Resistance
4. `25989` **Nomadic Teachings** (+2% to all max Elemental Resistances)

**Next three — life +1% max Fire Resistance: Barbarism**
5. `55649` Strength (branches from `6446`)
6. `44429` Life and Elemental Resistances
7. `53118` **Barbarism**

**Next five — strong regeneration: Hearty**
8. `30380` Life and Elemental Resistances
9. `59928` Strength
10. `2219` Life Regeneration
11. `48822` Life Regeneration
12. `30302` **Hearty** (1.8% life regeneration, 15% increased life regeneration rate)

These paths preserve all current RF investments, remain connected to the existing tree, and add no non-target nodes. At one point per character level, they roughly span level 28–39; quest point awards can make the progression earlier.

**Useful independent two-point detour already on target:** from existing `26866` Sanctity → `61471` Life → `41472` **Discipline and Training**. Use as warranted by life/defense and available points.

## Mid-level and end-level route landmarks (not exact all-node schedule)

- After Nomadic Teachings, Barbarism and Hearty, establish the Templar-side defensive path from Sanctity through Discipline and Training. The target contains `44799` Elemental Damage → `40927` Area of Effect → `61308` **Amplify**, useful for RF clearing on the way.
- Continue from that target route through the Life/Energy Shield and Intelligence connectors to **Sovereignty** (`32932`), taking reservation notables when an aura benefit exists.
- Continue the lower/left target travel chain from the Barbarism area toward **Champion of the Cause** (`33718`).
- Build **Empowered Bond** (`28034`) and the Link Mastery at or immediately before the actual aurabot swap rather than sacrificing useful RF leveling points too early.
- **Inexorable** (`54629`) and **Golden Glory** (`31517`, Uber-Lab ascendancy) are possible deferred upgrades when the full target budget is not yet available.

For reference, the *target-restricted graph paths* directly from currently allocated nodes require at least 16 new nodes to Sovereignty, 14 to Champion of the Cause, and 18 to Empowered Bond considered separately. Those paths can share target nodes; they are **not** a sum or an allocation-order mandate. Earlier pre-target provisional route counts of 10/9/12 used the unrestricted tree and **could require nodes not in the target**, so they should not be used as no-refund instructions.

## Validation gates at conversion

- Character has a properly equipped suitable mercenary and a working Link setup.
- Required aura/link support gear is equipped, plus sufficient reservation/defenses when the actual PoB configuration is re-calculated.
- Confirm passive quest rewards earned, ascendancy points/Labyrinth status, and all intended masteries.
- Finish permanent paths first; never refund a currently necessary connector.
- RF-specific nodes remain until RF is retired. Then use the 8-refund list and compare the new tree against the 13th `Spec`.
- If quest points or Uber Lab are incomplete, defer optional target passives rather than committing more temporary allocations.

Source for mapped node stats and graph edges: `src/TreeData/3_30/tree.lua` in this same fork. **No changes to Path of Building's calculation engine.**
