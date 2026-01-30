# Microsoft Teams in Chat Mode

Connecting Teams lets you **post updates, manage channels, schedule meetings, and coordinate teams directly from chat**, streamlining enterprise collaboration.

Use it for channel announcements, 1:1 messaging, meeting scheduling, and file sharing.

---

## What Teams can do

Once Teams is connected (Settings → Connections → Microsoft Teams), you can:

- Post messages to channels, chats, with @mentions, reactions.
- Create/update channels, tabs, welcome messages.
- Schedule Teams meetings with agendas/attendees.
- Share files, create adaptive cards.
- Manage members/permissions in teams/channels.
- Retrieve channel history and mentions.

!!! note
    Enterprise Microsoft 365 account with Teams permissions required.

---

## 1. Channel communication

### Post and engage in channels

**Capabilities:** Send messages, @mentions, reactions, threaded replies.  

**What it does:** Coordinates teams in channels.

1. Project status update

    ```text title="Prompt – channel announcement"
    Post to "#Pipeline‑Project" Teams channel:

    "📊 Pipeline Dashboard v2.1 Deployed! 🚀

    ✅ Live features:
    -  Real‑time deal velocity
    -  Cross‑CRM sync status  
    -  Executive summary widgets

    @devlead @salesops @stakeholders – please test!

    [Demo video link]"

    React with ✅ once posted.
    ```

2. Quick poll

    ```text title="Prompt – team decision"
    Post to "#Product" channel:

    "Quick vote: Next sprint priority?

    👍 Pipeline forecasting
    ❤️ CRM marketplace integrations
    🎯 Mobile dashboard
    💬 Customer portal

    React above! Results Friday."

    ```

---

## 2. 1:1 and group chats

### Direct messaging

**Capabilities:** Send to individuals, ad‑hoc group chats.  

**What it does:** Private coordination.

1. Follow‑up message

```text title="Prompt – direct message"
Send to Jordan Lee (@jordan.lee) in Teams chat:

"Hi Jordan, great demo discussion yesterday!

Next steps:
1. POC environment ready tomorrow
2. Custom pricing by EOD  
3. Kickoff call Thu 2PM?

[Shared proposal.docx]"

```

---

## 3. Meeting scheduling

### Teams meetings and calendar

**Capabilities:** Create instant/scheduled meetings, add attendees.  

**What it does:** Coordinates video collaboration.

1. Client workshop

    ```text title="Prompt – schedule meeting"
    Create Teams meeting "Pipeline POC Kickoff – Peak Performance"
    Thu Feb 5, 2PM PT, 60min.
    Invite: jordan.lee@peakperformance.com, support@company.com
    Agenda: Environment walkthrough + requirements
    Outlook calendar invite + Teams link.
    ```

2. Recurring sync

    ```text title="Prompt – standing meeting"
    Create recurring Teams meeting "Weekly Pipeline Review"
    Mon 10AM PT, 45min, weekly.
    Channel: #Pipeline‑Project
    Auto‑record, required attendees: sales, ops, eng leads.
    ```

---

## 4. File sharing and collaboration

### Documents and assets

**Capabilities:** Upload/share files, OneDrive/SharePoint integration.  

**What it does:** Centralizes resources.

1. Resource package

```text title="Prompt – file sharing"
In "#Sales‑Enablement" channel, upload:
-  Pipeline Playbook v2.pdf
-  Q1 Forecast Template.xlsx
-  Demo Recording.mp4

Post: "📚 Updated sales kit – Q1 ready!
Changes: new forecasting model + objection handling.

Questions? @salesenablement"

Pin conversation.
```

---

## 5. Team and channel management

### Organization and moderation

**Capabilities:** Create channels/teams, manage members/permissions.  

**What it does:** Structures collaboration.

1. New project team

```text title="Prompt – create workspace"
Create Teams team "Q1 Pipeline Initiative".
Channels: General, Planning, Development, Wins.
Members: @sales, @eng, @ops (full member).
Welcome tab: project brief + resources.

Post welcome: "Q1 Pipeline team activated! 🎯"
```

---

## Best practices for Teams

- **Channels > @everyone.** Topic‑specific channels reduce noise.  
- **Threads for discussions.** Keep channel clean, context preserved.  
- **Files in channels.** Better discoverability than chat.  
- **Combine tools.** Flow: HubSpot deal → Teams meeting → SharePoint docs → Slack summary.

To connect Teams, open **Settings → Connections → Microsoft Teams** (Microsoft 365 OAuth). Then run prompts directly from Chat Mode.