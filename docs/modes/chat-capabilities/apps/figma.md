# Figma in Chat Mode

Connecting Figma lets you **duplicate files, manage teams, organize designs, and collaborate directly from chat**, streamlining design workflows.

Use it for design system maintenance, project handoffs, and team libraries.

---

## What Figma can do

Once Figma is connected (Settings → Connections → Figma), you can:

- Duplicate/rename design files and versions.
- Create/manage teams, projects, folders.
- Share files with permissions/prototypes.
- List files by team/project, search designs.
- Comment on files, manage access.

!!! note
    Personal access token with file/team read/write permissions required.

---

## 1. File duplication and versioning

### Copy and organize designs

**Capabilities:** Duplicate files, create versions, rename.  

**What it does:** Creates working copies and maintains versions.

1. Project kickoff from template

    ```text title="Prompt – duplicate template"
    Duplicate Figma file "Design System v2.0" → "Acme Corp Landing Page v1".
    Move to project "Client Projects/Q1".
    Rename key frames: Home → Acme Home, Features → Acme Features.
    Share prototype link with client (view only).
    ```

2. Variant creation

    ```text title="Prompt – design variants"
    In "Mobile App Screens" file, duplicate "Dashboard" frame 3x:
    -  Dashboard‑Light → Dashboard‑Dark
    -  Dashboard‑Light → Dashboard‑Compact  
    -  Dashboard‑Light → Dashboard‑Premium

    Update color styles in variants.
    ```

---

## 2. Team and project organization

### Structure design libraries

**Capabilities:** Create teams/projects, move/organize files.  

**What it does:** Keeps design systems scalable.

1. New client project

    ```text title="Prompt – project setup"
    Create Figma project "Q1 Client Deliverables" under "Design Team".
    Move files: "Acme Landing v1", "Peak Perf Dashboard", "TechCo Flows".
    Create folder structure:
    -  Acme Corp/
    -  Peak Performance/
    -  TechCo Inc/

    Share project with client PMs (view/comment).
    ```

2. Component library update

    ```text title="Prompt – library publishing"
    In "Design System" team project:
    -  Create new library file "Components Q1‑2026"
    -  Publish updated Button, Card, Modal variants
    -  Notify #design Slack: "New components live!"
    ```

---

## 3. Collaboration and handoff

### Sharing and permissions

**Capabilities:** Generate share/prototype links, set access.  

**What it does:** Enables stakeholder review.

1. Client review process

```text title="Prompt – stakeholder sharing"
For "Acme Landing v1" Figma file:
-  Generate prototype link (starting frame: Home)
-  Permissions: Acme team comment access
-  Add dev handoff notes frame
-  Email link: "Review by Feb 2 → [prototype URL]"

Disable comments after Feb 5.
```

---

## 4. Design system management

### Components and styles

**Capabilities:** List files/teams, search designs.  

**What it does:** Maintains consistency.

1. Unused component audit

```text title="Prompt – design cleanup"
Search all Figma files in "Design System" project for:
-  Components with 0 instances
-  Deprecated color styles (red‑old, blue‑legacy)

List top 10 candidates for removal.
Export report to Google Sheet.
```

---

## 5. Team access control

### Permissions and archiving

**Capabilities:** Manage team members, file access.  

**What it does:** Scales design teams.

1. Contractor access

```text title="Prompt – temporary access"
Add freelance‑designer@contractor.com to "Q1 Client Projects" team:
-  Editor access only to Acme Corp folder
-  View access to Design System
-  Expires: Mar 1 (remove access)

Notify #admin Slack.
```

---

## Best practices for Figma

- **Naming conventions.** "Screen‑State‑Variant" (Home‑LoggedIn‑Dark).  
- **Prototype flows.** Test user journeys before sharing.  
- **Version everything.** Duplicate before major changes.  
- **Combine with Slack.** Flow: Figma prototype → Slack review → Jira tickets.

To connect Figma, open **Settings → Connections → Figma** (personal access token). Then run prompts directly from Chat Mode.