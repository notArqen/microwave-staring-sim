# Microwave Staring Sim

A browser game about staring at a microwave, and deciding when to open the door. Solo, or online with 2-4 players (peer-to-peer).

Open `index.html` in a browser, or play it on GitHub Pages. Press `I` on the menu for the rules.

**Scoring:** open the door as late as you dare. Right before it ends is +15, 0.5s away is +14, 10s away is +3, 14s away is +1, 20s or more is 0. Letting it end is -5.

**Online:** one player hosts a room and shares the 4-letter code. Connections use WebRTC via the public [PeerJS](https://peerjs.com) broker (loaded from jsDelivr) and Google STUN servers. No game data passes through a server after connecting.

**Music:** none is bundled. A synthesized techno loop plays instead. To use your own, add a looping `music/track.mp3`.

## Credits

- [three.js](https://threejs.org) (MIT)
- [PeerJS](https://peerjs.com) (MIT)
- Room tone: "creepy industrial sounds ambience" by Dragon-Studio, via Pixabay
