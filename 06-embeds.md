---
id: pg-docs-embeds
title: Interactive Embeds, Audio & Media Attachments 🔗
icon: 🔗
parentId: pg-docs-editor
tags: [embeds, audio, vinyl-player, video, media, attachments, airtable, miro]
createdAtDaysAgo: 91
updatedAtDaysAgo: 1
---

> 💡 Doction features two dedicated media modules: **Web Previews (`/web`, `/embed`)** for live interactive SaaS views, and the **Studio Vinyl Audio & Media Player (`/attach`)** for local audio, video, PDFs, and files.

---

## 1. Studio-Grade Vinyl Audio Player (`/attach`)

When you attach an audio file (`.mp3`, `.wav`, `.ogg`, `.flac`, `.m4a`), Doction renders a custom **Spotify-Grade Studio Vinyl Player**:

```
┌────────────────────────────────────────────────────────────────────────┐
│  [💿 TURNTABLE]   Track: Engineering_AllHands_Q3.mp3                  │
│   (Spinning Disc)  01:24 / 04:32  ·  12.4 MB                           │
│                                                                        │
│   |||||!||||||!||||||!||||||!|||||||   [1.25x ⚡] [🔊 80%] [⬇️] [🗑️]   │
│   (28-Bar Animated Frequency Waves)                                    │
└────────────────────────────────────────────────────────────────────────┘
```

### Key Audio Features
- 💽 **Spinning Vinyl Turntable Animation:** The album record disc (`Disc3`) physically rotates with smooth CSS hardware acceleration when playing and gently rests when paused.
- 🌊 **28-Bar Soundwave Frequency Visualizer:** 28 dynamic frequency spectrum bars pulse and animate rhythmically with playback progress, visually depicting audio energy.
- ⚡ **Speed Multiplier Selector:** Click the `Gauge` speed toggle to cycle through playback rates: `0.75x`, `1x`, `1.25x`, `1.5x`, and `2x` — perfect for reviewing recorded team meetings, podcasts, and audio notes.
- ⏱️ **Real-Time Duration Scrubbing:** Clean digital readout (`formatDuration`) showing elapsed time and total duration.
- 🔊 **Volume Control & Mute:** Smooth volume level slider with 1-click mute toggle (`Volume2` / `VolumeX`).
- 🔒 **100% Offline & Local Storage:** Audio tracks are stored directly in your browser's IndexedDB as high-capacity Blobs or Data URLs. They play instantly with 0ms latency without uploading to external servers.

---

## 2. Cinema Video Player (`/attach`)

When you upload video media (`.mp4`, `.webm`, `.mov`, `.mkv`):
- **16:9 Responsive Viewport:** Automatically fits document margins while preserving native aspect ratios.
- **Cinema Controls:** Fullscreen toggle, Picture-in-Picture (PiP), volume adjustments, and timeline scrubbing.
- **Local Persistence:** Plays completely offline without buffering from third-party hosting platforms.

---

## 3. PDF, Files & Universal Media Vault (`/attach`)

- **Interactive PDF Viewer:** Embedded PDF reader with page navigation and zoom controls directly inline.
- **File Type Badges:** Color-coded status icons for spreadsheets (`.csv`, `.xlsx`), archives (`.zip`, `.tar.gz`), source code (`.ts`, `.py`, `.json`), audio, video, and raw documents.
- **Strict 25 MB Safeguard:** Every upload is validated client-side to enforce a strict 25 MB safety ceiling, eliminating browser memory crashes and keeping backups within cloud quotas.
- **Universal SHA-256 Bytecode Deduplication:** Files are hashed on their raw binary bytes. If the same file is uploaded across multiple pages or spaces—under the same or different names—Doction stores the binary `Blob` **only once** in IndexedDB (`assets_store`).
- **Workspace Media Library:** Open the Attachments drawer and toggle to **Workspace Media** to view all deduplicated files across all spaces. Click **`+ Attach to this Page`** to link any existing media to your document with **zero duplicate storage bytes**.
- **Hardware-Accelerated Object URLs:** Media is rendered via native `blob:http://...` URLs with in-memory session caching, delivering 60fps GPU-accelerated previews while using 33% less RAM than Base64.
- **1-Click Download & Management:** Instant file download button and non-destructive removal controls (removing a file from Page 1 preserves it for all other pages using it).

---

## 4. Interactive Live Web Embeds (`/web` or `/embed`)

Type `/web` or `/embed` to embed live interactive SaaS dashboards and video services:

| Provider | Supported Formats | What It Renders |
|---|---|---|
| **Loom** | `loom.com/share/*` | Interactive walkthrough video with playback controls |
| **Airtable** | `airtable.com/shr*` | Live interactive database grid, Kanban, or form |
| **Miro** | `miro.com/app/board/*` | Zoomable collaborative infinite whiteboard canvas |
| **YouTube** | `youtube.com/watch?v=*`, `youtu.be/*` | Full YouTube video player with responsive scaling |
| **Vimeo** | `vimeo.com/*` | Clean Vimeo cinema viewport |
| **Generic Web** | Any public `https://` URL | Interactive responsive iframe with sandbox security |

---

## 5. Privacy & Offline Resilience

- **Lazy Initialization:** External iframes only initialize and connect when scrolled into the active viewport, conserving memory and network bandwidth.
- **Air-Gapped Offline Protection:** When working offline, third-party embeds gracefully display a clean offline placeholder card with the destination URL and a *Connect to internet to preview* badge, keeping your document fast and crash-free.
