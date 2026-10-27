# SIDEQUEST MAXXING ✳

**No quests. No glory.** A mobile-first Halloween nightlife game for consenting adults, designed for a shared phone.

## Start playing

Open `index.html` in a modern browser. No server, sign-up, API key, dependency, or build step is needed. You can also host these files on GitHub Pages.

The site adapts to any number of players, with no hard-coded group limit. For best results, one host controls the game on their phone: add names, start, randomly pick a player, choose CALM / MODERATE / BLACK, reveal a challenge, optionally reshuffle once within that difficulty, and record complete/failed. A leaderboard updates after every result. The Hall of Fame contains automatic score-based awards and host-chosen social awards.

## Publish on GitHub Pages

1. Upload `index.html`, `styles.css`, `app.js`, and `quests.js` to the default branch, at the root.
2. In the repo's **Settings → Pages**, select **Deploy from a branch**, your default branch, and **/(root)**, then save.
3. Visit the published URL after GitHub finishes the deployment. All files use relative paths and work on project subpaths too.

If Pages is already configured, pushing a change to the default branch will trigger a redeploy.

## Game rules

- Each player has **2 CALM**, **2 MODERATE**, and **unlimited BLACK** quest draws. These allowances are **per player**, not shared by the group.
- Issuing a quest uses one slot immediately. Rerolling does not use another slot.
- Every issued quest has **one optional reroll**, strictly within the original difficulty. There is no switching difficulty mid-turn.
- CALM / MODERATE / BLACK pay **1 / 3 / 5 points** for completed quests; failed quests award **0**.
- Where the challenge is to ask or approach, a respectful attempt counts even if the other person says no. No one should be pressured, filmed without permission, or subjected to unwelcome contact.
- Quest draws favor not-yet-used items globally and per player; after pools are exhausted, they avoid repeats for the same player when possible. This is random selection, **not cryptographic randomness**.
- The host can put players temporarily on the bench without deleting their history, and deliberately manage the roster after the game starts.
- Consequences are **optional**: a silly performance or a free pass. No consumption is required.

## Storage and backups

Game state is saved automatically in the browser's `localStorage`. There is **no cross-device sync** and no transmission of names, scores, or history. Host → **Export backup** downloads a JSON file. Host → **Import backup** restores it on a device. A confirmation protects reset and replacing a game with imported data. Private/incognito browsing may erase local storage when the session closes.

The separate quest library is bundled in `quests.js` (`window.SIDEQUEST_QUESTS`) rather than loaded by `fetch()` so the site works offline by opening `index.html` directly with a `file://` URL. `quests.json` is also provided as a machine-readable companion file. All **180 original ID slots** are present: CLM-001–060, MOD-001–060, BLK-001–060. The curated quest wording comes from the supplied build brief. The app never generates new quests.

## Safety and source adaptations

The source library includes adult flirting and physical-intimacy tasks. The build preserves the general challenge tone but makes minimal safety/consent adaptations to some missions, including no coercion, no venue-bathroom sex, no pressure to obtain kisses/contact information, no required filming, no physical restraint, no unwanted intimate touching, and no alcohol/spicy-substance punishment. Every MODERATE and BLACK card shows a consent reminder. Some potentially uncomfortable challenges have their descriptions adjusted to require explicit opt-in or substitute a harmless playful challenge. The adapted source items can be found by the ID in `quests.js`/`quests.json` and compared against the supplied PDF. The design intentionally does not award points for specific sexual outcomes.

## Browser support

Modern Chrome, Safari, Firefox and Edge. Keyboard focus states, minimum-size touch controls, reduced-motion support and safe viewport spacing are included. All game functions run client-side; no analytics and no paid services.