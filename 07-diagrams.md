---
id: pg-docs-diagrams
title: Visual Architecture & Diagramming 🎨
icon: 🎨
tags: [diagrams, visuals, architecture, mermaid, markmap, whiteboard]
createdAtDaysAgo: 90
updatedAtDaysAgo: 1
---

> 💡 Text alone cannot describe modern software architecture. Doction provides three purpose-built visual engines built directly into your documents with zero third-party subscriptions.

---

## The Three Visual Engines Compared

| Dimension | 📐 Mermaid.js (`/mermaid`) | 🧠 Markmap (`/diagram`) | 🎨 Doction Sketch Draw Engine (`/drawing`) |
|---|---|---|---|
| **Input Format** | Code-like DSL (`flowchart TD`, `-->`) | Standard Markdown (`#`, `-`) | Freehand mouse/stylus drawing & vector shapes |
| **Visual Style** | Sharp, precise technical diagrams | Dynamic, organic interactive D3 trees | Warm, hand-drawn rough vector aesthetic |
| **Interactivity** | Static vector layout | Click circles to fold/unfold branches | Full zoom/pan canvas, marquee selection, transform handles |
| **Best Used For** | System architecture, sequence flows, ER schemas | Roadmaps, taxonomies, brainstorming, specs | Back-of-the-napkin sketches, wireframes, flows |
| **Export Options** | SVG markup, SVG file download | SVG export | High-Res PNG download, Vector SVG download, Copy PNG |

---

## 1. When to Use Mermaid.js (`/mermaid`)

Use Mermaid when you need **formal, version-controlled technical documentation**:
- **Sequence Diagrams:** Visualizing API request/response handshakes between frontend, gateway, and database.
- **System Architecture:** Top-to-bottom or left-to-right microservice topology.
- **Git Branch Graphs:** Explaining release branching strategies (`main`, `develop`, `feature/*`).
- **Entity Relationship (ER) Schemas:** Documenting database tables, primary keys, and foreign key relations.

*Explore the subpage guide: [Mermaid Architecture Guide](pg-docs-mermaid)*

---

## 2. When to Use Markmap (`/diagram`)

Use Markmap when you need to **organize complex concepts into digestible hierarchies**:
- **Product Roadmaps:** Breaking down quarterly initiatives into milestones and deliverables.
- **API Taxonomies:** Outlining REST endpoints or GraphQL mutations in a clean tree.
- **Meeting Notes & Brainstorms:** Converting bullet points into an interactive visual graph.

*Explore the subpage guide: [Markmap Mindmaps Guide](pg-docs-markmap)*

---

## 3. When to Use Doction Sketch Draw Engine (`/drawing`)

Use the Doction Sketch Draw Engine when you need **creative freedom without rigid syntax**:
- **Low-Fidelity Wireframes:** Quickly drafting a user interface layout or modal flow.
- **System Sketches:** Drawing custom boxes, cylinders, and arrows with natural sketchy textures.
- **Freehand Calligraphy:** Annotating notes, circling key areas, or sketching mathematical formulas with pressure-sensitive strokes.

*Explore the subpage guide: [Doction Sketch Draw Engine Guide](pg-docs-drawing)*
