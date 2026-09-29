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
- **Campaign challenge**: Solo waves require rescuing a rising 72–78% quota and keeping a rising minimum amount of wall integrity. Local and online duels have four 30-second phases. The defender must rescue **3 / 4 / 5 / 6 knights** and finish each phase with at least **70 / 55 / 40 / 25 wall HP**, in order. Missing any phase quota or wall threshold, or letting the wall reach 0 HP, gives the attacker the win. The defender wins only after all four phases, with at least 6 rescues in the final phase and 25 wall HP remaining.
- **Online rematches**: Both players, including the host, press **Continue** after a duel. The ready player sees a waiting status until the other player is ready; then both games restart together. The result-screen button remains **Continue** for the active online room.
- **Attacker scoring**: Every siege action earns points, with a victory bonus weighted by speed and damage dealt.
- **Offline Local Duel**: Both players share one phone in portrait. The attacker taps siege weapons in the top half; the defender drags knights to beds and taps to heal in the bottom half. The split controls support simultaneous touch.
- **Online Duel**: Create or join a room to play attacker versus defender over the internet. It tries secure WebSocket and WebRTC links, with an HTTPS streaming relay as a browser-friendly fallback for restrictive mobile browsers. Both players need internet access. Copy/paste the 20-character invite on phones.

  The HTTPS fallback uses the public [ntfy.sh](https://ntfy.sh) service without an account. Room topics are public to anyone who knows the invite, and messages are cached by the service; the invite is long and randomly generated, but it is not account authentication or end-to-end encryption. Do not share personal information in a room. ntfy.sh documents a 250-message daily cap, so this is intended for short casual matches. Online play depends on third-party relays being reachable; offline local duel does not.

---

## 🏆 Jam Requirements & Autonomous AI Credits

- **Jam**: Slapjam AI 1 ([itch.io/jam/slapjam-ai-1](https://itch.io/jam/slapjam-ai-1))
- **Theme**: Castles
- **Human Creator**: (Your Itch handle)
- **AI Tools Used**: Google Antigravity and OpenAI Codex.
- **Technical Specs**:
  - Pure HTML5 + Canvas 2D + WebAudio synthesis.
  - No build step or npm packages. Online play uses public HTTPS/WebSocket relays and loads Paho MQTT and PeerJS on demand; offline/local modes need no network service.
  - Offline-ready with PWA Service Worker caching.
  - Package size: < 1 MB (well under the 15 MB limit).
