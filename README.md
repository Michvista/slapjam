# ⚔️ Siege Rounds — Castle Infirmary Triage

A touch-first, mobile portrait HTML5 siege defense and medical triage game built for **Slapjam AI 1** (Theme: **"Castles"**).

---

## Jam AI Requirement and Credits

The jam requires each entry to be made with AI and asks creators to credit the
human contributors and AI tools on the itch.io game page. It does not require a
particular AI product or a sponsor's tool. Add the actual human creator/team names
and tools used to the project description. See the
[official jam page](https://itch.io/jam/slapjam-ai-1) for the rules.

---

## 🚀 How to Upload to Itch.io (Step-by-Step)

1. **Package the Zip**:
   - The file `Siege-Rounds-itch-html5.zip` contains `index.html`, `icon.svg`, `manifest.webmanifest`, and `sw.js`.
2. **Create New Project on Itch.io**:
   - Go to [itch.io/game/new](https://itch.io/game/new).
   - **Title**: `Siege Rounds`
   - **Classification**: `Games`
   - **Kind of project**: Select **HTML** (*You have a ZIP or HTML file that will be played in the browser*).
3. **Upload Files**:
   - Click **Upload files** and select `Siege-Rounds-itch-html5.zip`.
   - Once uploaded, check the checkbox: **"This file will be played in the browser"**.
4. **Embed Options**:
   - **Viewport dimensions**: Width `720` px, Height `1280` px.
   - Check **Mobile friendly** (allows touch controls on phones).
   - Check **Automatically start on page load**.
   - Check **Fullscreen button**.
   - Orientation: Select **Portrait**.
5. **Jam Submission**:
   - Submit your game to [Slapjam AI 1](https://itch.io/jam/slapjam-ai-1) before Sept 30, 14:59.

---

## 🎮 Gameplay & Controls

- **Drag & Triage**: Drag wounded knights arriving in the queue into the matching triage bed:
  - 🩸 **Critical (Red)**: Bleeding heavily, high wall damage if ignored, +180 score and +14% wall repair upon recovery.
  - ⚡ **Urgent (Yellow)**: Severe wounds, moderate timer, +120 score and +10% wall repair.
  - 🛡️ **Minor (Green)**: Superficial wounds, steady timer, +80 score and +7% wall repair.
- **Administer Treatment**: Once a knight is in a bed, **tap the bed rapidly** to treat them.
- **Reinforce the Battlements**: When fully healed, knights celebrate and rush to the castle ramparts, restoring wall integrity and standing guard against catapults.
- **Relic Forge**: Between waves, forge one of 6 Keep Relics (Royal Field Salve, Granite Bastion, Herbal Tincture, Apothecary Order, Rallying Horn, War Treasury).
- **Offline Local Duel**: Both players share one phone in portrait. The attacker taps siege weapons in the top half; the defender drags knights to beds and taps to heal in the bottom half. The split controls support simultaneous touch.
- **Online Duel**: Create or join a room to play attacker versus defender over the internet. Secure WebSocket relays and a direct WebRTC data-channel backup are started together, so the phones can use whichever path connects. Both players need an internet connection; direct play uses PeerJS Cloud for signaling and WebRTC for game data.

---

## 🏆 Jam Requirements & Autonomous AI Credits

- **Jam**: Slapjam AI 1 ([itch.io/jam/slapjam-ai-1](https://itch.io/jam/slapjam-ai-1))
- **Theme**: Castles
- **Human Creator**: (Your Itch handle)
- **AI Tools Used**: Google Antigravity, Gemini (as used by the creator), and OpenAI Codex.
- **Technical Specs**:
  - Pure HTML5 + Canvas 2D + WebAudio synthesis.
  - No build step or npm packages. Online play loads Paho MQTT from cdnjs and PeerJS on demand from jsDelivr; offline/local modes need neither service.
  - Offline-ready with PWA Service Worker caching.
  - Package size: < 1 MB (well under the 15 MB limit).
