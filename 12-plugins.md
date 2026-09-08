---
id: pg-docs-plugins
title: Plugins & Modular Extension Engine 🧩
icon: 🧩
tags: [plugins, extensions, modular, zero-bloat, performance]
createdAtDaysAgo: 85
updatedAtDaysAgo: 1
---

> 💡 Doction is built on a **Zero-Bloat Modular Architecture**. Heavy visual and technical extensions load dynamically on-demand, keeping your baseline bundle razor-sharp and ultra-fast.

---

## 1. Accessing Extension Settings

Navigate to **Settings → Plugins & Extensions** (or click your profile in the sidebar and select *Plugins*):
- **Live Counter:** Shows active extensions (e.g., `11 / 12 Active`).
- **Category Filter Pills:** Quickly filter extensions by *All*, *Diagrams*, *Media & Web*, *Layout & Notes*, *Developer Tools*, or *AI*.
- **Search Palette:** Real-time search across plugin names, descriptions, and slash commands.

---

## 2. The 12 Modular Core Plugins

| Plugin ID | Extension | Category | Slash Command | Dynamic Chunk / Size | Description |
|---|---|---|---|---|---|
| `mermaid` | Mermaid Architecture & Diagrams | Diagrams | `/mermaid` | ~680 KB (Lazy loaded) | System architecture, sequence lifecycles, class models, ER schemas |
| `markmap` | Interactive Mindmaps & Diagrams | Diagrams | `/diagram` | Dynamic Chunk | D3 collapsible concept trees from pure Markdown outlines |
| `drawing` | Doction Sketch Draw Engine | Diagrams | `/drawing`, `/draw`, `/sketch` | ~25 KB (Vector Studio) | Hand-drawn rough vector studio for sketching ideas, shapes, and architecture |
| `webEmbed` | Web Previews & Media Embeds | Media | `/web`, `/embed` | ~14 KB | Live iframes, Loom, Miro, Airtable, YouTube, and Vimeo responsive players |
| `fileAttachment` | Audio, Video & File Attachments | Media | `/attach` | ~18 KB | Studio Vinyl Audio Player (28-bar equalizer, turntable), video player, PDFs, files |
| `toc` | Dynamic Table of Contents | Layout | `/toc` | ~8 KB | Auto-generated heading hierarchy with smooth anchor navigation |
| `fold` | Foldable Collapsible Sections | Layout | `/fold` | ~7 KB | Accordion toggle sections for FAQs and background notes |
| `callout` | Spotlight & Warning Cards | Layout | `/spotlight`, `/imp`, `/callout` | ~9 KB | Tinted accent cards for tips, architectural alerts, and danger notices |
| `table` | Interactive Grid Tables | Developer | `/table` | ~24 KB | Multi-row/column data grids with keyboard navigation and resizing |
| `codeBlock` | Syntax Highlighting & Code Blocks | Developer | `/code` | ~16 KB | Formatted code snippets across 10+ languages with 1-click copy |
| `taskList` | Interactive Task Checklists | Layout | `/todo` | ~9 KB | Clickable checkboxes with nested sub-tasks and strikethrough styling |
| `ai` | Bring Your Own AI (BYO-AI) | AI | `/ai`, `/ask`, `/summarize` | ~20 KB | Multi-provider AI assistant: Google Colab GPUs, local Ollama, Groq, OpenRouter, Gemini |

---

## 3. 1-Click Quick Profiles

Switch your entire workspace setup with a single click in Settings:

- 🚀 **Full Power:** All 12 extensions enabled for complete power and versatility.
- ✍️ **Minimal Writer:** Pure writing focus (core layout plugins enabled: `toc`, `fold`, `callout`, `taskList`) — disables heavy diagramming engines for distraction-free writing.
- 💻 **Developer Mode:** Optimized for technical engineering docs (Code highlighter, Mermaid, Tables, Draw Studio, Web embeds, and AI).

---

## 4. Zero-Bloat Dynamic Code Splitting

Traditional documentation apps force users to download massive diagramming bundles (like Mermaid, D3, MathJax) on initial page load, causing slow startup times and battery drain.

In Doction:
1. When you open a text note, **0 bytes of Mermaid or Markmap JavaScript are downloaded**.
2. When you open a document containing a diagram block, Vite asynchronously downloads the chunk only for that session.
3. If an extension is disabled in Settings, its `/` slash command is automatically omitted from the suggestion palette.

---

## 5. Non-Destructive Suspended State Cards

What happens if an extension is turned off, but you open an existing document that contains one of its blocks?

- **Zero Data Loss:** Your diagram source code and document content remain 100% intact.
- **Suspended State Card:** Doction renders a clean informational card with two options:
  - 📋 **"View Raw Code":** Lets you inspect and copy your diagram source without loading heavy libraries.
  - ⚡ **"Enable Plugin (1-Click)":** Dynamically activates the plugin, downloads the engine chunk, and renders the live visual instantly.
