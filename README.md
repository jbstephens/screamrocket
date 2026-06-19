# SCREAM ROCKET

A voice-controlled rocket game for the family arcade. Single self-contained `index.html` — HTML5 canvas + vanilla JS + Web Audio API.

**Squeal high to bank right, growl low to bank left, and the louder you are the higher you climb.**

## How to play
- **Volume** controls thrust. Silence = the rocket falls. Scream = max thrust.
- **Pitch** steers. High squeals bank right, deep growls bank left, mid keeps you straight.
- Dodge asteroids, satellites, space junk — and Zorg's UFO if he comes calling.
- Match the tone gates (LOW / MID / HIGH) for big points.
- Hum a steady tone to charge a one-hit shield.
- The pink Stealth Cloud has a sleeping space-creature inside — go quiet to drift past, or it wakes up and chases.
- Hold full scream too long and the engine overheats — steering gets twitchy.
- Every ~4,500 altitude you face **The Howler** — match the boss's target pitch with full volume.

## Pilots
Ben, Luke, Mom, Dad.

## Running locally
Mic access requires HTTPS (or `localhost`).

```
cd screamrocket
python3 -m http.server 8000
# then open http://localhost:8000
```

For real device testing on the iPad you'll need to host it on Netlify / Vercel / GitHub Pages / Render — `file://` will silently fail to get the mic.

## Game console integration
This folder is meant to be dropped into `gameconsole/games/screamrocket/`. The console will load `index.html` directly and inject a back button.

## Leaderboard (Supabase, optional)
Stub is at the bottom of `index.html`. Drop in your URL + anon key, create the `scream_rocket_scores` table, and uncomment the submit code.

## Tunables
All gameplay constants live in the `TUNE` object near the top of the `<script>` block — edit those to balance with the kids.
