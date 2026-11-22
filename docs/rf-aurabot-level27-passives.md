# RF Scion — verified level-27 passive tree and low-refund routing baseline

**Source:** User-uploaded `RF-Scion-Level27.xml.xml` inspected 2026-11-23. The source XML stays out of GitHub because it includes account/character hashes and inventory identifiers. The game-node definitions below are cross-checked against `src/TreeData/3_30/tree.lua` in this fork.

## Scope and verification status

- **Scion level 27**, no allocated ascendancy; passive tree `3_30`.
- **28 passive node entries, including class start node 58833**, corresponding to 27 allocated passive points.
- **One Fire Mastery allocation**, *not two*. The `masteryEffects="{48267,55308}"` pair identifies passive node `48267` and its effect `55308`: **Regenerate 1 Life per second for each 1% Uncapped Fire Resistance**.
- Righteous Fire selected as main skill; saved PoB **735.99 damage-over-time DPS**, max life **848**, life regeneration **272.10/s**, build degeneration **198.85/s**, net life regen **+73.25/s**, unreserved mana **133/319**, elemental resistances **75/75/75**.
- These numbers are from **saved PoB PlayerStat fields**, not a fresh PoB simulation.

## Exact allocated passive nodes

| Node ID | PoB 3.30 name | Classification for review |
|---|---|---|
| 58833 | Seven (Scion start) | start |
| 48828 | Physical Damage and Strength | starting connector |
| 33508 | Fire Resistance | resistance path |
| 36881 | Cold Resistance | resistance path |
| 35503 | Lightning Resistance | resistance path |
| 19144 | Sentinel | defence/resistance |
| 28330 | Strength | travel |
| 46578 | Strength | travel |
| 13714 | Life | life |
| 55485 | Constitution | major life |
| 65034 | Life | life |
| 46910 | Strength | travel |
| 33740 | Strength | travel |
| 15405 | Strength | travel |
| 50862 | Strength | travel |
| 2913 | Dexterity | travel |
| 44908 | Strength | travel |
| 26866 | Sanctity | defence/regeneration |
| 3167 | Life Regeneration | regeneration |
| 7335 | Armour and Life Regeneration | regeneration |
| 21413 | Combat Stamina | defence/life/regeneration |
| 16775 | Strength | travel |
| 63976 | Shaper | mana/life regeneration |
| 50422 | Strength | travel |
| 10221 | Strength | travel |
| 54396 | Burning Damage Multiplier | RF-specific benefit |
| 2550 | Arsonist | fire DoT + life regeneration |
| 48267 | Fire Mastery | uncapped fire resistance based life regeneration (effect 55308) |

**Do not refund the fire or regeneration cluster prematurely:** it contributes to the positive RF sustain margin.

## Provisional graph shortest routes to notable destinations

Computed by breadth-first search of the 3.30 passive-tree node graph, starting from any **currently allocated** node and allowing ordinary non-ascendancy nodes. These are **individual shortest paths**; the smallest *combined* route could share nodes, and the exact level-75 target PoB tree has not yet been supplied. **Not verified as the best aurabot swap path.**

| Destination | Target node ID | Nearest existing node | Minimum additional graph nodes | Example path of NEW node IDs |
|---|---:|---|---:|---|
| Sovereignty | 32932 | Strength 50422 | **10** | 50570, 29353, 44202, 23027, 60472, 26270, 64210, 5935, 9392, 32932 |
| Champion of the Cause | 33718 | Strength 46578 | **9** | 30733, 49178, 43374, 22703, 14056, 34400, 34513, 9995, 33718 |
| Empowered Bond | 28034 | Shaper 63976 | **12** | 33479, 10490, 47251, 7388, 60398, 46340, 42760, 36678, 57404, 3089, 60145, 28034 |

These counts are for reachability only; they do **not** include a target mastery allocation, any refund costs, mutually shared optimal path calculations, or a verified sequence to level 75. Graph proximity is not a substitute for comparing against the intended target tree and life/regen requirements.

## Low-refund guidance for the next milestone

1. Keep existing Constitution and life/regen investments while RF levels and sustains. **Do not allocate or refund solely from the graph estimates.**
2. Prioritize common long-term life/travel/reservation routes only when they match Allie's **3.30 Level 75 - Aurabot Swap** loadout.
3. The Arsonist/Burning Damage Multiplier/Fire Mastery branch is the most obvious fire-specific candidate for later respec, but it is both damage and regeneration now. Mark **candidate**, not confirmed refund.
4. The three elemental-resistance path nodes and Sentinel may or may not overlap the target; exact respec cost remains unknown.
5. Inspect any allocated masteries when switching — the current Fire Mastery is not automatically useful in the final aura/link configuration.
6. No PoB source code or in-game character was modified at this checkpoint.

## Needed for exact refund count and allocation order

Obtain **Allie's 3.30 PoB build** with **Level 75 - Aurabot Swap** selected in the PoB loadout selector, then save/export the target as XML or code. Compare exact node sets and check connectivity to produce:
- kept nodes; refundable nodes; required new nodes;
- mastery and ascendancy changes;
- level-based connected progression that retains RF sustain before swap;
- count of refunds and how many can be covered by campaign rewards.

Reference guide: https://mobalytics.gg/poe/builds/allie-luminary-guide
