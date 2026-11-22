# RF leveling to Luminary Aurabot — PoB fork workflow

Status: **planning checkpoint**. This document is not a character import, a calculated build, or a modification to PoB gameplay logic.

## Purpose

Use the existing Path of Building Community Fork engine to help plan a Scion's Righteous Fire (RF) + Fire Trap leveling progression and an eventual level-75 Luminary Aurabot transition. Make decisions from actual PoB snapshots, not assumed character stats.

## Confirmed capabilities in this fork

- `src/Classes/ImportTab.lua`: character and build import/export interface, including Path of Exile account authorization.
- `src/Modules/CalcOffence.lua`: offensive calculations, including damage over time.
- `src/Modules/CalcDefence.lua`: defensive calculations, including mitigation and regeneration-related logic.
- `src/Modules/BuildDisplayStats.lua`: calculated statistics shown in the UI.
- `src/Classes/PartyTab.lua`: party-support modelling, including auras, curses, warcries and link skills.
- `src/Classes/TreeTab.lua`, `src/Classes/PassiveSpec.lua`: passive-tree planning.

PoB already implements the core calculations and import tools. Avoid duplicating them.

## Current user-reported baseline (requires a fresh PoB export to verify)

- Character: Scion leveling toward a Luminary Aurabot build.
- Level reported at the last detailed leveling check: 24; confirm current character level after the restart.
- RF reportedly sustainable; Fire Trap planned for tough enemies.
- Auras: Purity of Fire and Vitality.
- Last reported mana: 139 unreserved / 328 total (may no longer be current).
- Shield Charge with support gems for movement.
- Goal: transition at approximately level 75 **when the required gear, passives, gem levels, reservation and survivability are ready**. Do not assume level alone is sufficient.

## Workflow

1. Import the current character into local Path of Building or load a build export.
2. Export a build code or XML snapshot **after checking it contains no account credentials or private data**.
3. Record a baseline: character level, ascendancy, allocated passive tree, main skill links, all active auras, gear, RF damage over time, Fire Trap burning-ground damage, life and life regeneration, max fire resistance, and unreserved mana.
4. Compare controlled changes one at a time (e.g. a support gem, passive point, item or aura) against the same configuration and enemy assumptions.
5. Save milestone build snapshots (suggested levels 24/35/50/65/75, adjusted to actual progress), and document the change and observed PoB outputs.
6. Independently create a level-75 aurabot target build. Verify party effects, reservation, defenses and respec cost before switching.

## First useful feature to consider

A **read-only RF / Aurabot build-review report** which consumes a user-provided PoB snapshot or PoB calculation output and presents:

- RF damage over time and Fire Trap burning-ground damage separately, with configuration assumptions.
- Max fire resistance, life, life regeneration, self-damage and any net-regeneration estimate with stated assumptions.
- Reserved/unreserved mana, active auras, and readiness for the aurabot's proposed reservation setup.
- Passive points required for the next milestone and prospective respec cost.
- Clearly flagged unknowns, unsupported stats and missing character data.

Build on PoB's existing calculations, not hand-written approximations. Design and tests must be reviewed before implementation; do not claim an accurate RF sustain value without checking all relevant effects.

## Safety and change controls

- **Do not change upstream game calculations** until a specific missing capability or reproducible bug is demonstrated.
- All proposed changes go through `feature/rf-aurabot-tools` and a reviewed pull request.
- Avoid changes to `dev` without review, and retain upstream compatibility.
- Never commit account tokens, OAuth material, Path of Exile session cookies, or other secrets.
- This repository is **public**; user character exports should be reviewed for privacy before committing.
- No game character data has been imported, no local PoB run has been completed, and no build calculations have been validated in this checkpoint.

## Next checkpoint

Obtain a fresh PoB build export from the user's actual character, inspect its XML/build content (without secrets), and produce a baseline report. Only then decide whether the desired improvement requires new PoB source code or can be delivered as a separate report or tooling.

## Import diagnostic: first user-provided export (2026-11-23)

A supplied PoB sharing code was decoded locally but **not committed** to GitHub. XML inspection showed:

- `Build`: Scion, level 1, no ascendancy; stored calculated life 60, mana 50, no life regeneration, no DoT damage.
- `Skills`: one empty `SkillSet`, no gems.
- `Items`: no item payloads, equipment slots all unassigned.
- `Tree`: tree version `3_30`, only the Scion start node (`58833`).

**Conclusion:** The code is a blank PoB template, not an import of the in-game RF character. No RF or aurabot baseline can be calculated yet. The XML also contained an account-derived hash in import metadata; neither the raw code nor that identifier belongs in this public repository.

**Recovery:** In PoB's **Import/Export Build → Import From Your Account**, select **Authorize with Path of Exile** as needed, **Fetch Characters**, choose the correct realm/league/character, then import both **Passive Tree and Jewels** and **Items and Skills**. Confirm the build shows the actual character level, passive nodes, gear and RF/Vitality/Purity of Fire gems before selecting **Build Sharing → Generate → Copy** and providing the new export for private review.
