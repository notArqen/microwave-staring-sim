# Microwave Staring Sim

A browser game about staring at a microwave, and deciding when to open the door. Solo, or online with 2-4 players (peer-to-peer).

Open `index.html` in a browser, or play it on GitHub Pages. Press `I` on the menu for the rules.

**Scoring:** open the door as late as you dare. The last 0.002 seconds is +15, then +14 out to about 0.25s, +13 at 0.5s, +12 at 1s, +8 at 5s, +3 at 10s, +1 at 14s and 0 from 20s on. Letting it end is -5. Opening after the clock has hit zero counts as letting it end.

**Online:** one player hosts a room and shares the 4-letter code. Connections use WebRTC via the public [PeerJS](https://peerjs.com) broker (loaded from jsDelivr) and Google STUN servers. No game data passes through a server after connecting. Five rounds, a different timer for everyone each round, most points wins.

**Music:** a synthesized dark techno track plays by default, heard "through a wall" (room reverb, highs cut). The window outside flashes blue on every kick. To use your own music, open **Settings** on the menu and load an audio file (mp3, wav, ogg or m4a, 40 MB max). It is stored only in your browser (IndexedDB) and is never uploaded. The game measures its tempo so the lights lock to the beat.

## Credits

- [three.js](https://threejs.org) (MIT)
- [PeerJS](https://peerjs.com) (MIT)
- Room tone: "creepy industrial sounds ambience" by Dragon-Studio, via Pixabay
