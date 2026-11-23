# Scion RF + Fireball of Radiation: custom Reliquarian map and endgame plan (3.30)

**Status:** New optional progression branch, compared with the existing verified **Luminary Aurabot** plan. **This is a proposed custom build, not an official Goratha export or engine-validated DPS sheet.**

## Goal and basis

Keep the player's real RF + Fire Trap leveling Scion working while developing a **self-cast Fireball of Radiation** endgame character able to map independently. Starts from their actual native level-27 PoB XML and 4 user-reported Nomadic Teachings allocations. User gear/account hashes are **NOT** copied into this public document.

Recent game references: [PoEDB Fireball of Radiation](https://poedb.tw/us/Fireball_of_Radiation), [PoEDB Reliquarian](https://poedb.tw/us/Reliquarian), [Goratha's 3.30 day-2 field report](https://pobarchives.com/build/6Qjaz7gK).

**Important:** Fireball of Radiation is a short direct **fire DoT debuff** (base duration 1 second). The skill **does not hit or crit** and modifiers to Spell Damage do apply to its Damage over Time. Its projectile count improves coverage; don't multiply DoT by projectiles without checking stacking. RF may coexist and grant Spell Damage.

## Passive plan, verified connected to the 3.30 tree

User's saved level-27 tree has **27 allocated ordinary passives** plus Scion start. The reported completed route adds exactly **4 ordinary nodes**: `6446`, `27166`, `48929`, `25989` (Nomadic Teachings).

All current and reported nodes are **retained** in the custom map/endgame example trees. Thus there are **zero mandatory refunds from existing allocations** to follow *this* custom route, compared with **8** existing-node refunds to match the *separate* Allie Aurabot level-75 tree. Retaining every RF travel/regen passive is **not proven to be optimal for min-maxed DPS at level 90**; future respecs may be sensible.

| Milestone | Ordinary passives | Highlights |
|---|---:|---|
| Saved level 27 | 27 | Verified original |
| Reported current | 31 | Nomadic Teachings completed |
| ~50 | 50 | Barbarism, Hearty, Recovery Mastery, Discipline and Training, Potency of Will, Exceptional Performance |
| ~70 | 83 | Tireless, Holy Dominion, Light of Divinity, Amplify, Sanctuary, Quick Recovery, Fire Walker, Arcanist's Dominion, Holy Fire |
| 75 | 97 | Sovereignty, Purity of Flesh, Acrimony, Cruel Preparation |
| 90 | 118 | Explosive Impact, Prismatic Skin, Juggernaut, Heart and Soul, Profane Chemistry |

The **level-90 118-point ordinary tree** consumes *all* 89 level-up points at level 90, **24 campaign rewards**, and **5 bonus ordinary passives** from the Reliquarian 8-point ascendancy path. If missing rewards/Labs, defer lower-value nodes; the table is a projected stage, not a guarantee at any level.

### Exactly what to allocate next

1. `55649` Strength
2. `44429` Life and Elemental Resistances
3. `53118` **Barbarism**
4. `30380` Life and Elemental Resistances
5. `59928` Strength
6. `2219` Life Regeneration
7. `48822` Life Regeneration
8. `30302` **Hearty**
9. `53517` **Recovery Mastery**, select effect **45653 = Regenerate 50 Life/sec**
10. `61471` Life
11. `41472` **Discipline and Training**
12. `33479` Intelligence toward **Potency of Will** via `7614`, `13191`, `1006`.

Keep the existing **Fire Mastery** node `48267` and its current life-regeneration effect `55308`.

## Reliquarian ascendancy (3.30)

- **Normal Lab:** `35936`, `22441` (bonus ordinary passive nodes).
- **Cruel Lab:** `36489` **Armour Display**, choice `56940` **The Brass Dome** (+5% maximum all elemental resistances; crit damage protection; Strength stops granting life).
- **Merciless Lab:** `16633`, `15544` (bonus passives), `2460` **Caster Weapon Display**, choice `59067` **Shade of Solaris**. Needs **a critical strike from a separate hitting skill**, e.g. Storm Brand, to maintain 200% **increased** Spell Damage for 8 seconds.
- **Eternal Lab:** `18147` (bonus passive), `35989` **Jewellery Display**, choice `54569` **The Arkhon's Tools**. Active only with **Summon Skitterbots**.

Display choices are free mutual-exclusive option nodes in the tree export, not additional ascendancy points.

## Suggested skills

**Level 27–40:** Retain user's RF 4-link, Fire Trap 3-link, Purity of Fire, Vitality, Shield Charge/Faster Attacks/Lifetap, Frostblink. No gear purchase necessary.

**Level 40–50 test:** Fireball of Radiation – Burning Damage – Efficacy – Greater Multiple Projectiles (4L). Do not retire Fire Trap until testing shows good clear/boss performance.

**Early maps 5L:** Fireball of Radiation – Burning Damage – Efficacy – Greater Multiple Projectiles – Lifetap.

**Level 75 map 6L:** Fireball of Radiation – Burning Damage – Efficacy – Swift Affliction – Greater Multiple Projectiles – Lifetap. RF 4L: RF – Burning Damage – Elemental Focus – Efficacy. Storm Brand 4L: Storm Brand – Increased Critical Strikes – Combustion – Lifetap. Need some **added fire damage to spells on an appropriate item** for Combustion to apply its ignite/resistance reduction with Brand. Movement: Shield Charge – Faster Attacks – Lifetap, plus Frostblink. Buffs: **Purity of Fire**, optional Determination and level-appropriate Vitality as mana permits.

**Level 90 boss:** Swap **GMP (green)** to **Elemental Focus (blue)** for damage if PoB confirms the gain. This requires **socket recolour, white socket, or separate body armour**; it is not a same-colour swap. With the Uber-Lab Arkhon choice, use **Skitterbots** (optionally Unbound Ailments), Purity of Fire and lower-level Vitality; trade Skitterbots for Determination in defensive variants if needed, accepting the Arkhon power will be unused.

## Gear and mechanical gates

1. Budget 5/6L gear and capped resists, life, enough attributes, and comfortable RF **net** regen before upgrades.
2. Sceptre priority: **+1 Fire Spell Gems**, fire DoT multiplier, cast speed, and fire/elemental damage. Existing low-level Ochre Sceptre is fine until a worthwhile upgrade appears.
3. Shield with life/resists/armour; rare body armour and other slots with life/resists. Get **added fire damage to spells** somewhere for Storm Brand Combustion.
4. Do not assume example gear used in a PoB is owned or market-available. Don't treat the example stage as a proven damage target.
5. For serious T16 and pinnacle bosses, recalculate actual DoT DPS with correct enemy config and no fabricated projectile stacking, plus full defensive hit/DoT survival, max fire res, chaos resistance and the actual aura budget.
6. Aspiring to **Shadowstitch** (instead of Brass Dome) or **Rathpith Globe** changes the defensive budget and requires separate testing; don't buy them blindly. Any build using **Kaom's Heart** must relocate Fireball out of the now socketless chest.

## Provenance and caution

- XML currently shared with the user in the chat includes user's sanitized original level-27 tree, five skill configurations and six connected tree specs (one per milestone).
- Programmatically verified valid XML, compressed-code round-trip, item-set structure and omission of account hashes/item unique IDs. No local Path of Building engine available to validate item modifier application, DPS, actual reservation or colour/gear sufficiency. This **must** be checked in the app before buying gear.
- The target was **not** imported from Maxroll. This plan is a separate original prototype informed by public gem/mechanics and Goratha's report; do not attribute its numeric stats to Goratha.
