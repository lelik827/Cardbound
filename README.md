# Cardbound — Shattered Wilds

A standalone browser card-battle exploration RPG. Open `index.html` to play the integrated adventure or `arena.html` to use the combat-only Battle Lab. No build step or remote assets are required.

## Integrated open world

The adventure now uses the same physical-card, mastery, deck, Soulbound, player-level, and ability systems as the Battle Lab.

Exploration is organized as an original connected eleven-room labyrinth:

- Move with WASD, arrow keys, or the on-screen directional pad.
- Encounters are visible in the world; collide with an enemy to battle.
- Rooms connect in multiple directions and support backtracking.
- The Ember Sigil opens flame seals.
- Briarstep Boots cross living-thorn routes.
- The Moon Lens reveals concealed passages.
- A persistent lower-right minimap records rooms only after they are discovered, highlights the current area, and shows explored-world progress. The full Map screen remains available for room names and relic details.
- Normal enemies respawn after three room transitions; bosses remain defeated.
- Meadowrest restores health.
- The Sunken Forge contains a discoverable upgrade material.

This structure takes inspiration from the non-linear exploration principles of early ability-gated adventure games while using original Cardbound locations, layouts, visuals, enemies, characters, and mechanics.


## Visual direction

The integrated world uses an original colorful fantasy-steampunk style:

- Brass and copper pipes, riveted machinery, animated gears, and teal steam lighting.
- Distinct saturated palettes for forests, ember chambers, flooded crypts, moon vaults, forges, and the Warden depths.
- A goggle-and-mechanical-backpack treatment for the player sprite.
- Ten detailed pixel-art cyber-monsters displayed in both exploration and combat:
  - Plasma-jawed Ember Jackal
  - Crystal-tipped Circuit Thornling
  - Armored bio-mech Briar Sentinel
  - Drill-snouted Tunnel Borehound
  - Crescent-armored Lunar Enforcer
  - Holographic Phase Shade
  - Ringed Data Wisp
  - Furnace-bodied Reactor Mauler
  - Crowned surveillance Observer
  - Vine-cabled Thorn Warden
- All artwork is original, dependency-free, and stored directly in the game file.

## Unified combat and progression

- Build a 4–10 card active deck from the owned card pool.
- Every physical card starts at Level 0 and tracks its own uses.
- Fifty uses plus one open-world upgrade material unlock each of three card levels.
- Purple Soulbound cards cannot be destroyed or lost.
- Bronze Impermanent cards may be destroyed and can be lost on defeat.
- Normal victories award 25 player XP; bosses award 50; defeats award 10.
- Player progression now spans Levels 1–30, with one talent point earned at every level from 2 onward.
- The three-branch Neural Talent Matrix offers ranked, incremental card-battle upgrades: Surge improves offense and Power Boost, Disruption improves Weaken, draw, and energy, and Resolve improves Retain, Block, health, and recovery.
- Deeper talent rows require points invested in that branch, with capstone upgrades available after ten branch points.
- Talent choices can be freely recompiled outside active encounters, making it practical to test different builds.
- Bosses have a 10% chance to drop an exclusive Soulbound card.
- Normal encounters have a 10% material chance; bosses guarantee one material.

## Saves and migration

The integrated adventure saves in browser localStorage under `cardbound-integrated-v1`. Upgrade materials remain shared under `cardbound-upgrade-materials-v1`.

When beginning the integrated adventure for the first time, a valid `cardbound-battle-lab-v3` save is imported automatically, including:

- Card pool and active deck
- Card levels and mastery uses
- Player level and XP
- Player talents (or an empty tree when importing an older Battle Lab save)
- Soulbound ownership

The older adventure save is used to prefill the adventurer name when available. Saves remain specific to the browser and site origin; there is no cloud synchronization.

## Verification

Automated logic checks cover:

- All eleven rooms and their connections
- Ember Sigil, Briarstep Boots, and Moon Lens route gates
- Normal-enemy three-room respawning
- Integrated physical-card mastery
- Player XP, the Level 30 cap, talent points, branch gates, prerequisites, and derived combat bonuses
- Boss material guarantees and the 10% Soulbound boundary
- Impermanent defeat loss and Soulbound protection
- Battle Lab save detection for migration
- JavaScript syntax and the responsive 800×500 logical world scaling

A full installed-Chromium visual pass was unavailable in the build workspace, so desktop and mobile visual behavior should continue to be checked on the hosted version after deployment.

## Hosting

GitHub Pages deploys the repository root from `main`. The live build is available at:

https://achubu.github.io/Cardbound/
