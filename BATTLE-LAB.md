# Cardbound Battle Lab

Play `arena.html` to work exclusively on card battles. `index.html` retains the open-world adventure.

## Card mastery and upgrades

- Every owned card starts at Level 0 with 0/50 uses.
- Playing a specific physical card increments that card's use counter once.
- Each upgrade requires 50 uses; progress stops at 50 until the upgrade is completed.
- A ready card also consumes one upgrade material to advance.
- Completing an upgrade resets that card to 0/50 uses for the next level.
- Cards have three upgrades: Level 1, Level 2, and Level 3.
- Newly rewarded normal and Soulbound cards always start at Level 0.

## Open-world upgrade materials

- Upgrade materials are shared through `cardbound-upgrade-materials-v1` localStorage.
- Battle Lab victories and card destruction do not create upgrade materials.
- Regular open-world monsters have a 10% chance to drop one material.
- The open-world Thorn Warden guarantees one material.
- The adventure quest panel displays the shared material balance.

## Deck Workshop

- The card pool contains every card owned during the run.
- Build an active deck of 4–10 cards from the pool.
- Add and remove owned cards freely between battles.
- Impermanent cards may be destroyed, but destruction does not provide world materials.
- Soulbound cards may be trained and upgraded, but cannot be destroyed or lost.

## Soulbound drops and card loss

- Every third Battle Lab encounter is a boss.
- A defeated Battle Lab boss has a strict 10% chance to offer one Soulbound card.
- Soulbound cards never appear in normal rewards.
- Defeat can permanently remove one random Impermanent card from the active deck.
- Defeat does not reduce the active deck below its four-card playable minimum.

Progress uses `cardbound-battle-lab-v3` localStorage and remains separate from adventure saves, while the upgrade-material balance is shared between both modes.

## Validation

Automated checks cover Level 0 initialization, the 49/50-use boundary, the 50th-use ready state, blocking upgrades without a world material, material consumption, progress reset after upgrading, Level 0 rewards, and destruction without material creation.

The v3 mastery system starts a fresh Battle Lab run so every card begins at Level 0; the shared open-world material balance is preserved.