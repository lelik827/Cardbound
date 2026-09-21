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
- The map records rooms only after they are discovered.
- Normal enemies respawn after three room transitions; bosses remain defeated.
- Meadowrest restores health.
- The Sunken Forge contains a discoverable upgrade material.

This structure takes inspiration from the non-linear exploration principles of early ability-gated adventure games while using original Cardbound locations, layouts, visuals, enemies, characters, and mechanics.

## Unified combat and progression

- Build a 4–10 card active deck from the owned card pool.
- Every physical card starts at Level 0 and tracks its own uses.
- Fifty uses plus one open-world upgrade material unlock each of three card levels.
- Purple Soulbound cards cannot be destroyed or lost.
- Bronze Impermanent cards may be destroyed and can be lost on defeat.
- Normal victories award 25 player XP; bosses award 50; defeats award 10.
- Level 2 unlocks a once-per-encounter Power Boost.
- Level 3 unlocks encounter-wide Weaken.
- Level 4 permanently improves either Power Boost or Weaken.
- Level 5 unlocks one retained card per turn.
- Bosses have a 10% chance to drop an exclusive Soulbound card.
- Normal encounters have a 10% material chance; bosses guarantee one material.

## Saves and migration

The integrated adventure saves in browser localStorage under `cardbound-integrated-v1`. Upgrade materials remain shared under `cardbound-upgrade-materials-v1`.

When beginning the integrated adventure for the first time, a valid `cardbound-battle-lab-v3` save is imported automatically, including:

- Card pool and active deck
- Card levels and mastery uses
- Player level and XP
- Level 4 mastery path
- Soulbound ownership

The older adventure save is used to prefill the adventurer name when available. Saves remain specific to the browser and site origin; there is no cloud synchronization.

## Verification

Automated logic checks cover:

- All eleven rooms and their connections
- Ember Sigil, Briarstep Boots, and Moon Lens route gates
- Normal-enemy three-room respawning
- Integrated physical-card mastery
- Player XP and Levels 2, 3, and 5 abilities
- Boss material guarantees and the 10% Soulbound boundary
- Impermanent defeat loss and Soulbound protection
- Battle Lab save detection for migration
- JavaScript syntax and the responsive 800×500 logical world scaling

A full installed-Chromium visual pass was unavailable in the build workspace, so desktop and mobile visual behavior should continue to be checked on the hosted version after deployment.

## Hosting

GitHub Pages deploys the repository root from `main`. The live build is available at:

https://lelik827.github.io/Cardbound/
