# SUNCOAST: HEATLINE — source outline

An open-world crime game in the spirit of GTA 6, built from static files under
`game/` with no build step. Three.js 0.160.0 is vendored under `game/vendor/`.
Everything else is original: the city, the characters, the vehicles, the
story, the art and the sounds. Play makes no network request. Every
texture is drawn on a canvas at runtime and every sound is synthesised live
with WebAudio.

## Files

- `game/index.html` — page shell and the whole HUD (mission panel, money and
  wanted panel, named police panel, radio and weapons, speedometer, round
  minimap, dialogue card, title screen, pause menu).
- `game/src/config.js` — tuning, economy and screenshot staging: the world
  layout, the 8 jobs, REP and wanted tables, and the five `?shot=` scenes
  with their exact job, cash, REP, jobs done, wanted, timer and speed.
- `game/src/world.js` — the world: gradient sunset sky with a low sun disc,
  animated ocean with foam and sun glitter, sand, beach road and cross
  streets, 190+ buildings with lit windows, leafy palms, ferris wheel,
  boardwalk kiosks, pier, lighthouse, container yard, garage, safehouse and
  the glowing mission marker.
- `game/src/vehicles.js` — the HEATLINE GT hero coupe (sloped hood, raked
  glass, flared arches, spoiler, twin exhausts, driver), traffic cars,
  police cars, the SKY-1 helicopter with its spotlight cone and pool,
  pedestrians, the on-foot player with a visible pistol and muzzle flash,
  and yard enemies with health bars.
- `game/src/main.js` — boot, game loop, driving and walking, missions and
  the $22,450 economy, police pursuit and helicopter, HUD and minimap,
  camera rigs and the five staged screenshot scenes.
- `game/src/audio.js` — WebAudio synthesis: engine hum, gunfire, pickups
  and three original radio stations (SHORELINE 96.7, PIER 102.5, DUNE 89.9).

## Economy — 8 jobs, $22,450 total

| # | Mission | Payout | Cash after |
|---|---|---|---|
| 1 | A FAVOR IN THE HEAT — meet Rae at the marker | $2,500 | $3,750 |
| 2 | LOOSE CARGO — pick up the sealed package | $2,500 | $6,250 |
| 3 | THE QUIET EXIT — deliver across town, low heat | $3,000 | $9,250 |
| 4 | STREET SWEEP — clear the yard crew (3 targets, $150 bounty each) | $3,500 + $450 | $13,200 |
| 5 | NO WITNESSES — reach the garage, lose the heat | $4,250 | $17,450 |
| 6 | LAST LIGHT — final run at dusk, roadblocks | $2,000 | $19,450 |
| 7 | THE MARINA SWAP — case swap at the marina | $1,500 | $20,950 |
| 8 | NORTH LIGHT — north-beach run to the lighthouse | $1,500 | $22,450 |

Story payouts sum to $19,750; plus $1,250 starting cash and $450 in yard
bounties the loop total is $22,450. REP runs 0, 1, 2, 3, 5, 6, 7, 8 across
jobs 1–8 and ends at 10. Wanted is 0 for jobs 1–3, 2 for job 4, 3 for job 5,
4 for job 6, 1 for jobs 7–8.

## Screenshots

Four genuine gameplay frames at 1280×720, staged with `?shot=<scene>&seed=1`:

1. `1-start.jpg` — wide high establishing shot at the boardwalk (JOB 1/8, $1,250).
2. `2-play.jpg` — beach-road chase at 141 km/h with SKY-1 above (JOB 2/8, $3,750).
3. `3-chase.jpg` — dusk downtown pursuit, wanted 3, drift popup (JOB 5/8, $13,200).
4. `4-mission.jpg` — on foot in the container yard, pistol and muzzle flash (JOB 4/8, $9,550, TARGETS 2/3).

A fifth scene, `?shot=end&seed=1`, is prepared in-game (north beach road to
the lighthouse, loop complete, $22,450, 8 jobs done). It is not one of the
four submitted files, because the kit caps `screenshots/` at four.

## Controls

WASD drive and walk, E enter and exit the car, Space drift, click to shoot on
foot, P pause, H hide the HUD, R radio, M mute, Z / X / C crew calls,
1–4 switch weapons. Save and load live in the pause menu (localStorage).
