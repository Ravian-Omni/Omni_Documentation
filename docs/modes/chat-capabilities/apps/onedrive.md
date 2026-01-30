# OneDrive in Chat Mode

Connecting OneDrive lets you **store, sync, share, and collaborate on files across devices directly from chat**, with real-time access, permissions, and enterprise security.

Use it for document management, team sharing, version tracking, and file automation.

---

## What OneDrive can do 

Once OneDrive is connected (Settings → Connections → OneDrive), you can:

- List/search drives, files, folders, children.
- Upload/download/copy/move/delete/share files.
- Manage permissions, shares, versions, activities.
- Check storage, thumbnails, metadata.

---

## 1. File and folder operations 

### Manage content

**Capabilities:** `UPLOAD_DRIVE_ITEM`, `DOWNLOAD_DRIVE_ITEM`, `COPY_DRIVE_ITEM`, `DELETE_DRIVE_ITEM`, `LIST_DRIVE_CHILDREN`.  

**What it does:** CRUD files/folders.

1. Upload project files

    ```text title="Prompt – batch upload"
    Create folder "Q1 Project Files" in root.
    Upload./reports/q1_financials.xlsx,./presentations/deck.pptx.
    List children in new folder, verify upload success.
    ```

2. Download and organize

    ```text title="Prompt – retrieve assets"
    Download "budget_2026.xlsx" to./local/budgets/.
    Copy "team_photos/" to "archive/2026/".
    Delete old "deprecated_models.ipynb".
    ```

---

## 2. Sharing and permissions 

### Collaborate securely

**Capabilities:** `CREATE_SHARING_LINK`, `GET_DRIVE_ITEM_PERMISSIONS`, `INVITE_DRIVE_ITEM`.  

**What it does:** Generates links, grants access.

1. Team share

    ```text title="Prompt – generate shares"
    Create view-only link for "Q1 Report.docx".
    Invite sales@company.com (edit) and client@partner.com (read) to "Project Folder".
    List permissions for "budget.xlsx".
    ```

2. Permission audit

    ```text title="Prompt – access check"
    Get permissions for "shared_proposals/".
    Revoke anyone@external.com, confirm changes.
    ```

---

## 3. Metadata and search 

### Discover content

**Capabilities:** `GET_DRIVE_ITEM`, `LIST_DRIVE_ITEMS`, `SEARCH_DRIVE_ITEMS`, `LIST_DRIVE_RECENT`.  

**What it does:** Finds and inspects files.

1. Search reports

```text title="Prompt – find files"
Search OneDrive: "financial report 2026" last 30 days.
List top 10 results with sizes, modified dates.
Get metadata for #1 item.
```

---

## 4. Versions and history 

### Track changes

**Capabilities:** `LIST_DRIVE_ITEM_VERSIONS`, `LIST_DRIVE_ITEM_ACTIVITIES`, `GET_DRIVE`.  

**What it does:** Restores and audits.

1. Version restore

```text title="Prompt – rollback"
List versions of "contract_v2.docx".
Restore to version from Jan 15, 2026.
Show recent activities on "project_plan.xlsx".
```

---

## 5. Drive management 

### Storage and thumbs

**Capabilities:** `GET_DRIVE`, `LIST_DRIVES`, `GET_DRIVE_ITEM_THUMBNAIL`.  

**What it does:** Oversees storage.

1. Storage overview

```text title="Prompt – drive stats"
List all drives, get quota/used for personal drive.
Generate thumbnail for "hero_image.png" (medium size).
```

---

## Best practices for OneDrive 

- **Folders first.** Organize before bulk ops.  
- **Permissions granular.** View vs edit links.  
- **Async aware.** Copy/upload returns monitor URLs.  
- **Combine apps.** OneDrive → Excel → Teams.

To connect OneDrive, open **Settings → Connections → OneDrive** (OAuth/Microsoft auth). Then run prompts directly from Chat Mode.