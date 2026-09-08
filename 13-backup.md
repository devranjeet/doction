---
id: pg-docs-backup
title: Data Ownership, Anti-Inspection Formats & Sovereign Cloud 💾
icon: 💾
tags: [backup, cloud, byoc, security, storage, jdoction, doction, encryption, indexeddb]
createdAtDaysAgo: 80
updatedAtDaysAgo: 0
---

> 💡 In Doction, you are never locked in and your privacy is never compromised. Your data is stored locally in your browser's IndexedDB v2, exported via tamper-proof anti-inspection containers (`.jdoction` and `.doction`), and backed up to your sovereign cloud providers (Google Drive, GitHub, S3/Cloudflare R2) with client-side zero-knowledge encryption.

---

## 1. The Anti-Inspection Guarantee (`.jdoction` & `.doction`)

Traditional documentation tools export raw, unencrypted JSON files that anyone can open in Windows Notepad, TextEdit, or standard zip extractors to read your confidential thoughts, financial metrics, and company architecture.

In **Doction**, all exports and cloud backups are **anti-inspection protected**:

| Container Format | File Extension | Structure | Security Model | Notepad / External View |
| :--- | :--- | :--- | :--- | :--- |
| **JDoction Stream** | `.jdoction` | Single-file cryptographic container (`application/vnd.doction.stream+json`) | Sealed with AES-GCM-256 binary ciphertext + SHA-256 integrity seal | Scrambled binary ciphertext. **Zero readable text, titles, or JSON.** |
| **Doction Vault** | `.doction` | Multi-file archive bundling `vault.jdoction` + deduplicated `assets/` | ZIP archive with internal `vault.jdoction` stream and SHA-256 hashed binary blobs | Renaming to `.zip` reveals NO plaintext documents or notes. |

---

## 2. Two-Tier Privacy Model (Without Password vs With Password)

Doction gives you complete flexibility over privacy without sacrificing convenience:

### Tier 1: Mode A — Application Protocol Seal (Default / Without Password)
- **Zero Friction:** You don't need to create, remember, or enter a password.
- **Notepad Protection:** Content is sealed using WebCrypto AES-GCM-256 with the Doction application protocol key.
- **External View:** Third parties or unauthorized file viewers see only scrambled binary ciphertext.
- **In Doction:** Restores in 1-click with zero friction and instant integrity verification.

### Tier 2: Mode B — User Passphrase E2EE (Zero-Knowledge Privacy)
- **Custom Master Passphrase:** Switch encryption ON in Backup Settings to require a user-chosen passphrase.
- **Military-Grade Key Derivation:** 250,000 iterations of PBKDF2-SHA256 with a unique 128-bit cryptographic salt prevent brute-force attacks.
- **Emergency Master Recovery Key:** Generate a 128-bit hexadecimal recovery key (`DOC-XXXX-XXXX...`) to ensure you are never locked out of your data if you forget your passphrase.
- **Zero-Knowledge:** Not even Doction can decrypt your data without the password or recovery key.

---

## 3. Sovereign Bring Your Own Cloud (BYOC) Backup Engine

From **Settings → Data & Backup → Cloud Backup (BYOC)**, connect your sovereign cloud directly from the browser with **zero intermediate servers**:

| Cloud Provider | Integration Method | Best For | Storage Ceiling |
| :--- | :--- | :--- | :--- |
| **GitHub** | Direct GitHub Contents API commits with SHA commit history | Developers, versioned repositories, changelogs | 25 MB single-file guardrail |
| **S3-Compatible** | Cloudflare R2, AWS S3, Backblaze B2, MinIO via `aws4fetch` SigV4 | Teams, media-heavy vaults, multi-gigabyte storage | Unlimited |
| **Google Drive** | `drive.appdata` sandboxed hidden folder via OAuth2 Token Client | Personal workspaces, friction-free Google accounts | Google Drive quota |

### Automated Naming & Retention
- Cloud backups are named using ISO timestamps: `doction-backup-YYYY-MM-DDTHH-mm-ss.jdoction` (or `.enc.jdoction` when passphrase protected).
- **Auto-Pruning:** Set a maximum retention count (e.g., keep the 10 most recent versions) to automatically clean up older snapshots and prevent storage bloat.

---

## 4. Decoupled IndexedDB v2 & Universal Asset Store

Doction uses an enterprise-grade **Decoupled Two-Store Database** (`doction_db` v2) that guarantees 0ms typing latency, eliminates RAM bloat, and provides automatic binary deduplication:

### 4.1 `workspace_store` (Lightweight State Engine)
- **Key:** `"current_workspace"`
- Stores spaces, pages, blocks, user settings, and lightweight attachment metadata.
- **Zero Base64 Bloat:** Heavy media files are never embedded into the text JSON. Serializing and saving workspace state takes ~1 millisecond.

### 4.2 `assets_store` (Universal Content-Addressed Media Vault)
- **Primary Key (`keyPath`):** SHA-256 binary bytecode `hash`.
- **Automatic Bytecode Deduplication:** Files are hashed on their raw binary bytes. If you upload the same image or PDF across 5 different pages or spaces—even under different file names—the binary `Blob` is stored **only once** in IndexedDB.
- **Bi-Directional Usage Tracking:** Each stored asset maintains a registry of usages:
  `usages: [{ id, name, pageId, spaceId, at }]`
  Deleting a file from Page 1 removes only that usage reference. The underlying asset remains safe for all other pages using it.
- **Hardware-Accelerated Object URLs:** Served via native browser `blob:http://...` URLs with in-memory session caching. Provides 60fps GPU rendering while consuming 33% less RAM than legacy Base64 data strings.
- **25 MB Safeguard Limit:** Enforces a strict 25 MB per-file safety ceiling to prevent browser memory leaks and ensure 100% compliance with GitHub and S3 upload quotas.

---

## 5. Full Workspace Backups (`.doction` Vaults) & Safe Restores

From **Settings → Data & Backup → Local File (.doction)**:
- **Portable `.doction` Vault:** Bundles `vault.jdoction` (sealed workspace state) and deduplicated raw binary files in `assets/`.
- **Non-Destructive Merge Mode:** Ingests spaces, pages, and attachments alongside existing work, using Section 15 Graph ID Remapping to prevent collisions.
- **Replace Mode:** Performs a 100% clean restore of the entire workspace state.
- **Backward Compatibility:** Seamlessly restores modern `.jdoction`, DOCTN_V2 `.doction` vaults, and legacy v1/v2 JSON archives.

---

## 6. Single-Page Markdown & PDF Exports

Need to share or publish an individual document?
- Click `•••` in the top right corner of any page.
- **Export Markdown (`.md`):** Clean GitHub-Flavored Markdown with YAML frontmatter, tables, and diagram code.
- **Print / PDF (`Ctrl + P`):** Clean printable layout with high-contrast typography.

