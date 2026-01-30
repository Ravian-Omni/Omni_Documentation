# Google Docs in Chat Mode

Connecting Google Docs lets you **create, edit, and collaborate on documents directly from chat**, turning conversations into formatted content instantly.

Use it for meeting notes, proposals, reports, and collaborative writing.

---

## What Google Docs can do

Once Google Docs is connected (Settings → Connections → Google Docs), you can:

- Create new documents from templates or blank.
- Insert text, headings, lists, tables, images, links.
- Format content: bold/italic, fonts, colors, styles.
- Replace/find text, batch formatting.
- Append content to existing docs.
- Share with permissions, convert to other formats.

---

## 1. Document creation

### New docs and templates

**Capabilities:** Create blank docs, from templates, structured content.  

**What it does:** Generates complete documents from descriptions.

1. Meeting notes template

    ```text title="Prompt – create meeting notes"
    Create Google Doc "Product Strategy Q1 – Jan 30 Meeting Notes"

    Structure:
    # Attendees
    [Table: Name | Role | Company]

    # Agenda
    1. Q1 priorities
    2. Pipeline goals  
    3. Resource needs

    # Key Decisions
    -  Bullet list

    # Action Items
    [Table: Task | Owner | Due | Status]

    Share with product@company.com (edit access).
    ```

2. Proposal generator

    ```text title="Prompt – sales proposal"
    Create "Peak Performance – Operations Proposal" Google Doc.

    Sections:
    # Executive Summary
    # Current Challenges
    # Proposed Solution
    # Pricing & Timeline [Table]
    # Next Steps

    Pre‑fill pricing table, add company logo.
    Share with jordan@peakperformance.co (view).
    ```

---

## 2. Content editing and formatting

### Insert and style text

**Capabilities:** Insert paragraphs, headings, lists, tables, replace text.  

**What it does:** Builds and formats documents precisely.

1. Quarterly report

    ```text title="Prompt – structured report"
    Open/create "Q1 Pipeline Report" Google Doc.

    Insert after "Financial Summary":
    ## Key Metrics Table

    | Metric | Q1 Target | Q1 Actual | % Complete |
    |--------|-----------|-----------|------------|
    | Pipeline | $2.5M | $2.1M | 84% |
    | Deals Closed | 15 | 12 | 80% |

    Format table headers bold blue, add conditional colors.
    ```

2. Meeting minutes append

    ```text title="Prompt – live notes"
    Append to open "Daily Standup Notes" Google Doc:

    **Jan 30 – Engineering**
    - Pipeline API v2.1 deployed ✅
    - CRM sync fix pending review
    - Blockers: @architect approval

    Italic blockers, strikethrough completed items.
    ```

---

## 3. Tables and data

### Structured content

**Capabilities:** Create complex tables, merge cells, formulas.  

**What it does:** Handles reports and trackers.

1. Sales pipeline table

```text title="Prompt – pipeline tracker"
Insert table into "Sales Dashboard" Google Doc:

**Q1 Pipeline**

| Deal Name | Stage | Value | Close Date | Owner | Probability |
|-----------|-------|-------|------------|-------|-------------|
| Peak Perf | Proposal | $24K | Feb 15 | Sarah | 70% |
| TechCo | Demo | $45K | Mar 1 | Jordan | 50% |

Auto‑calculate weighted pipeline column.
```

---

## 4. Collaboration and sharing

### Permissions and export

**Capabilities:** Share docs, set permissions, export formats.  

**What it does:** Manages access and distribution.

1. Client review process

```text title="Prompt – proposal sharing"
For "Peak Performance Proposal" Google Doc:
-  Share with jordan@peakperformance.co (comment access)
-  Add comment: "Jordan – please review pricing/terms"
-  Request comment resolution before sharing final PDF
-  Email link when ready
```

---

## 5. Advanced formatting

### Styles and automation

**Capabilities:** Batch formatting, find/replace, styles.  

**What it does:** Polishes documents efficiently.

1. Brand compliance

```text title="Prompt – style cleanup"
In "Q1 Report" Google Doc:
-  Heading 1: Company Blue (#1E3A8A), 24pt bold
-  Body text: Inter font, 12pt, 1.15 line spacing
-  Tables: alternating row colors
-  Replace "todo" with strikethrough formatting

Apply company header/footer.
```

---

## Best practices for Google Docs

- **Headings for structure.** H1–H3 create automatic TOC.  
- **Tables for data.** Better than lists for comparisons.  
- **Comments for feedback.** @mention collaborators in comments.  
- **Combine with Sheets.** Docs for narrative + Sheets for data → embed charts.

To connect Google Docs, open **Settings → Connections → Google Docs** (Google Workspace OAuth). Then run prompts directly from Chat Mode.