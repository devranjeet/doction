---
id: pg-docs-markmap
title: Interactive Mindmaps (Markmap Guide) 🧠
icon: 🧠
parentId: pg-docs-diagrams
tags: [mindmap, markmap, diagrams, guide, visual, tree]
createdAtDaysAgo: 87
updatedAtDaysAgo: 1
---

> 💡 Doction features native, zero-bloat support for **Markmap** — a blazing fast Markdown-to-Mindmap engine that converts text outlines into interactive D3 vector trees with 0ms latency.

Type `/diagram` on any empty line to insert a mindmap block into your document.

```markmap
---
markmap:
  colorFreezeLevel: 2
  initialExpandLevel: 2
---

# 🧠 Markmap Interactive Engine
## ⚡ Performance
- 0ms Local-First render
- Pure Vector SVG
- Zero bloat on-demand loading
## 🎨 Features
- **Bold**, *Italic*, ~~Strike~~
- \`code snippets\`
- [x] Checklists & tasks
- <span style="background:#0f7b5f;color:#fff;padding:1px 5px;border-radius:4px;font-size:11px">CUSTOM BADGE</span>
## 🛠️ Controls
- Click circles to fold/unfold
- Mouse scroll to zoom
- Drag canvas to pan
- 1-Click SVG export
```

---

## 1. Why Markmap in Doction?

Traditional diagramming tools require dragging boxes, aligning arrows, and manual layout adjustments. Markmap eliminates that friction completely:

| Feature | Markmap (`/diagram`) | Mermaid Flowcharts (`/mermaid`) |
|---|---|---|
| **Syntax** | Pure standard Markdown (`#`, `-`) | Custom domain syntax (`flowchart TD`, `-->`) |
| **Interactive Folding** | ✅ Native circle collapse & expand | ❌ Static SVG layout |
| **Bundle Size** | ~30 KB (Super lightweight) | ~650 KB (Heavy library) |
| **Speed** | Instant D3 vector layout | Async layout engine |
| **Best For** | Brainstorming, specs, syllabus, roadmaps | Architecture diagrams, sequence flows |

---

## 2. Basic Markdown Syntax

Markmap constructs tree branches automatically from your Markdown hierarchy.

### A. Using Headings (`#`)
Headings create primary and secondary root branches:

```markdown
# 🚀 Product Launch 2026
## Marketing Strategy
### Social Media
### Newsletter Blast
## Engineering Deliverables
### Performance Polish
### Offline Storage
```

### B. Using Nested Bullet Lists (`-` or `*`)
Nested lists allow deep branching depth without heading size constraints:

```markdown
# ⚡ Tech Stack
- Frontend
  - React 18
  - TypeScript
  - Tailwind CSS v4
- Backend & Storage
  - IndexedDB
  - WebSocket Realtime Sync
```

---

## 3. Frontmatter Configuration (`---`)

At the very top of your mindmap code, you can define a YAML frontmatter block starting and ending with `---` to customize Markmap's behavior:

```yaml
---
markmap:
  colorFreezeLevel: 2
  initialExpandLevel: 2
  maxWidth: 320
---
```

- **`colorFreezeLevel`:** Freezes colors at a specific depth so sub-branches inherit their parent's hue.
- **`initialExpandLevel`:** Sets which depth level should be open by default on document load.
- **`maxWidth`:** Wraps long node text labels automatically.
