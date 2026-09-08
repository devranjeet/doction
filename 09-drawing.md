---
id: pg-docs-drawing
title: Doction Sketch Draw Engine Guide 🎨
icon: 🎨
parentId: pg-docs-diagrams
tags: [drawing, sketch, whiteboard, canvas, roughjs, vector, doction-sketch]
createdAtDaysAgo: 88
updatedAtDaysAgo: 1
---

> 💡 Doction features a first-class native vector drawing engine — the **Doction Sketch Draw Engine** — embedded directly inside your documents. Type `/drawing`, `/draw`, or `/sketch` on any blank line to insert an illustration block. In reading mode, it renders cleanly as a crisp graphic; click it to enter the full-screen creative studio!

---

## 1. Interactive Drawing Example

```drawing
{
  "caption": "Doction Sovereign Architecture",
  "elements": [
    {
      "id": "el_1",
      "type": "rectangle",
      "x": 40,
      "y": 40,
      "width": 160,
      "height": 90,
      "strokeColor": "#35c495",
      "backgroundColor": "rgba(53, 196, 149, 0.22)",
      "fillStyle": "hachure",
      "strokeWidth": 2.5,
      "strokeStyle": "solid",
      "roughness": 1.2,
      "opacity": 1,
      "seed": 42
    },
    {
      "id": "el_2",
      "type": "arrow",
      "x": 200,
      "y": 85,
      "width": 100,
      "height": 0,
      "strokeColor": "auto",
      "backgroundColor": "transparent",
      "fillStyle": "none",
      "strokeWidth": 2.5,
      "strokeStyle": "solid",
      "roughness": 1.2,
      "opacity": 1,
      "seed": 43
    },
    {
      "id": "el_3",
      "type": "diamond",
      "x": 300,
      "y": 35,
      "width": 140,
      "height": 100,
      "strokeColor": "#38bdf8",
      "backgroundColor": "rgba(56, 189, 248, 0.22)",
      "fillStyle": "hachure",
      "strokeWidth": 2.5,
      "strokeStyle": "solid",
      "roughness": 1.2,
      "opacity": 1,
      "seed": 44
    },
    {
      "id": "el_4",
      "type": "text",
      "x": 70,
      "y": 70,
      "width": 100,
      "height": 30,
      "strokeColor": "#ffffff",
      "backgroundColor": "transparent",
      "fillStyle": "none",
      "strokeWidth": 2,
      "strokeStyle": "solid",
      "roughness": 0,
      "opacity": 1,
      "seed": 1,
      "text": "Client App",
      "fontSize": 20,
      "fontFamily": "handwriting"
    },
    {
      "id": "el_5",
      "type": "text",
      "x": 335,
      "y": 70,
      "width": 100,
      "height": 30,
      "strokeColor": "#ffffff",
      "backgroundColor": "transparent",
      "fillStyle": "none",
      "strokeWidth": 2,
      "strokeStyle": "solid",
      "roughness": 0,
      "opacity": 1,
      "seed": 1,
      "text": "Local Vault",
      "fontSize": 20,
      "fontFamily": "handwriting"
    }
  ]
}
```

---

## 2. Creative Studio 10-Tool Arsenal

When the studio modal opens, the top toolbar provides a complete drawing arsenal accessible via both letter and number hotkeys:

| Tool | Letter Hotkey | Number Hotkey | Description |
|---|---|---|---|
| **Hand (Pan)** | `H` | `1` | Drag and navigate across the infinite drawing canvas |
| **Select & Transform** | `V` | `2` | Select, move, multi-drag, and resize shapes |
| **Rectangle** | `R` | `3` | Sketch system boxes, containers, and interface frames |
| **Diamond** | `D` | `4` | Decision trees, gateways, and flow branching nodes |
| **Ellipse / Circle** | `O` | `5` | Draw actors, start/end states, databases, and hubs |
| **Arrow** | `A` | `6` | Directed flow arrows with automatic arrowhead rendering |
| **Line** | `L` | `7` | Straight connectors, dividers, and custom vectors |
| **Freehand Pen** | `P` | `8` | Pressure-sensitive calligraphy drawing with smooth tapering |
| **Text** | `T` | `9` | Hand-drawn aesthetic text with automatic wrapping |
| **Eraser** | `E` | `0` | 1-Click deletion of unwanted elements |

---

## 3. Two-Way Live Style Panel

Selecting any shape opens the **Style Properties Panel** on the left with live real-time preview:
- **Stroke Color:** Choose from curated architectural shades (Slate, Mint Green, Sky Blue, Warm Amber, Coral Red, Violet, Rose Pink) or select **Theme Auto** (dynamically adapts stroke color to light or dark mode ink).
- **Background Fill Color:** Transparent or soft translucent pastels (Mint Tint, Blue Tint, Amber Tint, Red Tint, Violet Tint).
- **Fill Style:**
  - `none`: Clean wireframe outline.
  - `hachure`: Authentic sketchy diagonal hatch lines.
  - `cross-hatch`: Crossed technical drafting grid shading.
  - `solid`: Full opaque color fill.
- **Stroke Width:** Thin (1.5px), Medium (2.5px), or Bold (4px).
- **Roughness:**
  - `0.2`: Architectural drafting precision with clean edges.
  - `1.2`: Classic hand-drawn sketch aesthetic (default).
  - `2.2`: Expressive artistic doodle.

---

## 4. Power Productivity Gestures

- **Marquee Selection:** Click and drag on empty canvas to draw a dashed selection box around multiple elements.
- **Multi-Select Drag:** Dragging any element in a selection translates all chosen shapes simultaneously.
- **Arrow-Key Micro-Nudge:** Press the `Arrow Keys` to nudge selected shapes by **1 pixel** (or hold `Shift` for **10-pixel jumps**). An automatic 350ms debouncer prevents flooding your undo history!
- **Quick Duplicate (`Ctrl + D`):** Instantly clones selected elements with a +20px offset and selects the new copy.
- **Layer Z-Ordering:**
  - `]` : Bring Forward
  - `[` : Send Backward
  - `Ctrl + ]` : Bring to Front
  - `Ctrl + [` : Send to Back
- **In-Place Text Editing:** Double-click any text label on canvas to edit its words directly with an auto-resizing input overlay.
- **Focal-Point Zoom & Pan:**
  - Hold `Ctrl` while scrolling the mouse wheel (or pinch on a trackpad) to zoom smoothly into the exact cursor position.
  - Two-finger drag or holding `Spacebar` while dragging pans the infinite canvas anytime.
- **Safe Multi-Stage Escape:**
  1. *First Escape:* Cancels active drawing, resizing, or marquee box.
  2. *Second Escape:* Clears the active element selection.
  3. *Third Escape:* Closes the studio only when completely idle.
- **Save Shortcut (`Ctrl + Enter`):** Saves the drawing and embeds the updated vector directly into your document.

---

## 5. Vector & Raster Export Options

At the top right of the studio, click the export dropdown:
- 📋 **Copy PNG to Clipboard:** Instantly paste your diagram into Slack, Discord, or messages.
- 💾 **Download High-Res PNG:** High-resolution transparent raster graphic.
- 📐 **Download Scalable Vector SVG:** Clean, resolution-independent SVG file ready for Figma, pitch decks, and presentations.
- 💾 **Embedded JSON Persistence:** Drawings are saved inside the document as lightweight JSON definitions, meaning zero compression artifacts and infinite lossless re-editing!
