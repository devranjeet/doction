---
id: pg-docs-sidebar
title: Sidebar & Workspace Navigation 🧭
icon: 🧭
tags: [sidebar, navigation, layout, shortcuts, resize]
createdAtDaysAgo: 86
updatedAtDaysAgo: 1
---

> 💡 The Doction sidebar is engineered for speed and ergonomic control: smooth desktop resizing, instant keyboard collapse, sticky navigation anchors, and space context menus.

---

## 1. Desktop Sidebar Resizing (200px — 550px)

Customize the width of your workspace navigation to fit your screen size:
- **Draggable Handle:** Hover over the right border of the sidebar to reveal the resizer handle (`col-resize` cursor).
- **Drag to Resize:** Click and drag left or right to adjust the sidebar width anywhere between **200px** (compact view) and **550px** (wide outline view).
- **Double-Click Reset:** Double-click the resizer border at any time to instantly reset the sidebar to its golden default width of **260px**.
- **Persistent Width:** Your preferred width is automatically saved in `localStorage` (`doction:sidebar_width`), persisting across browser refreshes.

---

## 2. Collapse & Expand Shortcuts (`Ctrl + /` & `Ctrl + \`)

Need maximum screen real estate for writing, whiteboarding, or code architecture?
- **Keyboard Shortcut:** Press `Ctrl + /` or `Ctrl + \` anywhere to toggle the sidebar closed or open.
- **Header Button:** Click the `PanelLeftClose` icon in the sidebar header to collapse it.
- **Unhide Button:** When collapsed, a compact `PanelLeftOpen` button appears seamlessly in the document top bar.
- **Zero Collision Design:** The expand button is integrated directly in-flow before the Back (`←`) and Forward (`→`) buttons, ensuring it never obstructs your navigation controls.

---

## 3. Dual Sticky Header & Footer Architecture

In Doction, you never lose access to primary navigation, search, or settings while scrolling through hundreds of pages:

```
┌───────────────────────────────────────────────┐
│ 🏛️ Doction v1.0              [Collapse Icon] │ <-- Sticky Top (Never scrolls)
│ 🔍 Quick Search (⌘K)                          │
│ 🏠 Home  |  ⚙️ Settings                       │
│ SPACES                                    [+] │
├───────────────────────────────────────────────┤
│ 📁 Documentation                              │
│   ├── 📄 Welcome                              │ <-- Middle Scrollable Area
│   └── 🌳 3-Level Subpages                     │     (Only this section scrolls)
│ 📁 Engineering                                │
├───────────────────────────────────────────────┤
│ 💻 Self-Host Preview (Docker)                 │ <-- Sticky Bottom (Never scrolls)
│ 🌓 Dark / Light Theme Toggle                  │
│ 👤 Current User Profile & Role                │
└───────────────────────────────────────────────┘
```

---

## 4. Space Context Menu (Right-Click)

Right-click on any space row in the sidebar to open the fast context menu:
- 📄 **New Page:** Instantly opens the page creator pre-assigned to that space.
- ⚙️ **Space Settings:** Navigate directly to access controls and permissions.
- 🗑️ **Delete Space:** Secure deletion with confirmation dialog.

---

## 5. History Navigation (`Alt + ←` / `Alt + →`)

Doction maintains a full in-app route history stack:
- Press `Alt + ArrowLeft` to go back to previously visited pages or spaces.
- Press `Alt + ArrowRight` to move forward in history.
- The top bar Back (`←`) and Forward (`→`) buttons highlight dynamically whenever history items are available.

---

## 6. Spotlight Search & Command Palette (`Ctrl + K` / `Cmd + K`)

Press `Ctrl + K` (or `Cmd + K` on macOS) anywhere to open the central spotlight palette:
- **Instant Full-Text Search:** Scans both page titles and complete block body text in real time.
- **Weighted Relevance Scoring:** Title matches receive a 100-point boost, while body matches receive 40 points, ranking the most relevant notes at the top.
- **Keyword Snippet Context:** Automatically extracts matching sentence fragments around your search terms.
- **Recent Pages Index:** When the search bar is empty, it instantly displays your most recently updated documents.
- **Command Actions:** Run workspace actions with one keystroke: *Create New Page*, *Go Home*, *Open Self-Host Guide*, or *Manage Settings*.

---

## 7. Context Drawers (Comments, History, Attachments)

Clicking the header action icons opens smooth sliding right-side drawers:
- 💬 **Comments Drawer (`MessageSquare`):** Anchor comments to the document or to a specific block. Threaded replies and 1-click resolve checkmarks keep discussions organized.
- 🕒 **Version History Drawer (`History`):** Inspect automatic and manual snapshots (`Camera` icon), view diff metrics (`+added`, `−removed`), and roll back with 1-click restore.
- 📎 **Attachments Drawer (`Paperclip`):** Drag and drop images, PDFs, videos, and datasets. Click `+` to insert an uploaded file directly into your note as an interactive block.
