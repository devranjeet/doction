---
id: pg-docs-wikilinks
title: Wikilinks & Backlinks System 🔗
icon: 🔗
tags: [wikilinks, backlinks, linking, references, knowledge-graph]
createdAtDaysAgo: 65
updatedAtDaysAgo: 0
---

> 💡 Doction connects your thoughts into a living **Knowledge Web**. With **Wikilinks** and automatic **Bidirectional Backlinks**, no note remains isolated.

---

## 1. What are Wikilinks & Backlinks?

- **Wikilinks (Outgoing Links):** Fast, in-editor links to other documents across any space in your workspace without having to copy or paste URLs.
- **Backlinks (Incoming References):** Automatic two-way relationships. When Page A references Page B, Page B automatically knows about it and displays an incoming link in its **Backlinks & References** panel.

---

## 2. Creating a Page Link

You have two intuitive ways to link another document while writing:

### Method A: The `/link_page` Slash Command
1. In the editor, type `/link_page` (or `/link` or `/page`).
2. Press `Enter` or click **Link to Page** in the menu.
3. The **Link to Page Picker** modal opens.
4. Type keywords to search across all spaces, or use the **Space Filter Dropdown** right inside the search bar to filter by a specific space.
5. Select the target page and press `Enter`.

### Method B: Double Brackets `[[`
1. Anywhere while typing a sentence, type `[[`.
2. The **Link to Page Picker** opens instantly at your cursor.
3. Select your target document and press `Enter`.

---

## 3. Atomic, Resilient Link Badges

Once inserted, the link appears as a clean, rounded pill:

```text
[[ 📄 API Architecture & Endpoints ]]
```

- **Resilient Renaming:** Doction tracks links by unique `pageId`. If you rename the target page tomorrow, the link pill automatically reflects the latest title.
- **Instant Jump:** Clicking the pill navigates directly to the linked document.
- **Cross-Space Support:** You can link pages across different spaces seamlessly.

---

## 4. The Backlinks & References Panel

At the bottom of every page (above the subpages grid), Doction displays an automated **Backlinks & References** section:

- **Incoming Reference Counter:** Shows exactly how many pages reference the current note (`N pages link here`).
- **Contextual Quote Snippets:** Displays the surrounding sentence or block where the reference was made so you know *why* it was linked without opening the source page.
- **Space Badges & Timestamps:** Shows which space the link originated from and when it was last updated.
- **One-Click Navigation:** Click any backlink card to jump straight to the referring document.
