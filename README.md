# Cardbound — Crystalwood Edition

A standalone browser card-battle RPG with original retro pixel artwork. Open `index.html` to run; no build step or external game assets are required.

## Preview status

This is an **unverified preview**. Offline DOM/logic checks passed for customization, deck selection, card limits, combat calculations, rewards, deck improvements, save serialization, and defeat recovery. Sprite renders were inspected. A full real-browser playthrough remains pending; offline checks do not establish that the complete interface works.

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
