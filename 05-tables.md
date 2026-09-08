---
id: pg-docs-tables
title: Interactive Grid Tables Guide 📊
icon: 📊
parentId: pg-docs-editor
tags: [tables, spreadsheets, data, grid, markdown]
createdAtDaysAgo: 92
updatedAtDaysAgo: 1
---

> 💡 Type `/table` on any empty line to insert a responsive, spreadsheet-style grid table directly into your document. Manage columns and rows on the fly without leaving the keyboard.

---

## 1. Live Interactive Table Example

| Module | Engine | Status | Privacy | Performance |
|---|---|---|---|---|
| **Block Editor** | TipTap v2 | Shipped 🚀 | Local IndexedDB | 0ms keystroke lag |
| **Flowcharts** | Mermaid.js | Shipped 🚀 | Code-as-Doc | Lazy chunk loaded (~650 KB) |
| **Mindmaps** | Markmap D3 | Shipped 🚀 | Zero-Bloat | Instant interactive vectors |
| **Doction Sketch Draw Engine** | Rough.js + Freehand | Shipped 🚀 | Air-Gapped | Pressure-sensitive SVG |
| **3-Level Tree** | Recursive CSS | Shipped 🚀 | Persistent LS | Golden ratio navigation |

---

## 2. Table Editing Controls

- ➕ **Add Columns:** Click the `+` icon on the far right column header.
- ➕ **Add Rows:** Click `+ Row` at the bottom of the table.
- 🗑️ **Delete Columns:** Hover over any column header and click the trash/remove icon.
- 🗑️ **Delete Rows:** Hover over any row index on the left to delete that specific entry.
- 🎨 **Header Row Styling:** The top row is automatically formatted as a distinct, bold semantic header with background contrast.

---

## 3. Keyboard Flow & Rapid Entry

You never need to reach for your mouse while populating data:
- Press `Tab` to advance to the next cell.
- Press `Shift + Tab` to navigate backward to the previous cell.
- When you are in the **last cell of the final row**, simply pressing `Enter` automatically creates a brand-new row and moves your cursor into the first cell.

---

## 4. Markdown Compatibility & Export

All tables in Doction adhere to **GitHub Flavored Markdown (GFM)**:
- When exporting a page to Markdown (`.md`), tables convert into clean `| col1 | col2 |` pipe formatting.
- When importing Markdown files, standard tables are automatically parsed into interactive Doction grid widgets.
