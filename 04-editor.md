---
id: pg-docs-editor
title: Editor & Slash Commands Guide ✍️
icon: ✍️
tags: [editor, slash-commands, shortcuts, formatting, view-mode]
createdAtDaysAgo: 95
updatedAtDaysAgo: 1
---

> 💡 In Doction, every thought is an interactive block. Type `/` on any blank line to access the **Slash Command Palette**, or use Markdown triggers for instant formatting.

---

## 1. Quick View & Edit Modes (`Alt + V`)

Doction features two distinct reading and editing states:
- ✏️ **Editing Mode:** Full interactive editor with drag handles, `/` command menu, and inline formatting controls.
- 👁️ **Reading Mode:** Distraction-free presentation view with locked layout, ideal for reading technical specs, reviewing release notes, or sharing presentations.
- **Keyboard Shortcut:** Press `Alt + V` anywhere on a page to toggle between View and Edit modes with zero mouse clicks.

---

## 2. Cloud Save & Live Indicator

Doction automatically persists every keystroke locally into IndexedDB with zero delay:
- **Saving State:** When typing, a subtle animated spinner (`Saving...`) appears in the top navigation bar.
- **Saved State:** Once idle for 850ms, a green cloud checkmark appears, confirming all changes are safely stored in IndexedDB.
- **Undo / Redo:** Use the top bar buttons or press `Ctrl + Z` (Undo) and `Ctrl + Y` / `Ctrl + Shift + Z` (Redo).

---

## 3. Complete Slash Command (`/`) Reference

Type `/` on a blank line to open the searchable command menu:

### Text & Structure
| Command | Result | Markdown Shortcut |
|---|---|---|
| `/h1` | Large Section Heading | `# Text` |
| `/h2` | Medium Subheading | `## Text` |
| `/h3` | Small Group Heading | `### Text` |
| `/bullet` | Unordered Bullet List | `- Text` or `* Text` |
| `/number` | Ordered Step List | `1. Text` |
| `/todo` | Interactive Checkbox Item | `[] Text` or `[ ] Text` |
| `/quote` | Pull Quote / Callout Blockquote | `> Text` |
| `/callout` | Highlighted Alert Card with Accent | Type `> 💡` |
| `/divider` | Horizontal Visual Separator | `---` |
| `/link_page` | Link to Page (Wikilink Picker) | `[[` |
| `/toc` | Dynamic Auto-Generated Table of Contents | — |
| `/fold` | Collapsible Foldable Section | — |

### Technical & Visual Modules
| Command | Result | Use Case |
|---|---|---|
| `/code` | Syntax-Highlighted Code Editor | TypeScript, Python, SQL, Rust, Go, CSS, HTML, JSON with 1-click copy |
| `/table` | Interactive Grid Table | Custom rows/columns, spreadsheet-style editing, rapid keyboard entry |
| `/drawing` | Doction Sketch Draw Engine | Hand-drawn rough vector studio, 10 tools, pressure pen, SVG/PNG export |
| `/mermaid` | Mermaid.js Diagram Engine | Flowcharts, sequence lifecycles, database schemas, git branching trees |
| `/diagram` | Markmap Mindmap Engine | Dynamic D3 vector concept trees from standard Markdown outlines |
| `/web` or `/embed` | Interactive Web Embed | Loom, Airtable, Miro, YouTube, Vimeo, and iframe embeds |
| `/attach` | Studio Vinyl Audio & Media Block | Studio Vinyl Player (turntable & 28-bar visualizer), video, PDFs, files |

---

## 4. Inline Formatting & Floating Bubble

Select any text inside a block to open the **Floating Formatting Bubble**:
- **Bold (`Ctrl + B`):** `**text**`
- **Italic (`Ctrl + I`):** `*text*`
- **Underline (`Ctrl + U`):** `<u>text</u>`
- **Strikethrough (`Ctrl + Shift + S`):** `~~text~~`
- **Inline Code (`Ctrl + E`):** `` `code` ``
- **Hyperlinks:** Click the link icon or press `Ctrl + K` to attach a web URL.
- **Text Color & Background Highlight:** Choose from 6 soft pastel accents to highlight critical terms.

---

## 5. Block Handles & Drag-and-Drop

Hover over any paragraph to reveal the **6-Dot Drag Handle** on the left margin:
- **Reorder:** Click and drag the handle up or down to reposition blocks effortlessly.
- **Range Selection:** Hold `Shift` while clicking drag handles to select multiple contiguous blocks for bulk copying or deletion.
- **Context Menu:** Right-click any block to change its block type, wrap it with an accent color, copy it as raw Markdown, or add an anchored comment.

---

## 6. Real-Time Document Statistics
At the top of each document, Doction displays real-time metadata:
- **Word Count:** Automatically calculated from plain text, headings, and nested blocks.
- **Estimated Reading Time:** Based on standard 200 words-per-minute reading speed.
- **Last Edited:** Real-time relative timestamp (e.g., *just now*, *5m ago*, *yesterday*) alongside the author's avatar.
