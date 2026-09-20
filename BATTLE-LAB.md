# Cardbound Battle Lab

Play `arena.html` to work exclusively on card battles. `index.html` retains the original adventure.

## Initial balance

- Six-card starter: three Ember Blades, two Crystal Wards, one Starlit Focus.
- Three energy and four cards per turn. Unplayed cards discard; exhausted cards return next battle.
- 30 player health. First enemy: 42 health and 8 base attack.
- Every third turn is a telegraphed heavy attack (+4). Attack increases by 1 every two turns.
- Each successive enemy has 7 more health; base attack increases every two battles.
- Win to recover 4 health and choose one of three card rewards, or skip.
- Remove cards between battles, keeping at least six.
- Defeat ends the run; restarting builds a fresh six-card deck.

Each card has original inline SVG artwork, a cost gem, a title, a type, and rules text. No remote assets or build dependencies are required.

Progress uses `cardbound-battle-lab-v1` localStorage, including the current hand, enemy, and turn. This is separate from adventure saves. No cloud save sync.

## Validation

Offline checks cover damage, energy, block expiry, drawing, exhaustion, enemy escalation, defeat, rewards, and starting a stronger next battle. Difficulty is an initial tuning baseline, not a guarantee for every deck or draw. Browser playtest results are recorded separately as coverage is completed.
