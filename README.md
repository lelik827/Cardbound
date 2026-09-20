# Cardbound — Crystalwood Edition

A standalone browser card-battle RPG with original retro pixel artwork. Open `index.html` to run; no build step or external game assets are required.

## Preview status

The core gameplay loop was playtested in desktop Chrome on 2026-09-20 at https://lelik827.github.io/Cardbound/.

Verified through normal UI controls: all customization options, repeated card picks/removal/copy cap, Balanced starter, entering the world, directional-pad movement and tree collision, two monster victories, attack/block/mana/draw behavior, reward selection, earned-card removal and re-addition, use of Blood Pact in the second battle, and save/reload with restored name, appearance, XP, gold, and quest progress. No game-origin errors were observed in captured browser logs.

The playtest found a stale Continue saved adventure control inside character editing; the follow-up fix removes it after adventure entry. Mobile layout, keyboard hold behavior, defeat recovery, and the final boss still need browser testing. Offline logic checks also passed. This remains a preview, not an assurance that every path works.

## Hosting

In repository Settings → Pages, choose **Deploy from a branch**, **main**, and **/(root)**, then Save. Subsequent changes to the publishing branch will update the site.

## Saved progress

Progress uses browser localStorage under `cardbound-v2`. Saves are specific to the browser and origin; there is no cloud synchronization. Saves occur outside combat. Moving from a downloaded file to the hosted site does not automatically transfer an existing save.

## Required playtest before marking an update verified

- Exercise every customization category and compare male/female previews with world sprites.
- Manually pick, remove, and swap cards; check presets, copy limits, and the ten-card starting gate.
- Enter the world and walk into a monster encounter through normal controls.
- Play cards, end turns, win, choose a reward, and return to the world.
- Add an earned card to the deck and complete another battle.
- Reload and continue the saved adventure; test defeat recovery.
- Check desktop and mobile layouts and browser errors.

Keep unverified changes clearly labeled until this sequence passes in a real browser.
