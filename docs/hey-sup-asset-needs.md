# hey, sup? — Asset Needs Assessment

*October 8, 2026. First production pass: what we have, what we need, and what blocks what. Theme: pure 90s retro — the gardening theme was removed 2026-10-08.*

## Art direction — DECIDED 2026-10-08: 2D chibi

Side-scrolling 2D in **2D chibi: thick outlines, flat colors, expressive faces** (the look of the duo sprite sheets and avatar work). Reads well at mobile sizes, cheap to animate, and the video-to-sprite pipeline already produces it. Selfie Social Society's "warm storybook 3D" direction does **not** carry over. Squirmy's current render (glossy 3D) gets redone in 2D chibi to match.

## What exists already

- Duo sprite sheets (him + her): 9 actions each — idle, walk, run, jump, double jump, crawl, roll, dusting attack, victory. Extracted from generated video; keyboard backgrounds baked in (need transparent re-exports).
- Shared cinematic sheet: both characters in frame, same 9 actions.
- Squirmy the worm: one static image (needs 2D chibi restyle + animation).
- Concept doc: `hybrid-multiplayer-concept.md`.

## Production decisions — ALL DECIDED 2026-10-08

1. **Player character system:** preset cast — literally the user + wife as the playable characters, who also serve as the game's mascots (title screen, tutorials, branding). Cast can expand later.
2. **Art direction:** 2D chibi.
3. **Minigame designs:** multiplayer-first collection — Mullet Kart 64, Mall Brawl, Buck Hunt, Toxic the Hedgehog, Brick Game, Recess, WEEDSWEEPER, Arcade Cadet, Super Market Bros; SkiFlea for solo/async.

## P0 — first playable

**Characters**
- The duo re-exported on transparent backgrounds (current sheets have keyboards baked in).
- Confirm the 2D chibi look as final against the sheets.

**Bedroom (home base) — TWO starter rooms**
- His plain bedroom + her plain bedroom: bare walls, bed, dresser, window, door. Deliberately sparse — customization is progression.
- Decor catalog (unlock with progress): posters, VHS shelf + tapes, CRT TV, pog board, lava lamp, beanbag, skateboard, CD rack, plushie shelf.
- Room module: walls, floor, window (day/night variants).

**Street (side-scrolling world)**
- Parallax set: sky (day + night), distant rooftops/trees, 90s houses, arcade exterior, mall entrance.
- Sidewalk tiles, street props (fire hydrant, bike, basketball hoop).

**Phone UI**
- Phone chrome + home screen.
- App icons: Room, Events, Mailbox, Friends (core four for first playable).
- Texting UI: message bubbles, typing indicator, small emoji set.

## P1 — the full game

**Bedroom expansion**
- Full decor catalog: beanbag chairs, lava lamps, sticker collections, plushie shelf, CD rack, skateboard.
- VHS tapes: collectible designs (parody titles).
- Pog collection UI.

**World expansion**
- Arcade interior: cabinets (parody titles), prize counter, neon signage, token slot. DONE 2026-10-08 (imagine_media/media-generation-heysup-arcade-interior-0-*.webp)
- Mall food court: tables, burger/pizza/smoothie stands, skylight. DONE 2026-10-08 (imagine_media/media-generation-heysup-food-court-0-*.webp)
- Cubicle Maze — the idle screensaver: simulated-3D cubicle walls.
- Seasonal variants (summer/winter palettes, holiday mall dressing).

**Phone UI expansion**
- Remaining apps: Settings, BAM (messenger), TamaGotcha, MyPlace, BoomBox, BlockQuest, Ask Beavis.
- Voice call UI (incoming call screen, in-call), FaceTime-style video call UI.
- Notifications + lock screen.

**Nostalgia parody branding** (cheap, high charm — good early win)
- Wordmarks/logos: MyPlace, BAM, A-OK Online, Panes 96, ISeeU, BoomBox, Ask Beavis, BlockQuest, NapTime, TamaGotcha, plus minigame logos (Mullet Kart 64, Mall Brawl, Buck Hunt, Toxic the Hedgehog, Brick Game, Recess, WEEDSWEEPER, Arcade Cadet, Super Market Bros, SkiFlea).
- Boot sequence art: dial-up → Panes 96 desktop parody.
- Blue Screen of GAME OVER.

**Minigames**
- Mullet Kart 64: track tiles (suburban streets), racer sprites, lunch-tray projectiles, soda-spill boost strips, start/finish arch.
- Mall Brawl: food-court arena, knockback effects, edge-fall animation.
- Buck Hunt: critter targets (3 types), mascot (don't shoot!), crosshair/tap effects.
- Toxic the Hedgehog: race track segments, barrel obstacles, spin effect, timer UI.
- Brick Game: brick pieces (5 colors), versus boards, line-clear burst effects.
- Recess: dodgeball/kickball/tetherball mini-kits.
- WEEDSWEEPER: tile states (covered, uncovered, flagged), mimes, numbers, safe tiles, UI frame.
- Arcade Cadet: pinball table, flippers, bumpers, steel ball.
- Super Market Bros: platform tiles, cereal-box blocks (the ?-blocks), enemy shoppers?, conveyor belts, freezer-aisle flagpole.
- SkiFlea (solo): endless slope segments, flea-market tables, yeti.
- Elimination: bracket UI, arena dressing, trophy.
- Rhythm/dance: BoomBox DJ booth, dance floor tiles, beat indicators.

**NPCs & antagonists**
- Squirmy: 2D chibi restyle + animations (idle, popup, point, celebrate, "dismissed" poof).
- **EMO US** (arch-nemeses): same outfits as the duo, paler skin, long droopy emo bangs over one eye (user-corrected 2026-10-08 — NOT the all-black redesign). Both transparent sheets DONE + keyed 2026-10-08 (imagine_media/heysup-emo-him-sprites-transparent.png, heysup-emo-her-sprites-transparent.png — each mirrors its original's layout row-for-row).
- Arcade staff / mall characters (TBD — can reuse chibi style).

**Virtual pet (TamaGotcha)**
- Purrby: egg, baby, adult stages; idle/hungry/cranky/sleeping/celebrating animations. Deliberately NOT garden-themed.
- TamaGotcha app UI: stats (hunger, happiness, discipline), minigame link.

**Audio** (specs; the audio sampler tool can produce these)
- Dial-up handshake, Panes-96-esque chime, "YOU'VE GOT MAIL!" voice line, BAM door creak/slam, ISeeU "uh-oh!", critical-stop *ding*, connecting screech.
- Ambience: suburban day/night, arcade interior, mall food court.
- Music: BoomBox dance tracks, minigame stingers, victory jingle.

## P2 — later

- Cinematics: storyboard + sheets (shared sheet exists as a start).
- Seasonal decor sets, holiday events.
- Advanced phone features (video call backgrounds, custom ringtones).

## Reuse from Selfie Social Society

- Multiplayer architecture only (Firebase-only plan: Auth, Firestore, RTDB). No asset reuse — different art direction, different theme. The gardening system design doc stays with SSS.

## Suggested build order

1. Transparent re-exports of the duo sheets; lock 2D chibi style guide.
2. P0 bedroom + street + phone chrome → walkable 90s street.
3. Texting (BAM) between two players → first real multiplayer moment.
4. TamaGotcha (Purrby) → the cozy loop lands.
5. First scheduled event (minigame night: WEEDSWEEPER or Mullet Kart 64) → the loop closes.
6. Parody branding pass → the game's personality lands.
7. Everything else in P1 order.
