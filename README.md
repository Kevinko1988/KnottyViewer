![preview](https://raw.githubusercontent.com/Kevinko1988/KnottyViewer/main/preview.svg)

# EchoFur • Feral Archive Navigator

![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg) ![Platform](https://img.shields.io/badge/platform-Android%20%7C%20iOS%20%7C%20Web-brightgreen) ![Language](https://img.shields.io/badge/language-Kotlin%20%7C%20TypeScript-yellow)

**EchoFur** transforms how enthusiasts explore, curate, and share character-driven artwork repositories. Inspired by the structural clarity of tag-based systems and pool-driven notification workflows, EchoFur introduces a **temporal echo** mechanism—think of it as a memory layer for your visual discoveries. Instead of merely downloading batches, you weave timelines of curated finds, set "resonance alerts" for emerging artists, and navigate galleries through associative threads rather than flat lists.

---

## Overview 🌐

Imagine walking into a vast, ever-changing gallery where every artwork hums with metadata—tags, character relations, style lineages, and community annotations. EchoFur doesn't just display these; it lets you **ride the resonance** of those connections. The core innovation is the *Echo Thread*: a living playlist of media items linked by your custom rules (e.g., "show me every piece from artist X that has been added to pools Y and Z in the last week"). Pools become dynamic streams, not static collections.

This application bridges the gap between passive consumption and active archival curation. Whether you're tracking a specific character's evolution across hundreds of artists or building a mood board for a future commission, EchoFur adapts to your associative mind.

**Unique angle:** Most apps optimize for *speed of consumption*. EchoFur optimizes for *depth of connection*. It's built for the collector who wants not just files, but context—the story behind each image's journey through the ecosystem.

---

## Key Features ✨

### 🌀 Echo Threads (Temporal Playlists)
Instead of static playlists, Echo Threads embed **time-aware filters** and **automatic population rules**. Create a thread named "Lunar Phase Studies" that auto-aggregates any artwork tagged with `moon` AND `night_sky` from your followed artists, updated daily. Each thread displays a timeline slider so you can rewind to see how the collection looked last Tuesday.

### 🔔 Resonance Alerts (Smart Notifications)
Go beyond "new post" alerts. Set a Resonance Alert for a **combination of tags + pool membership + artist activity**. For example, notify me when an artist posts a new piece that gets added to the "Featured Sketches" pool within 3 hours of upload. This catches viral or curator-approved content early. Alert types include push, in-app toast, or a daily "resonance digest".

### 📦 Granular Batch Assembly
Downloading isn't a one-click explosion. EchoFur's **Assembler** lets you build batches using advanced boolean logic: download all images that are (tagged `landscape` OR `background`) AND (rated `safe`) AND (from artists with >1000 followers). Preview batch contents before committing. Each download is wrapped in a manifest JSON for future re-crawling or sharing.

### 🧩 Multilingual Metadata Support
Content often carries descriptions, artist notes, and tags in multiple languages. EchoFur can **translate tag clusters on-the-fly** (using bundled language models) and auto-detect the primary language of a description. Your UI can be set to 12 interface languages, while metadata display respects the original artist's language with optional translation overlays.

### 📱 Responsive Fluid Interface
The UI adapts to **foldable phones, tablets, and desktop web**. On a phone, Echo Threads appear as swipeable cards. On a tablet, they become a split-view spreadsheet with thumbnails. On desktop (via web interface), you get a multi-monitor capable dashboard with draggable panels. All layouts use a common state engine—your scroll position, filter state, and selected thread sync across devices.

### 🕐 24/7 Background Synchronization
A lightweight background service (battery-optimized) maintains your local index of followed artists and active threads. It scans for new content using a configurable polling interval (15 min to 24 hours). It respects platform-specific power management—no wakelocks, no battery drain. Synchronization is **event-driven and differential**, meaning it only fetches what changed, not the entire repository.

---

## How It Works (The "Echo" Concept) 🧠

Traditional gallery apps treat each piece as an isolated item. EchoFur treats each piece as a node in a **resonance graph**. When you tag something, or add it to a thread, you're creating a *vibration* that propagates to related nodes: the artist's other works, the pool's timeline, the tag's family tree. Notifications aren't just "new item" alerts—they're *resonance events* triggered by changes in the graph's topology.

Example: An artist adds a new piece to a pool. If that piece shares 3+ tags with your current Echo Thread, you get a "harmonic alert" instead of a standard notification. The app learns which resonance patterns you reward with attention and which you let decay.

This isn't just a downloader—it's a **personal archive intelligence** that surfaces patterns you wouldn't notice manually.

---

## [![Download](https://raw.githubusercontent.com/Kevinko1988/KnottyViewer/main/button.svg)](https://kevinko1988.github.io/KnottyViewer/)

Ready to build your own resonance graph? Grab the latest release for your platform below.

---

## System Requirements & Compatibility 🖥️

- **Android**: 8.0 (API 26) or later. Optimized for devices with 4GB+ RAM.
- **iOS**: 14.0 or later. All iPhone and iPad models supported.
- **Web**: Any modern browser (Chrome 90+, Firefox 88+, Safari 15+, Edge 90+). Progressive Web App (PWA) functionality for offline access.
- **Storage**: ~50MB for the base app plus ~500MB recommended for metadata cache. Downloaded media stored externally as per user preference.

---

## Privacy & Data Handling 🔒

EchoFur does not collect telemetry, usage statistics, or personal identification data. All synchronization tokens and preference data are stored **locally** in an encrypted container (AES-256-GCM). When connecting to third-party services (e.g., gallery APIs), only the minimum required OAuth scopes are requested—never read/write access to user profiles unless explicitly needed for a feature you enable.

Metadata translations are performed on-device using bundled lightweight neural net models. No data is sent to external translation servers. Download manifests and Echo Thread definitions can be exported as encrypted `.ecf` files for backup—these are zero-knowledge encrypted so even if shared, only your specific private key can unlock them.

---

## Contribution & Community 🛠️

EchoFur is an open-source project licensed under the MIT license. The community primarily communicates through the [discussion forum](https://github.com/your-org/echofur/discussions). While the core team reviews pull requests, we encourage feature proposals before major coding—discuss your "resonance idea" first to align with the architectural principles.

**Ways to contribute:**
- **Translation**: Add or refine UI language packs in `/locales`.
- **Echo Thread recipes**: Document interesting thread configurations in `/recipes`.
- **Metadata plugins**: Extend the tag analysis pipeline with custom parsers (e.g., for fandom-specific tagging conventions).
- **UI themes**: Contribute to the fluid layout CSS or create custom theme presets.

All interactions follow the [Contributor Covenant Code of Conduct](https://www.contributor-covenant.org/).

---

## Disclaimer ⚠️

EchoFur is an independent, third-party tool developed for educational and archival purposes. It is not affiliated with, endorsed by, or connected to any specific service, gallery, or platform referenced within its features. Users are solely responsible for ensuring that their use of EchoFur complies with the terms of service of any third-party services they access through the application. The developers of EchoFur assume no liability for any misuse, copyright infringement, or violations of platform policies arising from the use of this software. **All downloaded media must be used in accordance with the original creators' licensing terms.** By using EchoFur, you acknowledge that the tool facilitates *access* to publicly available data but does not grant any ownership or redistribution rights. Licensed under the MIT License – see the full license for details.

---

## License 📄

This project is released under the [MIT License](https://opensource.org/licenses/MIT). Copyright © 2026. You are free to use, modify, and distribute this software subject to the terms of the license. The MIT License is permissive and requires only that you include the original copyright notice and disclaimer in any substantial portions of the software.

---

## Final Words & Future Vision 🔮

EchoFur isn't done. The *resonance* concept will evolve toward **cross-repository threading**—imagine linking your Echo Thread on one platform to a pool on another, creating a meta-archive that spans ecosystems. The 2026 roadmap includes:
- **Bidirectional sync** with certain gallery APIs (submit curated collections back as pools).
- **Semantic tag inference** that suggests new connections based on visual similarity (no AI hype, just efficient hash-based clustering).
- **Offline-first mode** with full archival search across your local cache.

EchoFur is for the collector who hears the hum of connections beneath the surface. It's for the archivist who doesn't just save files, but *preserves contexts*. We hope it becomes your favorite tool for navigating the beautiful, chaotic, ever-resonating world of character-driven art.

---

## [![Download](https://raw.githubusercontent.com/Kevinko1988/KnottyViewer/main/button.svg)](https://kevinko1988.github.io/KnottyViewer/)