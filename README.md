# Microwave Staring Sim

A browser game about staring at a microwave and deciding when to open the door. Solo, or online with 2-4 players (peer-to-peer).

**Also here:** [Sump Clerk](sump-clerk/), a one-room night-shift horror game about keeping three needles in the green until 06:00. Play it at [/sump-clerk/](https://notarqen.github.io/microwave-staring-sim/sump-clerk/).

**Opening:** a black screen with one click (browsers need a click before they will play sound), then the Dithered Dread logo fades in over low ambience and fades out, about five seconds of pure black, and the menu hard-cuts in. Going back to the menu from inside the game skips it. Add `?skipintro` to the address to skip it yourself.

Open `index.html` in a browser, or play it on GitHub Pages. `I` on the menu shows the rules, `S` opens settings, `Esc` goes back to the menu from anywhere.

**Solo:** the timer is a random 0:15 to 3:00 each run. Turn that off in **Settings** to pick your own (`1`-`6` or the arrow keys).

**Scoring (Normal):** open the door as close to the alarm as you can.

| seconds away | points |
|---|---|
| the last few milliseconds | +15 |
| 0.5 s | +5 |
| 1 s | +3 |
| 2 s | +2 |
| 4 s | +1 |
| 8 s or more | 0 |

Letting it ring costs points. **Difficulty** (Settings for solo, the host's lobby for online) squeezes the distances and raises the penalty: Easy -3, Normal -5, Hard -8, Brutal -12.

Leave it ringing and the alarm gets louder, the screen darkens from the edges and the camera shakes. Open the door after it has gone off and you get a defibrillator-style black-out, then a white-out that fades back to normal.

**Online:** one player hosts a room and shares the 4-letter code (Backspace fixes a typo, Delete clears, you can paste). Connections use WebRTC via the public [PeerJS](https://peerjs.com) broker (loaded from jsDelivr) and Google STUN servers. No game data passes through a server after connecting. Five rounds with a 10 second wait before each countdown, a different timer for everyone, a stacked layout for 3-4 players, and you can hear the others' microwaves, quietly. Everyone is told when someone leaves. If a VPN or strict network blocks peer-to-peer links, the room will fail to connect; try without the VPN or on another network.

**Music:** a synthesized dark techno track plays by default, heard "through a wall" (room reverb, highs cut), and the window outside flashes blue on every kick. **Settings** can switch to the Legacy Synth (the original track) or load your own audio file (mp3, wav, ogg or m4a, 40 MB max). Your file is stored only in your browser (IndexedDB) and is never uploaded, and the game measures its tempo so the lights lock to the beat.

## Credits

- [three.js](https://threejs.org) (MIT)
- [PeerJS](https://peerjs.com) (MIT)
- Room tone: "creepy industrial sounds ambience" by Dragon-Studio, via Pixabay
