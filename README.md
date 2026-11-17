<img src="app-512.png" alt="Katherine" width="96" align="right">

# Katherine

**A draft assistant and coach for League of Legends ranked play on Windows.**

Katherine runs beside the League client. In champion select it follows the draft and, on each of your turns, shows
several pick and ban options with the reasons behind them. After the game it files the draft and its result so you can
review it. It works for a full five-stack in Ranked 5s, for a partial lineup in Flex, and for a solo player or a duo in
Solo/Duo.

> [!IMPORTANT]
> Katherine **only reads** champion select. It never hovers, picks, bans, locks or accepts anything in the League
> client, it does not read the running game, and it shows nothing during a game that was not known before the game
> started. The decisions are always yours.

**[Download the installer](https://github.com/muff1ntogo/Katherine-releases/releases/latest/download/Katherine-Setup.exe)**
(Windows 10 or 11, free) · [What's new](../../releases) · [Privacy](https://muff1ntogo.github.io/Katherine-releases/privacy.html) ·
[Terms](https://muff1ntogo.github.io/Katherine-releases/terms.html)

---

## Contents

- [Features](#features)
- [System requirements](#system-requirements)
- [Installation](#installation)
- [Getting started](#getting-started)
- [Updates](#updates)
- [Your data and privacy](#your-data-and-privacy)
- [Troubleshooting](#troubleshooting)
- [Legal](#legal)

---

## Features

### Live: champion select

- **Pick and ban options on every turn,** each with a short reason: the lane matchup, how it fits the team's
  composition, and how comfortable the player is on it. Close calls are marked as close; contested picks show how likely
  the enemy is to take them next.
- **Two clear figures for the draft:** *Draft edge* (what the champions alone give your side) and *With comfort* (the
  same, including how well your players know their champions).
- **Both draft formats, detected automatically:** tournament draft for Ranked 5s, and standard draft (simultaneous bans)
  for Flex and Solo/Duo.
- **The enemy side:** their most likely picks for each open role, the roles their flexible picks are probably going to,
  and the biggest threats left in the pool.
- **Composition panels** for both teams, with each comp's fighting style and when it is strongest.
- **Next two picks:** pairs that work well together for your remaining slots.
- **Enemy scouting (Ranked 5s):** when the client shows the enemy players' Riot IDs, Katherine reads their recent ranked
  games and mastery, and splits ban options into "from their pools" and "the rest". It flags one-tricks and players whose
  role is uncertain.
- **Solo/Duo mode:** with one or two known players, suggestions concentrate on your own lane (and your duo's), and the
  rest of the team is treated as unknown.
- **Pinned plan:** a plan built in Prep appears as a bar at the bottom of Live, showing which planned champions are still
  available and how the draft compares with the plan.
- **Fast and resilient:** turns update in well under a second, and if one panel fails the rest of the screen keeps
  working.

### Strategy and the in-game overlay

- Once the draft is locked, the **Strategy** tab shows notes that are known before the game starts: a lane plan, the
  levels and items where each side is strongest, kill pressure, the team's power timeline and a game plan.
- An optional **in-game overlay** keeps the blocks you pin in a small window over the game. It never takes keyboard
  focus, can be locked so clicks pass through, and remembers its position, size and opacity. It closes at the end of the
  game. It is an ordinary window: nothing is injected into the game. (Borderless or Windowed mode only.)

### Prep

- **Plan:** priority bans for each side, the best picks this patch from your pools, safe blind first picks and flex
  picks, with the plan's pick order, risks and backups. Pin a plan for the next game.
- **Synergy:** how your pools' champions work together, explored visually.
- **Matchup tree:** answers to each kind of lane opponent, with the gaps in each player's pool.
- **Lane ban tables:** which bans protect each lane most.

### Review

- **History:** every logged game with its draft, the figure predicted at lock-in, a draft report, and a split of the game
  into the draft, the early game and the conversion, so you can see where it was won or lost. Filters, an overview band
  with charts over the last 10 to 100 games, and markers for whether a pinned plan was followed and how scouting went.
- **Import missed games:** ranked games of the last 60 days in which three or more of your players were together, even
  if Katherine was not running.
- **Team trends:** recent form, draft against execution over the last 10, 20 or all games, per-player figures, and your
  record by composition style.

### Roster and player profiles

- **Lineup and bench:** five active players and a bench that keeps a swapped-out player's pool. Swap, bench or move
  players between roles with a 10-second Undo.
- **Add player:** look up a Riot ID, let Katherine read their ranked games and propose a champion pool, review it, and add
  them to the lineup or the bench.
- **Profiles:** each player's games, win rate, KDA, CS and vision per minute, lane execution, roles, mastery and an
  editable pool per role, with tier suggestions from recent games and a pool health check.
- **Personal model:** with enough games, a player's profile learns where they do better or worse than expected and
  suggests champions worth trying.

---

## System requirements

- **Windows 10 or 11**, 64-bit (the League client runs only there).
- **Microsoft Edge WebView2**, which ships with Windows 10 and 11. Without it Katherine opens in your default browser
  instead.
- An internet connection for champion statistics, match history and updates. Once the statistics are downloaded,
  champion select keeps working offline.
- No Riot API key, administrator rights, Python or Node.js are needed. Katherine is currently available for **EUW**.

---

## Installation

1. **[Download the installer](https://github.com/muff1ntogo/Katherine-releases/releases/latest/download/Katherine-Setup.exe)**
   (`Katherine-Setup.exe`, always the latest stable release).
2. Run it. It installs for your user only into `%LOCALAPPDATA%\Programs\Katherine` and creates Start menu shortcuts (and
   a Desktop shortcut if you tick it). It asks no other questions.
3. Open Katherine. On first start it fetches champion data and the project's statistics by itself, with a progress
   banner. Champion select works straight away and improves as the data arrives.

Windows SmartScreen may warn about an unrecognised app, because the installer is not yet code-signed. The update
checksums and signatures are checked by Katherine itself.

**Uninstalling:** use *Uninstall Katherine* in the Start menu or Windows Settings. Your data folder is kept so a
reinstall picks up where you left off; to remove your data as well, use **Settings > Data > Delete my data** first, then
delete `%LOCALAPPDATA%\Katherine`.

---

## Getting started

1. **Open Katherine** from the Desktop or Start menu. It opens in its own window and finds the League client by itself.
2. **Welcome page:** tell Katherine who you are (your Riot ID), and optionally add a duo partner or a team. Katherine
   reads each player's ranked games and proposes a champion pool; adjust it and set each player's stats bracket on their
   profile.
3. **Plan ahead (optional):** build a plan in **Prep** and pin it for the next game.
4. **Queue as usual.** When champion select starts, **Live** follows the draft and shows its options on your turns.
5. **After the game,** the draft and result appear in **Review**. **Import missed games** fills in anything Katherine
   was not running for.

Want to look around without a game? Start Katherine with `--demo` for simulated drafts.

---

## Updates

Katherine checks for a new release at start-up and every 6 hours. When one is available an **Update** banner appears with
what's new; one click downloads the installer, verifies it, installs it and restarts the app. Updates are never offered
from champion select to the end of the game, and they wait for a running job to finish. Your data folder is never
touched by an update. Running the latest installer by hand does the same. Every release's notes are on the
[releases page](../../releases).

---

## Your data and privacy

- **Your games and players stay on your computer** in `%LOCALAPPDATA%\Katherine` (**Settings > Data** shows the path):
  the database, roster, pools, logged drafts and settings.
- **Riot data goes through the Katherine service,** so no API key is stored in the app. If you sign in (with Discord),
  or create or join a team or duo, the account identifier, your Riot ID and what the group shares are kept on the
  service. You can use Katherine without an account.
- **Champion statistics carry no player identities:** they are aggregate counts built from public ranked matches.
- **Nobody hidden is looked up.** In Solo/Duo and Flex the game hides other players' names, and Katherine respects that.
- **The local server only answers the app.** It listens on your own machine and checks every request against a token
  issued at launch.
- **No advertising, no analytics and no telemetry:** Katherine does not report usage or crashes anywhere.
- **Delete my data** (**Settings > Data**) removes every player, pool, fetched game, logged draft and scouted player from
  this machine and, if you are signed in, can delete your account too.

Full details: [Privacy Policy](https://muff1ntogo.github.io/Katherine-releases/privacy.html) and
[Terms of Service](https://muff1ntogo.github.io/Katherine-releases/terms.html).

---

## Troubleshooting

| Problem | What to do |
| --- | --- |
| Katherine opens in the browser instead of its own window | Install or repair Microsoft Edge WebView2, then restart Katherine. |
| Live says the client isn't connected | Start the League client. Katherine finds it by itself; there is nothing to configure. |
| No suggestions or statistics after a new patch | Statistics catch up when the project publishes new ones; until then Katherine uses its starting statistics. |
| Match history or scouting fails | Riot's rate limits apply; Katherine waits and retries by itself. Try again in a minute. |
| The overlay doesn't appear | It shows only in Borderless or Windowed mode, not exclusive Fullscreen, and never with `--browser`. Check it is switched on in Settings. |
| The Update banner is missing | Updates are held during champion select and an active game. |

Anything else: open an issue on this repository. Please don't post personal details there.

---

## Legal

Copyright © 2026. All rights reserved. The source code is private. The installer is provided under its own end-user
terms (see the [Terms of Service](https://muff1ntogo.github.io/Katherine-releases/terms.html)).

Katherine isn't endorsed by Riot Games and doesn't reflect the views or opinions of Riot Games or anyone officially
involved in producing or managing Riot Games properties. Riot Games and all associated properties are trademarks or
registered trademarks of Riot Games, Inc.

The licences of the open-source software included in the app are listed under **Settings > About**.
