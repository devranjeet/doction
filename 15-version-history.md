---
id: pg-docs-versions
title: Version History & Time-Machine 🕒
icon: 🕒
tags: [versions, history, rollback, checkpoints, git, backup]
createdAtDaysAgo: 70
updatedAtDaysAgo: 0
---

> 💡 Doction features a **Git-Style Version History** and Time-Machine designed around meaningful, deliberate checkpoints rather than noisy single-keystroke auto-saves.

---

## 1. The Philosophy: Meaningful Checkpoints

Unlike word processors that record every single letter typed—cluttering your history with hundreds of micro-edits—Doction approaches versioning like developer tools (Git and Figma):

- **Intentional Checkpoints:** You record a snapshot when you complete a thought, milestone, or section.
- **Clear Commit Messages:** Give your checkpoints clear, memorable titles like `"First Draft Completed"`, `"Added Pricing Matrix"`, or `"Before Major Restructure"`.
- **Zero Clutter:** Your revision timeline remains clean, readable, and easy to navigate even after months of work.

---

## 2. Creating a Version Checkpoint

To save a milestone on any document:

1. Click the **History** icon (`🕒`) in the top navigation bar to open the **Version History Drawer**.
2. Type a short description into the **Save Checkpoint** input (e.g. `Client Review v1`).
3. Click **Save** or press `Enter`.
4. Your checkpoint is immediately saved with:
   - **Author Avatar & Name:** Clearly indicates who committed the change.
   - **Timestamp:** Exact date and relative time (e.g., `10 minutes ago`).
   - **Delta Stats:** Green and red badges showing words added (`+N`) and words removed (`−N`).
   - **Block Count:** Total document blocks at that point in time.

---

## 3. Read-Only Preview Modal

Before rolling back, you can inspect the exact historical state without modifying your active document:

- Click **Preview** on any version card in the timeline drawer.
- A full-screen, read-only preview modal opens showing:
  - The document title and complete content rendered in standard Doction styling.
  - Word count and delta statistics.
  - Historical author and timestamp metadata.
- If it's the version you need, you can restore it directly from the modal. Otherwise, click **Close** to return to your current work unchanged.

---

## 4. Safe 1-Click Rollback & Informative Safety Snapshots

Accidental overwrites are completely eliminated in Doction:

- Whenever you click **Restore** on a previous version (for example, `"Draft 1 Completed"`), Doction **automatically creates a pre-restore safety snapshot** of your current active document first:
  $$\text{Safety Snapshot: } \mathbf{"Before\ restore\ to:\ 'Draft\ 1\ Completed'"}$$
- The selected historical version is then cleanly loaded into the editor.
- If you ever change your mind, you can immediately restore the `"Before restore..."` snapshot to get your work back!

---

## 5. Configurable Background Auto-Snapshots (Optional)

Prefer automatic background checkpoints? You can enable them anytime:

1. Navigate to **Settings → Data & Backup**.
2. Scroll to **Version History & Auto-Snapshots**.
3. Toggle the switch to **Enabled** (Default: **Disabled / Manual-first**).
4. Configure your preferred triggers:
   - **Inactivity Idle Trigger:** Capture a background checkpoint after 5, 10, 15, or 30 minutes of typing inactivity.
   - **Page Switch Trigger:** Capture a snapshot whenever you navigate away to another page.
   - **Max History Retention:** Limit snapshots per page (20, 50, or 100) to keep your local IndexedDB storage light and lightning-fast.
