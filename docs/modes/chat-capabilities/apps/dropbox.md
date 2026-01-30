# Dropbox in Chat Mode

Connecting Dropbox lets you **upload, organize, share, and collaborate on files directly from chat**, managing your cloud storage conversationally.

Use it for project folders, client deliverables, backups, and team file sharing.

---

## What Dropbox can do

Once Dropbox is connected (Settings → Connections → Dropbox), you can:

- Upload files/folders from local or URLs.
- Create/share folders with permissions.
- Search files by name/content/location.
- Move/copy/delete/rename files.
- Generate share links (view/edit).
- List folder contents, previews.

---

## 1. File uploading and organization

### Upload and folder structure

**Capabilities:** Upload files/URLs, create folders, organize hierarchy.  

**What it does:** Builds file systems from descriptions.

1. Project folder setup

    ```text title="Prompt – client project"
    Create Dropbox folder "Acme Corp – Q1 Deliverables":

    Inside it:
    -  "Proposal/Proposal v1.2.pdf" [upload local file]
    -  "Workshop Materials/" folder
    - "Slide Deck.pptx" [upload]
    - "Handout.pdf" [from URL]

    Share folder with acme.project@company.com (edit access).
    ```

2. Bulk asset upload

    ```text title="Prompt – media library"
    Upload these to "Marketing/Assets/2026/Q1":
    -  hero‑banner.jpg, product‑demo.mp4, case‑study.pdf
    -  social‑templates.zip [URL download]

    Set folder permissions: team‑marketing view+download.
    Generate public share link expiring in 30 days.
    ```

---

## 2. File search and retrieval

### Locate and preview content

**Capabilities:** Search by name/path/content, list folders.  

**What it does:** Finds files instantly.

1. Asset discovery

    ```text title="Prompt – find creative assets"
    Search Dropbox for files containing "Q1‑campaign" modified since Jan 1:
    -  Show name, path, owner, size, last modified
    -  Preview first 5 results
    -  Download top 3 to local "campaign‑assets"

    Filter: images + PDFs only.
    ```

2. Version recovery

    ```text title="Prompt – file recovery"
    Find versions of "Proposal‑Acme v1.2.pdf" from last 14 days.
    List changes, restore version from Jan 28 (pre‑final edits).
    ```

---

## 3. Sharing and collaboration

### Permissions and links

**Capabilities:** Share links, set permissions, team folders.  

**What it does:** Controls access precisely.

1. Client review link

    ```text title="Prompt – secure sharing"
    For "Acme Corp – Q1 Deliverables" folder:
    -  Generate password‑protected share link (pwd: Q1‑review‑2026)
    -  Edit access: only acme.project@company.com
    -  Expires: Feb 28
    -  Notify via email when accessed

    Revoke after Feb 15.
    ```

2. Team distribution

    ```text title="Prompt – internal sharing"
    Share "Marketing/Assets/2026/Q1" with marketing@company.com group:
    -  Can edit, comment, download
    -  Request access notifications to me
    -  Embed code for Notion page
    ```

---

## 4. File operations

### Move, copy, delete

**Capabilities:** Rename/move/copy/delete files/folders.  

**What it does:** Organizes storage.

1. Archive old projects

    ```text title="Prompt – cleanup"
    Find folders "Project‑2025‑*" with no changes in 12+ months.
    Move to "Archive/2025‑Projects/", delete empty folders.
    Log: what moved, total space saved.
    ```

2. Duplicate template

    ```text title="Prompt – template reuse"
    Copy "Proposal‑Template/" folder → "NewCo‑Proposal‑v1/"
    Rename index.docx → "NewCo Custom Proposal.docx"
    Update placeholders: [Client] → NewCo Inc.
    ```

---

## 5. Advanced organization

### Team folders and previews

**Capabilities:** Paper docs, previews, comments.  

**What it does:** Collaborative workflows.

1. Quick status doc

```text title="Prompt – live tracker"
Create Dropbox Paper doc "Q1 Pipeline Status" in project folder:

# Active Deals
| Deal | Stage | Value | Next Step |
|------|-------|-------|-----------|
| Peak Perf | Proposal | $24K | Send deck |

Share with sales team, @mention blockers.
```

---

## Best practices for Dropbox

- **Descriptive names.** "2026‑Q1‑Acme‑Proposal‑v1.2.pdf" > "doc.pdf".  
- **Folder hierarchies.** Client > Project > Deliverables > Version.  
- **Share links expire.** Set dates/passwords for sensitive files.  
- **Combine with Docs.** Dropbox storage → Google Docs editing → client sharing.

To connect Dropbox, open **Settings → Connections → Dropbox** (OAuth). Then run prompts directly from Chat Mode.