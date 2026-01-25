# Google Drive in Chat Mode

Connecting Google Drive lets Ravian **create, find, move, share, and download files directly from chat**, turning “put this in Drive and share it” into executed actions.

Use it for storing artifacts from workflows, organizing project folders, and wiring Drive into your research, reporting, and collaboration flows.

---

## What Ravian can do with Google Drive

Once Google Drive is connected (Settings → Connections → Google Drive), Ravian can:

- Create files and folders, and organize them into project structures.
- Upload, download, move, and delete files.
- Search Drive with rich filters (type, date, folder, permissions).
- Manage sharing and permissions on files and folders.
- Work with comments, revisions, and shared drives.

!!! note
    Google Drive works especially well when combined with Docs, Sheets, Slides, Gmail, and Notion as part of a full Ravian workflow.

---

## 1. Create and organize files & folders

### Create files and folders

**Capabilities:** `GOOGLEDRIVE_CREATE_FILE, GOOGLEDRIVE_CREATE_FILE_FROM_TEXT, GOOGLEDRIVE_CREATE_FOLDER, GOOGLEDRIVE_CREATE_SHORTCUT_TO_FILE, GOOGLEDRIVE_CREATE_DRIVE`  

**What it does:** Creates new files, folders, shortcuts, and shared drives, optionally from provided text content.

1. Create a folder structure

    ```text title="Prompt – create project folders"
    In my Google Drive, create a folder called "Ravian Docs".
    Inside it, create subfolders "Specs", "Screenshots", and "Releases".
    ```

2. Create a file from text

    ```text title="Prompt – create file from text"
    In the "Ravian Docs/Specs" folder, create a Google Docs file called
    "Documentation Plan" using the outline we discussed in this chat.
    ```

3. Create a shortcut

    ```text title="Prompt – create shortcut"
    Create a shortcut to the "Ravian Job Tracker" Google Sheet inside the
    "Ravian Docs" folder so I can find it quickly.
    ```

---

## 2. Upload, download, and edit content

### Upload files

**Capabilities:** `GOOGLEDRIVE_UPLOAD_FILE, GOOGLEDRIVE_UPLOAD_FROM_URL, GOOGLEDRIVE_RESUMABLE_UPLOAD`  

**What it does:** Uploads local files or remote files (via URL) into Drive, supporting large files via resumable uploads.

1. Upload a local file

    ```text title="Prompt – upload local file"
    Upload my local file `C:\Users\Me\Desktop\ravian_overview.pdf`
    to Google Drive under the "Ravian Docs/Releases" folder.
    ```

2. Upload from URL

    ```text title="Prompt – upload from URL"
    Fetch the file from this URL:
    https://example.com/ravian-whitepaper.pdf
    and upload it into my "Ravian Docs/Specs" folder in Google Drive.
    Name it "ravian_whitepaper.pdf".
    ```

### Download files

**Capabilities:** `GOOGLEDRIVE_DOWNLOAD_FILE, GOOGLEDRIVE_DOWNLOAD_FILE_OPERATION`  

**What it does:** Downloads or exports Drive files (Docs, Sheets, Slides) into the requested format.

```text title="Prompt – download as PDF"
Find the Google Docs file named "Ravian AI Product Brief"
in my Drive and download it as a PDF to my local Documents folder.
```

---

## 3. Search and navigate Drive

### Find files and folders

**Capabilities:** `GOOGLEDRIVE_FIND_FILE, GOOGLEDRIVE_FIND_FOLDER, GOOGLEDRIVE_LIST_FILES, GOOGLEDRIVE_LIST_REVISIONS, GOOGLEDRIVE_GET_FILE_METADATA`  

**What it does:** Searches Drive across My Drive and shared drives using names, MIME types, dates, folders, and more, and inspects file metadata and revisions.

1. Find a specific file

    ```text title="Prompt – find a file"
    Find the most recent PDF in my Google Drive whose name contains
    "Ravian docs" and show me its location, owner, and last modified time.
    ```

2. Browse project files

    ```text title="Prompt – list project files"
    List all files in the "Ravian Docs/Releases" folder, grouped by type
    (PDF, Doc, Sheet, Slide), and sort them by last modified date.
    Highlight anything updated in the last 7 days.
    ```

3. Inspect revisions

    ```text title="Prompt – view revisions"
    For the file "Ravian AI Product Brief", list its last 5 revisions with
    timestamps and authors, and tell me whether the size changed
    significantly between versions.
    ```

---

## 4. Move, trash, and delete

### Move and reorganize

**Capabilities:** `GOOGLEDRIVE_MOVE_FILE`  

**What it does:** Moves files between folders (parents), letting you reorganize Drive from chat.

```text title="Prompt – move file"
Move the file "ravian_whitepaper.pdf" from the root of my Drive
into the "Ravian Docs/Specs" folder. If the folder doesn't exist,
create it first.
```

### Trash and delete

**Capabilities:** `GOOGLEDRIVE_TRASH_FILE, GOOGLEDRIVE_UNTRASH_FILE, GOOGLEDRIVE_GOOGLE_DRIVE_DELETE_FOLDER_OR_FILE_ACTION, GOOGLEDRIVE_EMPTY_TRASH`  

**What it does:** Soft‑deletes files (moves to trash), restores them, permanently deletes specific items, or empties the trash.

1. Safe delete (trash)

    ```text title="Prompt – move to trash"
    Move the file named "Ravian Draft Notes (old)" to the trash.
    Show me the file details before you act and ask for confirmation.
    ```

2. Restore from trash

    ```text title="Prompt – restore file"
    Find the file "Ravian Draft Notes (old)" in the trash
    and restore it back to its original location.
    ```

3. Hard delete / empty trash

    ```text title="Prompt – empty trash (careful)"
    Show me how many items are currently in my Google Drive trash
    and their total size. After I confirm, empty the trash completely.
    ```

!!! warning
    Permanent deletion cannot be undone. Always confirm before running destructive actions.

---

## 5. Sharing, permissions, and labels

### Manage sharing and access

**Capabilities:** `GOOGLEDRIVE_ADD_FILE_SHARING_PREFERENCE, GOOGLEDRIVE_LIST_PERMISSIONS, GOOGLEDRIVE_DELETE_PERMISSION, GOOGLEDRIVE_UPDATE_PERMISSION`  

**What it does:** Grants, lists, updates, and revokes access for users, groups, domains, or “anyone with the link”.

1. Share a file with a teammate

    ```text title="Prompt – share with view access"
    For the file "Ravian AI Product Brief", give view-only access
    to pm@example.com. Do not change existing permissions.
    After updating, show me the complete permission list.
    ```

2. Make a link shareable

    ```text title="Prompt – shareable link"
    For the folder "Ravian Docs/Releases", ensure that anyone with the link
    can view files inside it. Then generate a shareable link and paste it here.
    ```

3. Clean up access

    ```text title="Prompt – clean permissions"
    List all non‑owner users who currently have edit access to
    the "Ravian Docs" folder. Suggest which ones might no longer
    need access, then remove only the ones I explicitly approve.
    ```

### Labels and approvals

**Capabilities:** `GOOGLEDRIVE_FILES_MODIFY_LABELS, GOOGLEDRIVE_LIST_FILE_LABELS, GOOGLEDRIVE_LIST_APPROVALS, GOOGLEDRIVE_LIST_ACCESS_PROPOSALS`  

**What it does:** Manages labels on files and inspects approvals / access proposals for governance workflows.

```text title="Prompt – apply labels"
On the file "Ravian AI Product Brief", add labels to mark it as
"Confidential" and "Docs v1". Show me all existing labels afterward.
```

---

## 6. Comments, replies, and collaboration

### Work with comments

**Capabilities:** `GOOGLEDRIVE_CREATE_COMMENT, GOOGLEDRIVE_LIST_COMMENTS, GOOGLEDRIVE_UPDATE_COMMENT, GOOGLEDRIVE_DELETE_COMMENT, GOOGLEDRIVE_CREATE_REPLY, GOOGLEDRIVE_GET_COMMENT, GOOGLEDRIVE_LIST_REPLIES_TO_COMMENT, GOOGLEDRIVE_UPDATE_REPLY, GOOGLEDRIVE_DELETE_REPLY`  

**What it does:** Creates, lists, updates, and deletes comments and replies on Drive files.

1. Add a comment

    ```text title="Prompt – add comment"
    On the "Ravian AI Product Brief" file, add a comment saying:
    "Please verify the section on Chat vs Task mode aligns with the latest UI."
    Tag kingsuk@example.com if possible.
    ```

2. Summarize comment threads

    ```text title="Prompt – summarize comments"
    For the same file, summarize all comments and replies into a list
    of open issues and resolved items so I can see what’s left to do.
    ```

---

## 7. Shared drives and monitoring (advanced)

### Shared drives

**Capabilities:** `GOOGLEDRIVE_CREATE_DRIVE, GOOGLEDRIVE_GET_DRIVE, GOOGLEDRIVE_UPDATE_DRIVE, GOOGLEDRIVE_DELETE_DRIVE, GOOGLEDRIVE_HIDE_DRIVE, GOOGLEDRIVE_UNHIDE_DRIVE`  

**What it does:** Creates and manages shared drives, including visibility and metadata.

```text title="Prompt – set up shared drive"
Create a shared drive called "Ravian Team Shared" for collaborative docs.
Make sure it is visible in my Drive and summarize the default settings
(owner, sharing, storage).
```

### Watch changes

**Capabilities:** `GOOGLEDRIVE_WATCH_CHANGES, GOOGLEDRIVE_WATCH_FILE, GOOGLEDRIVE_STOP_WATCH_CHANNEL, GOOGLEDRIVE_LIST_CHANGES, GOOGLEDRIVE_GET_CHANGES_START_PAGE_TOKEN`  

**What it does:** Subscribes to and inspects changes in Drive or on specific files (for advanced automation).

```text title="Prompt – monitor a folder (conceptual)"
Monitor changes in the "Ravian Docs" folder and keep a running log
of new or updated files in a Google Sheet called "Ravian_Drive_Audit".
Include who changed what and when.
```

---

## Best practices for Google Drive with Ravian

- **Organize by project.** Ask Ravian to create and maintain a clear folder structure per project.  
- **Start with read‑only actions.** Use search, listing, and metadata prompts before you let Ravian move or delete files.  
- **Be explicit about locations.** Mention folder paths or parent folder names to avoid touching the wrong files.  
- **Combine with other tools.** For example: research → Docs/Sheets in Drive → share via Gmail → link in Calendar invites.

To connect Google Drive, open **Settings → Connections → Google Drive** in the Ravian app and complete the sign‑in flow. After that, you can run any of the prompts above directly from Chat Mode.
