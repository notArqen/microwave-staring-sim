# Sump Clerk

**Keep it level.**

A one-room night-shift horror game for the browser. You work the pumps in a sealed station from 22:00 to 06:00, trimming pressure valves to keep three needles in the green. Something else is on the wall.

**Play:** <https://notarqen.github.io/microwave-staring-sim/sump-clerk/>

Open `index.html` through any local web server, or play it on GitHub Pages. It needs a modern desktop browser with WebGL. Headphones and a dark room are recommended.

> **Warning:** flickering lights, a pulsing red alarm light, loud sounds and unsettling themes.

## How to play

- **Drag a wheel right (+)** to raise that pump's pressure, **left (-)** to lower it. The slider under each wheel shows where the valve is set.
- Keep every needle in the green. A needle that stays out of the green too long trips the pump, which costs a fault. Run out of faults and the station floods.
- **Move the cursor to look around.** A centred cursor frames the three pumps; the far right looks along the east wall.
- **Click the ledger** on the desk to read it. The shift keeps running while you read.
- Hold until 06:00.

## Settings

`S` on the menu (or click "[ S ] SETTINGS"). `Esc` goes back.

- **Difficulty:** TOO EASY, EASY, MEDIUM, HARD, BRUTAL. This changes how wide the green is, how many faults you get, how long a needle can sit out of the green, how fast the needles drift, and how early and fast the thing on the wall arrives.
- **Game length:** 3, 5, 8 or 12 minutes for the whole shift. Everything scales with it.
- **Music:** none by default. You can load your own audio file (up to 80 MB); it plays from very far away, as if through the earth. The file is kept only in your browser (IndexedDB) and is never uploaded. There is a Remove button.

## How it is made

A single `index.html` with [three.js](https://threejs.org) (r128, MIT). The scene renders at a low resolution, never above your screen's native resolution, then goes through a six-tone palette with Bayer dither, grain and a vignette. Vertex positions snap to the pixel grid, textures are generated procedurally, text is drawn inside the same filter, and all sound is synthesised live with the Web Audio API. There are no image or audio files.

It loads `../three.min.js` from this repository and falls back to cdnjs if that file is missing. Your settings (difficulty, length, music) are stored in your browser's localStorage and IndexedDB.

Optional URL flags: `?skipintro` skips the opening, `?mute` disables sound, `?h=300` sets the render height (capped at native).

## Credits

- [three.js](https://threejs.org) (MIT)
- Inspired by the look of low-resolution, dithered analogue-horror games. No art, music or code from other games is used.
