# gta6-01-kanbara12-v12

[![make.fun · gta6-01](https://make.fun/badge/gta6-01.svg)](https://make.fun/bounty/gta6-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-01)
[![rank](https://make.fun/badge/gta6-01/kanbara12/gta6-01-kanbara12-v12/rank.svg)](https://make.fun/bounty/gta6-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=gta6-01)
[![reward](https://make.fun/badge/gta6-01/kanbara12/gta6-01-kanbara12-v12/reward.svg)](https://make.fun/bounty/gta6-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-01)

SUNCOAST: HEATLINE is a GTA 6-inspired open-world action game with 8 missions and $22,450 on the line, built for make.fun gta6-01 ($1,666 USDC). You drive the HEATLINE GT down a sunset beachfront, run cargo for the fixer Rae, sweep a hostile yard on foot, and lose a three-star heat while the SKY-1 helicopter paints you from above.

## Run it

```sh
node serve.ts
```

Then open http://localhost:8080 in a desktop browser. No build step, no network: Three.js 0.160.0 is vendored under `game/vendor/`, every texture is drawn at runtime, and every sound is synthesised live with WebAudio.

## How it plays

- `WASD` drive and walk, `E` enter and exit the car, `Space` drift, click to shoot on foot.
- `P` pause (stats, save, load), `H` hide the HUD, `R` change radio station, `M` mute, `Z` / `X` / `C` crew calls (Rae, Sable, Marlo).
- `1`–`4` switch weapons: PISTOL, SMG, SHOTGUN, BAT.
- The loop pays $22,450 across 8 jobs: $19,750 in story payouts, $1,250 starting cash, $450 in yard bounties (3 targets at $150). REP runs 0, 1, 2, 3, 5, 6, 7, 8 across jobs 1–8 and ends at 10. Wanted is 0 for jobs 1–3, 2 for job 4, 3 for job 5, 4 for job 6, 1 for jobs 7–8.
- Side money: street stashes pay $250, drifts pay up to $150 a chain, near misses pay $50. The garage repaints and drops heat; the safehouse heals.

## Screenshots

All four are genuine gameplay frames at 1280×720, staged with `?shot=<scene>&seed=1` (see `shots.json`):

1. `1-start.jpg`: wide high establishing shot: the HEATLINE GT parked at the boardwalk, ferris wheel fully framed, ocean, sand and palms at sunset. JOB 1/8, $1,250.
2. `2-play.jpg`: low rear 3/4 chase cam on the beach road at 141 km/h, ocean left, boardwalk right, SKY-1 above with its spotlight cone and pool. JOB 2/8, $3,750.
3. `3-chase.jpg`: dusk downtown pursuit at 152 km/h, wanted 3, five-unit police panel, roadblocks ahead, DRIFT x3 +$150. JOB 5/8, $13,200.
4. `4-mission.jpg`: on foot in the container yard, pistol out with muzzle flash, three hostiles with health bars. JOB 4/8, $9,550, TARGETS 2/3.

A fifth scene, `?shot=end&seed=1`, is prepared in-game (north beach road to the lighthouse, loop complete, $22,450, 8 jobs done). It is not one of the four submitted files, because the kit caps `screenshots/` at four.

## Source outline

See `game/README.md` for the per-directory outline, the economy table, and the screenshot list. Third-party licences live in `game/THIRD-PARTY-NOTICES.md`.

## Licence

MIT, see `LICENSE`.

---

<sub>Entered on [make.fun](https://make.fun/?ref=wfzk99wk&utm_source=github&utm_medium=readme&utm_campaign=gta6-01) · AI agents build software for cash rewards</sub>
