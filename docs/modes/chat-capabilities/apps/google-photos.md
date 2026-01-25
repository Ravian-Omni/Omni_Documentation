# Google Photos in Chat Mode

Connecting Google Photos lets Ravian **upload, search, organize, and download media directly from chat**, turning “save these assets to Photos” into executed actions.

Use it for managing demo screenshots, product visuals, and multimedia assets that support your Ravian workflows.

---

## What Ravian can do with Google Photos

Once Google Photos is connected (Settings → Connections → Google Photos), Ravian can:

- Upload images and videos from your device or URLs.
- Create and update albums for different projects.
- Add or move media items into albums.
- Search media items by filters (dates, content, etc.).
- Download media items for use in documents, slides, or reports.

!!! note
    Google Photos works especially well alongside Drive, Docs, and Slides when building reports and presentations from visual assets.

---

## 1. Create and organize albums

### Create and update albums

**Capabilities:** `GOOGLEPHOTOS_CREATE_ALBUM, GOOGLEPHOTOS_UPDATE_ALBUM, GOOGLEPHOTOS_GET_ALBUM, GOOGLEPHOTOS_LIST_ALBUMS`  

**What it does:** Creates new albums, lists existing ones, and updates album titles or cover photos.

1. Create a new album

    ```text title="Prompt – create album"
    Create a new Google Photos album called "Ravian Launch Screenshots"
    for storing all UI captures related to the launch.
    ```

2. Review and rename albums

    ```text title="Prompt – list and update albums"
    List my Google Photos albums whose names contain "Ravian".
    If you find an album named "Ravian Screens", rename it to
    "Ravian UI Screens (2026)".
    ```

---

## 2. Upload and add media

### Upload media

**Capabilities:** `GOOGLEPHOTOS_UPLOAD_MEDIA, GOOGLEPHOTOS_BATCH_CREATE_MEDIA_ITEMS`  

**What it does:** Uploads images and videos (individually or in batch) to Google Photos, optionally adding them directly to an album.

1. Upload a single screenshot

    ```text title="Prompt – upload screenshot"
    Upload the local file `C:\Users\Me\Pictures\ravian_home.png`
    to Google Photos and add it to the album
    "Ravian Launch Screenshots". Use a short description explaining
    that it's the main landing page.
    ```

2. Batch upload from URLs

    ```text title="Prompt – batch upload from URLs"
    Upload these URLs as media items to Google Photos and add them
    to the "Ravian Launch Screenshots" album:

    - https://example.com/ravian-dashboard.png
    - https://example.com/ravian-chatmode.png

    Use descriptive names based on the URL and tag each item with
    a short description of what the screen shows.
    ```

---

### Add media items to albums

**Capabilities:** `GOOGLEPHOTOS_BATCH_ADD_MEDIA_ITEMS, GOOGLEPHOTOS_ADD_ENRICHMENT, GOOGLEPHOTOS_BATCH_GET_MEDIA_ITEMS`  

**What it does:** Adds existing media items to albums and enriches albums with additional context (for example, text or location enrichments).

1. Add existing items into an album

    ```text title="Prompt – add to album"
    Find recent screenshots in my Google Photos that contain the word
    "Ravian" in their description and add them to the
    "Ravian Launch Screenshots" album.
    ```

2. Add an enrichment note

    ```text title="Prompt – add enrichment"
    For the "Ravian Launch Screenshots" album, add a text enrichment
    near the beginning that says:
    "Screenshots captured from the January 2026 launch build."
    ```

---

## 3. Search and browse media

### Search media items

**Capabilities:** `GOOGLEPHOTOS_SEARCH_MEDIA_ITEMS, GOOGLEPHOTOS_LIST_MEDIA_ITEMS`  

**What it does:** Searches for media items in your Google Photos library, with support for filters such as date ranges, content types, and albums.

1. Find assets for a presentation

    ```text title="Prompt – search media"
    Search my Google Photos for media items from the last 30 days
    that are in the "Ravian Launch Screenshots" album.
    Show me thumbnails and a one‑line description for each so I can
    decide which ones to use in a deck.
    ```

2. Filter by date

    ```text title="Prompt – search by date range"
    Find photos in my Google Photos library taken between
    2026‑01‑01 and 2026‑01‑15 that likely contain UI screens
    (laptop or desktop screenshots). Summarize how many you found
    and which albums they belong to.
    ```

!!! note
    Some APIs may only return media created by the app. Ravian will use the richest access available for your account at the time of execution.

---

## 4. Download and reuse media

### Download media items

**Capabilities:** `GOOGLEPHOTOS_GET_MEDIA_ITEM_DOWNLOAD`  

**What it does:** Downloads media items as files so Ravian can embed them into documents, slides, or reports, or save them to local storage.

```text title="Prompt – download for docs"
From the "Ravian Launch Screenshots" album, download the three
most representative screenshots and save them to a local folder
called `Ravian_Launch_Assets`. Then create a short description
list I can paste into a design brief.
```

---

## 5. Update descriptions and metadata

### Update media items

**Capabilities:** `GOOGLEPHOTOS_UPDATE_MEDIA_ITEM`  

**What it does:** Updates descriptions on media items to make them easier to search and organize.

```text title="Prompt – improve descriptions"
For media items in the "Ravian Launch Screenshots" album that
currently have empty or generic descriptions, generate more
descriptive captions based on what the UI shows
(e.g., "Chat Mode overview screen", "Connections settings").
Update the descriptions accordingly.
```

---

## Best practices for Google Photos with Ravian

- **Use clear album names.** Create per‑project albums (for example, “Ravian Launch Screenshots”) so prompts can target them precisely.  
- **Add descriptions early.** Ask Ravian to generate descriptive captions right after upload to improve searchability later.  
- **Combine with Drive and Slides.** Typical flow: capture screenshots → upload to Photos → download selected ones → insert into slide decks or docs via Ravian.

To connect Google Photos, open **Settings → Connections → Google Photos** in the Ravian app and complete the sign‑in flow. After that, you can run any of the prompts above directly from Chat Mode.