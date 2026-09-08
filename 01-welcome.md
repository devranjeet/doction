---
id: pg-docs-overview
title: Welcome to Doction (Document Nation) 🏛️
icon: 🏛️
tags: [welcome, overview, manifesto, guide]
createdAtDaysAgo: 100
updatedAtDaysAgo: 1
---

> 🏛️ **Doction — Document Nation** is your personal digital space where you can create, organize, connect, and manage your documents, notes, ideas, and knowledge.
> 
> ***Your documents. Your ideas. Your space.***

Welcome to your sovereign knowledge space! Doction combines the **visual block editing of Notion**, the **clean structured hierarchy of GitBook**, and the **privacy and data ownership of Obsidian** into a unified, zero-bloat platform.

---

## The Four Pillars of Document Nation

### 1. 🔒 Personal Sovereignty & Air-Gapped Privacy
In traditional cloud tools, you are merely a tenant — your confidential notes, system architecture, and proprietary ideas live on external servers. In **Doction**, you are the ruler of your own document nation:
- **100% Local-First:** Your workspace is persisted securely inside your browser's IndexedDB v2 decoupled engine (`workspace_store` + `assets_store`).
- **Anti-Inspection Security:** Cloud snapshots and vault archives are sealed in non-plaintext containers (`.jdoction` and `.doction`). Notepad or text editors cannot open or inspect your notes.
- **Two-Tier Privacy Model:** Choose between zero-friction *Protocol Sealed (Mode A)* or zero-knowledge *Passphrase E2EE (Mode B)* with 250k PBKDF2 rounds and Master Recovery Keys.
- **Universal Bytecode Deduplication:** Files uploaded across any space or page are deduplicated via binary SHA-256 hashes, saving up to 80% storage with 0 bytes wasted.
- **Sovereign BYOC Cloud Connectors:** Connect your own GitHub repository, S3 bucket (Cloudflare R2, AWS, MinIO), or Google Drive AppData with client-side encryption.
- **Full Data Portability:** Download complete `.doction` encrypted vaults anytime or export individual notes to clean GitHub-Flavored Markdown.

### 2. ✍️ Modern Block-Based Writing Flow
- Type `/` anywhere to open the **Slash Palette** with instant access to headings, callouts, tables, code blocks, and diagrams.
- Standard Markdown shortcuts (`#`, `-`, `1.`, `[]`, `>`, `---`) format your thoughts at the speed of typing.
- Toggle between **Editing Mode** and **Reading Mode** instantly using `Alt + V`.

### 3. 🎨 Zero-Setup Visual Architecture Studio
No need to install third-party plugins or pay for external whiteboarding subscriptions:
- **Mermaid.js (`/mermaid`):** Code-as-documentation for system flowcharts, sequence diagrams, and ER schemas.
- **Markmap (`/diagram`):** Interactive D3 vector mindmaps that collapse and expand with one click.
- **Doction Sketch Draw Engine (`/drawing`):** Full vector sketching canvas with Rough.js hand-drawn styling and pressure-sensitive calligraphy ink.

### 4. 🌳 Disciplined 3-Level Hierarchy Tree
Never lose a thought in an infinite maze of random subfolders:
- **Space → Level 1 (Page) → Level 2 (Subpage) → Level 3 (Sub-subpage)**
- Interactive sidebar tree with geometric connector lines and persistent collapse/expand states.
- Clickable ancestor breadcrumbs showing your exact location at all times.

---

## Documentation Roadmap

Explore the comprehensive user manual across all 17 structured chapters:

| Level | Chapter Document | What You'll Learn |
|---|---|---|
| **Root** | [Welcome to Doction](pg-docs-overview) | Sovereign Document Nation manifesto, four pillars, architecture |
| ↳ L2 | ├── [3-Level Hierarchy & 400+ Emojis](pg-docs-hierarchy) | Strict 3-level depth rules, sidebar tree, breadcrumbs, 400+ emoji icon picker |
| ↳ L3 | │   └── [Keyboard Shortcuts & Hotkeys](pg-docs-shortcuts) | Home-row productivity, Markdown triggers, draw engine hotkeys, comments |
| **Root** | [Editor & Slash Commands](pg-docs-editor) | Slash palette, block drag handles, view/edit mode (`Alt+V`), autosave |
| ↳ L2 | ├── [Interactive Grid Tables](pg-docs-tables) | Spreadsheet data tables, row/column tools, rapid keyboard entry |
| ↳ L2 | └── [Embeds & Studio Vinyl Player](pg-docs-embeds) | Spinning turntable vinyl player, 28-bar equalizer, video, web embeds |
| **Root** | [Visual Architecture Overview](pg-docs-diagrams) | Comparing Mermaid, Markmap, and Doction Sketch Draw Engine |
| ↳ L2 | ├── [Mermaid Architecture Guide](pg-docs-mermaid) | Flowcharts, sequence diagrams, class models, ER schemas |
| ↳ L2 | ├── [Doction Sketch Draw Engine](pg-docs-drawing) | Vector studio, 10 tools, pressure pen, shapes, PNG/SVG exports |
| ↳ L2 | └── [Markmap Mindmaps Guide](pg-docs-markmap) | Interactive D3 collapsible concept trees from Markdown outlines |
| **Root** | [Sidebar & Workspace Navigation](pg-docs-sidebar) | Desktop resizing (200px–550px), `Ctrl+/` collapse, dual sticky headers |
| **Root** | [Plugins & Extension Engine](pg-docs-plugins) | 12 modular plugins, dynamic code-splitting, 1-click profiles |
| **Root** | [Data Ownership, Anti-Inspection & BYOC](pg-docs-backup) | Decoupled IndexedDB v2, SHA-256 deduplication, .jdoction & .doction anti-inspection, BYOC cloud (GitHub/S3/Drive), Two-Tier privacy |
| **Root** | [Version History & Time-Machine](pg-docs-versions) | Git-style checkpoints, delta pills, read-only preview modal, safe rollback |
| **Root** | [Wikilinks & Backlinks System](pg-docs-wikilinks) | Slash `/link_page`, `[[` wikilinks, auto-completing search picker, backlinks panel |
| **Root** | [BYO-AI Integration Engine](pg-docs-byo-ai) | Colab GPU tunnels, local Ollama, cloud API keys, live `/v1/models`, streaming preview |
| **Root** | [Self-Hosting & Docker Deployment](pg-docs-selfhost) | Production deployment runbook, Docker Compose, PostgreSQL & Redis |

---

- [x] Read the Welcome Manifesto
- [ ] Explore the 3-Level Subpages Guide and 400+ Emoji Picker
- [ ] Try creating your first hand-drawn sketch with `/drawing`
- [ ] Test the Studio Vinyl Audio Player with an MP3 file
- [ ] Save a Version Checkpoint in the History drawer
- [ ] Download a full `.doction` backup package from Settings > Data & Backup
