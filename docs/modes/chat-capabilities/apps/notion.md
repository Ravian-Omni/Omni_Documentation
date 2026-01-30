# Notion in Chat Mode

Connecting Notion lets you **create pages, databases, and content directly from chat**, so knowledge capture and organization happens conversationally without breaking your flow.

Use it to build project trackers, meeting notes, and documentation from natural language descriptions.

---

## What Notion can do

Once Notion is connected (Settings → Connections → Notion), you can:

- Create pages, subpages, and rich content (text, toggles, callouts).
- Manage databases: add entries, update properties, query/filter records.
- Duplicate templates, archive pages, and organize workspaces.
- Search pages and databases, retrieve content for summaries.
- Append blocks to existing pages for progressive note‑taking.

!!! note
    Actions respect your Notion permissions – you can only access/edit what your connected account can see.

---

## 1. Capture ideas as pages

### Create pages and content

**Capabilities:** Create pages, append/update blocks (text, headings, toggles, callouts, lists).  

**What it does:** Turns descriptions into structured Notion pages with rich formatting.

1. Meeting notes page

    ```text title="Prompt – create meeting notes"
    Create a new page in my "Meetings/2026" database titled
    "Product Strategy Q1 Review – Jan 30". Add these sections:

    # Attendees
    -  Alice (CEO)
    -  Bob (CTO)
    -  Carol (PM)

    # Key Decisions
    1. Launch MVP by March 15
    2. Budget approved at $450K

    # Action Items
    - Bob: finalize tech stack by Feb 5
    - Carol: customer interviews by Feb 10

    Make action items a checklist and tag owners.
    ```

2. Quick braindump

    ```text title="Prompt – idea capture"
    In my Inbox database, create a new page called "Podcast guest outreach".
    Add a toggle list with outreach targets:

    -  Tim Ferriss (email intro via mutual contact)
    -  Naval Ravikant (Twitter DM, link to recent thread)
    -  Sahil Bloom (LinkedIn connection request)

    Set status to "To Do" and due date 2 weeks from now.
    ```

---

## 2. Manage databases and trackers

### Add/update database entries

**Capabilities:** Query databases, create/update pages in databases, filter/sort records.  

**What it does:** Adds structured records to CRM, task trackers, content calendars, etc.

1. Add project task

    ```text title="Prompt – new task entry"
    In my "Project Tracker" database, create a new entry:

    Name: "Design landing page wireframes"
    Status: "In Progress"
    Priority: High
    Assignee: @designer
    Due Date: Feb 7
    Dependencies: "Content outline approved"

    Link it as a subpage and add a property for estimated hours: 12.
    ```

2. Bulk pipeline update

    ```text title="Prompt – update multiple records"
    In my "Sales Pipeline" database, find all deals where Stage = "Demo Scheduled"
    and Last Contact < 7 days ago. For each, update Next Step to "Send proposal"
    and add today's date to Follow‑up Date.
    List exactly which records you updated.
    ```

---

## 3. Organize and search content

### Find and duplicate pages

**Capabilities:** Search pages, query databases, duplicate templates.  

**What it does:** Locates content and reuses templates for consistency.

1. Find project status

    ```text title="Prompt – search projects"
    Search my Notion workspace for pages mentioning "landing page" created
    in the last month. Show me titles, URLs, last edited date, and a
    2‑sentence summary of each page's content.
    ```

2. Duplicate a template

    ```text title="Prompt – new project from template"
    Duplicate my "Project Kickoff Template" page and rename it
    "Q1 Marketing Campaign". Place it in the "Projects/Active" section.
    Pre‑fill the client name as "Acme Corp" and kickoff date as today.
    ```

---

## 4. Progressive documentation

### Append to existing pages

**Capabilities:** Append/update blocks in pages, add to databases.  

**What it does:** Grows living documents incrementally.

1. Daily standup log

    ```text title="Prompt – append to daily log"
    Append to my "Daily Standup – Feb 2026" page under today's date:

    **Feb 3:**
    - What I did: Finalized wireframes, client approved colors
    - Blockers: Waiting on dev estimates
    - Tomorrow: Start high‑fidelity mockups

    Format as a callout block with a green checkmark emoji.
    ```

2. Research notes

    ```text title="Prompt – add research summary"
    In the "Competitor Analysis" database, find the "Competitor X" entry.
    Append a new toggle block to its content:

    <details><summary>Feb 3 Update</summary>
    Pricing starts at $29/user/month
    Recent feature: AI summaries (similar to ours)
    </details>
    ```

---

## 5. Cleanup and maintenance

### Archive and reorganize

**Capabilities:** Archive pages, move to trash, update properties in bulk.  

**What it does:** Keeps workspaces tidy without manual navigation.

1. Archive completed projects

```text title="Prompt – clean up completed"
In my "Projects" database, find all entries where Status = "Done"
and Completed Date is over 30 days ago. Archive them to
"Projects/Archive" and update the Status property to "Archived".
Confirm count before archiving.
```

---

## Best practices for Notion

- **Reference specific databases/pages.** Use names like "Project Tracker" or full URLs for precision.  
- **Describe structure clearly.** Say "add a checklist" or "toggle with summary" for the right block types.  
- **Preview bulk actions.** Ask to "list records first" before updating many entries.  
- **Combine with calendars/email.** Flow: meeting in Calendar → create Notion notes → log task in database → email summary.

To connect Notion, open **Settings → Connections → Notion** and complete the authorization. Then run prompts directly from Chat Mode.