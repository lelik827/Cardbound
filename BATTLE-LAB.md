# Cardbound Battle Lab

Play `arena.html` to work exclusively on card battles. `index.html` retains the original adventure.

## Deck Workshop

- The card pool contains every card owned during the run.
- Build an active deck of 4–10 cards from the pool.
- Add and remove owned cards freely between battles.
- Every card has a Base form and three upgrade levels: I, II, and III.
- Upgrades cost 1, 2, then 3 upgrade materials.
- Each victory awards 1 upgrade material.
- Destroying an Impermanent card returns 1 material plus its upgrade level.
- Soulbound cards may be upgraded, but cannot be destroyed or lost.

## Soulbound drops and card loss

- Every third encounter is a boss.
- A defeated boss has a strict 10% chance to offer one Soulbound card.
- Soulbound cards are exclusive to that boss-drop roll and never appear in normal rewards.
- Defeat can permanently remove one random Impermanent card from the active deck.
- Soulbound cards are always protected from defeat loss.
- Defeat does not reduce the active deck below its four-card playable minimum.

## Combat baseline

- Six-card starter pool and active deck: three Ember Blades, two Crystal Wards, one Starlit Focus.
- Three energy and four cards per turn.
- 30 player health. First enemy: 42 health and 8 base attack.
- Every third turn is a telegraphed heavy attack (+4).
- Enemy health and attack scale with battle number; bosses receive additional health and attack.
- Wins recover 4 health and offer one of three normal cards, or the player may skip.

Progress uses `cardbound-battle-lab-v2` localStorage and remains separate from adventure saves.

## Validation

Automated logic checks cover starter pool/deck creation, all three upgrade levels and their costs, material refunds, Impermanent destruction, defeat loss, Soulbound protection, the exact 10% drop boundary, reward ownership, and save writes.