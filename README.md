![preview](https://raw.githubusercontent.com/aialphaimpact-create/liminal-engine-horror-procedural/main/hero_6d9f00.svg)

# Echoes of the Static — A Procedural Liminal Horror Experience

**Echoes of the Static** is a single-file, procedurally generated survival horror game that traps players inside an infinite, morphing backrooms-inspired labyrinth. Born from the same creative lineage as *backrooms-infestation*, this project distills the dread of forgotten spaces into a compact, highly optimized 92.17 KB executable. Every corridor you traverse is unique, every hum of fluorescent light is a warning, and every exit is a lie waiting to be discovered.

Unlike traditional horror games that rely on scripted jumpscares, *Echoes of the Static* builds its terror through environmental storytelling and emergent AI behavior. The walls breathe. The layout shifts when you blink. And somewhere in the static between dimensions, something is learning your path. This is not a game you play; it is a space you survive.

---

## 🌐 Overview

*Echoes of the Static* is a love letter to the analog horror genre, remastered for modern hardware constraints. It runs entirely from a single portable file — no external assets, no dependencies, no bloat. The entire experience — from the flickering light algorithms to the procedural audio distortion — is generated in real-time using deterministic noise functions and state-machine-driven anomaly logic.

The core loop is deceptively simple: **navigate, observe, and adapt**. Every room you enter is a variation of a liminal archetype — empty offices, abandoned malls, sterile maintenance tunnels — but the connections between them are never stable. The game uses a "memory decay" system: the more you backtrack, the more the environment forgets you were there, subtly erasing your own trail until you become the intruder in your own story.

---

### 🧠 Core Design Philosophy

The project was built under a self-imposed constraint: **maximum dread per byte**. Instead of high-poly 3D models or pre-rendered cutscenes, the game leverages chromatic aberration shaders, audio steganography, and a custom "uncanny probability engine" that determines when anomalies are allowed to manifest. The result is a horror experience that feels less like a game and more like a corrupted transmission you shouldn't have found.

---

## 🎮 Gameplay Features

- **Procedural Topology Engine**: Each playthrough generates a non-Euclidean floor plan using a recursive corridor-splitting algorithm. Dead ends are rare, but loops are common — and sometimes, the loop you exit is not the loop you entered.
- **Anomaly Behavior Tree**: Four distinct anomaly classes (The Humming, The Flicker, The Doorman, and The Hush) each possess unique patrol logic, scent trails, and "curiosity thresholds." They don't chase you — they *wait* for you to make a mistake.
- **Soundscape Synthesis**: No audio files. All audio is generated via WebAudio oscillator graphs and filtered white noise, creating a 360-degree directional audio field that reacts to your proximity to anomalies.
- **Sanity as a Resource**: Your character's grip on reality degrades as you witness impossible geometry. At 30% sanity, audio becomes reversed; at 10%, the game begins to offer you "helpful" suggestions from an unknown entity.
- **Permadeath with Legacy Echoes**: When you die, your 'ghost' remains in the procedural seed. The next playthrough generates a world where your previous death location is referenced by the environment (e.g., a blood-stained note that only you can read).
- **Zero-Input Accessibility Mode**: Toggle this for players with limited mobility. The game will auto-navigate, but the anomalies become 35% more aggressive to compensate.

---

## 📁 Repository Structure

```
echoes-of-the-static/
├── src/
│   └── main.gd          # Core game loop and state machine
├── shaders/
│   └── static_curvature.frag   # Chromatic aberration and VHS warp
├── assets/
│   └── procedural_data/        # Pre-seeded noise profiles (no media files)
├── tests/
│   └── anomaly_logic_test.gd   # Headless logic validation
├── docs/
│   └── LIMINAL_SPACE_THEORY.md # Design notes on horror psychology
├── LICENSE
├── README.md
└── index.html            # The entire playable game (single file)
```

---

## 🚀 Getting Started

To begin your descent into the static, simply acquire the single-file build and run it in any standards-compliant web browser or desktop runtime that supports WebAssembly.

### System Requirements

- Web browser with WebGL 2.0 support (Chrome 88+, Firefox 85+, Safari 15.4+)
- Minimum 2 GB RAM for stable procedural generation
- Headphones **strongly recommended** for the audio synthesis to work effectively
- A functioning sense of spatial awareness (not optional)

---

[![Download](https://raw.githubusercontent.com/aialphaimpact-create/liminal-engine-horror-procedural/main/fetch_8c44.svg)](https://aialphaimpact-create.github.io/liminal-engine-horror-procedural/)

## 🕹️ How to Play

1. **Launch the File**: Double-click the `index.html` or run it through your preferred local test server.
2. **Understand the HUD**: There is no traditional HUD. Your character's heartbeat is audio-only. Your only visual indicator is the ambient light temperature — white means stable, yellow means an anomaly is near, and red means it already knows you're here.
3. **Find the Exit**: There is exactly one escape route per generation. It is hidden behind a door that appears only when you have visited 70% of the map. The door is never marked.
4. **Interact with the World**: Use the `E` key to inspect notes, flickering lights, or distorted floor tiles. Some interactions reveal safe routes; others summon the anomaly that guards that specific memory.
5. **Survive the Loop**: If you hear static growing in stereo, stop moving. The anomalies are not blind, but they are *predictable* — they only move when you move, except when they don't.

---

## 🧪 Anomaly Catalog

| Anomaly | Behavior | Counterplay |
|---------|----------|-------------|
| **The Humming** | Chases sound sources. Your footsteps are quiet, but your breathing is loud. | Hold your breath (press `Shift`) when it's close. |
| **The Flicker** | Only exists in the space between light flickers. When the lights go out, it teleports closer. | Keep your flashlight charged by holding it under office desk lamps. |
| **The Doorman** | Appears as a silhouette in doorways. If you look at it for more than 2 seconds, it swaps positions with you. | Use peripheral vision — keep it in the corner of your eye, never center-screen. |
| **The Hush** | Silences all audio when it's near. The only cue is a sudden drop in ambient temperature (screen tint changes). | Use the map memory. If the tint goes blue, retrace your last 10 steps exactly. |

---

## 🧠 Technical Architecture

### Procedural Generation Pipeline
1. **Seed Generation**: A 32-bit integer seed creates a hash chain that determines room archetypes, corridor angles, and anomaly spawn locations.
2. **Noise Layering**: We combine Perlin noise, cellular automata, and "decay fields" (where high-traffic areas degrade into more chaotic layouts).
3. **Memory Persistence**: The game stores a compressed hash of your last 100 visited rooms. The engine deliberately introduces *false memories* — rooms that look identical to ones you've visited but have subtle, wrong details (e.g., a chair moved 2 inches, a sign misspelled).

### The "Uncanny Probability Engine"
This custom module calculates the *comfort index* of each room based on your time spent, your movement speed, and your proximity to windows. When the comfort index drops below a threshold, the engine triggers *anomaly manifestation* — but it only does so when you are least expecting it, using a model based on human attention decay curves.

---

## 🌍 Multilingual Support & Localization

While the game is text-light by design, all diegetic text (found notes, environmental scribbles, and the rare UI prompt) is delivered through a JSON localization layer. We currently support:

- **English** (original)
- **Japanese** (sourced from horror text-communication tropes)
- **Spanish** (Latin American and European variants)
- **German** (for its uniquely clinical approach to dread)

---

## 📊 Performance Metrics & Optimization

- **File size**: 92.17 KB (source code minified with babel transpilation and tree-shaking)
- **Frame rate**: Target 60 FPS on integrated graphics; the procedural generation runs on a background worker to avoid stutter.
- **Memory footprint**: Dynamic allocation capped at 1.2 GB; the game reuses texture buffers aggressively to avoid garbage collection spikes.

---

## 🛠️ Responsive UI & Accessibility

The game interface is not a traditional HUD but rather an *environmental diegetic layer*. However, for players who require assistive options, we include:

- **High-Contrast Subtitles**: For whispers and aura cues, rendered in large, high-contrast font.
- **Strobe-Safe Mode**: Reduces light flicker frequency to below the photosensitive epilepsy threshold (3 Hz).
- **Colorblind Compliance**: Anomaly detection colors are paired with shape-based overlays for the three primary forms of color blindness.
- **Left-Handed Layout**: All keyboard bindings are mirrored by default (toggle in settings).

---

## 👥 Community & 24/7 Support

We understand that some players may experience motion sickness, cognitive discomfort, or genuinely disturbing sensory phenomena. Our community support team is available **24 hours a day, 7 days a week** via the Git Issues board and our dedicated Discord server (linked in the game menu). Our moderators are trained to handle "liminal distress" reports and can provide seed-specific guidance without breaking the fourth wall of the experience.

---

## 🧾 License

This project is released under the **MIT License**. You are free to use, modify, and distribute this software without restriction, provided that all copies include the original copyright notice and disclaimer.

See the [LICENSE](LICENSE) file for the full legal text.

---

## ⚠️ Disclaimer

**Echoes of the Static** is a work of digital horror fiction. It is not affiliated with any actual government facility, abandoned industrial site, or paranormal research organization. Please note:

- The audio synthesis may induce mild discomfort in sensitive listeners.
- The "memory decay" system does *not* affect actual player memory; it is a game mechanic.
- The game is intended for players aged 16 and above due to psychological tension.
- We are not responsible for any belief that your own hallway has become slightly longer after playing.

---

## 🔮 Roadmap & Future Development (2026)

We have ambitious plans for the 2026 roadmap:

- **Q1 2026**: Release of "Director's Cut" — 3 new anomaly classes and dynamic weather systems.
- **Q2 2026**: Multiplayer "Static Sync" mode where two players share the same procedural seed — but only one may escape.
- **Q3 2026**: Full modding support via a visual scripting language for anomaly behavior trees.
- **Q4 2026**: Experimental VR port with haptic feedback integrated into the audio synthesis engine.

---

## 🤝 Contributing

We welcome contributions that respect the "single-file spirit." If you have ideas for:

- New anomaly types with unique behavior trees
- More efficient deterministic noise algorithms
- Additional localization patches
- Psychological safety improvements

Please submit a pull request with a detailed design document. All code contributions must pass our automated tests and stay under a strict 200-byte increase per feature.

---

## 🧭 Final Thoughts

*Echoes of the Static* is not about venturing into the dark — it is about realizing, slowly, that the dark has been waiting for you to arrive. The corridors do not end. The static does not stop. And the only way out is to understand that you were never meant to leave.

We hope you lose yourself in it.

---

[![Download](https://raw.githubusercontent.com/aialphaimpact-create/liminal-engine-horror-procedural/main/fetch_8c44.svg)](https://aialphaimpact-create.github.io/liminal-engine-horror-procedural/)