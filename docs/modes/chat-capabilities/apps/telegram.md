# Telegram in Chat Mode

Connecting Telegram lets you **send messages, manage groups/channels/bots, and coordinate teams directly from chat**, powering communities and automation.

Use it for group announcements, channel broadcasting, bot interactions, and file sharing.

---

## What Telegram can do

Once Telegram is connected (Settings → Connections → Telegram), you can:

- Send text, images, documents, audio, stickers, polls to chats/groups/channels.
- Manage groups: add/remove members, set permissions.
- Post to channels (broadcasting).
- Create/edit polls, quizzes, inline keyboards.
- Interact with bots via commands.
- Forward messages, pin content.

!!! note
    Bot tokens required for channel/group management. Regular accounts for personal use.

---

## 1. Team and community messaging

### Group and direct messages

**Capabilities:** Send text/media, polls, locations, contacts to chats/groups.  

**What it does:** Coordinates teams and communities.

1. Team standup update

    ```text title="Prompt – group announcement"
    Send to "Engineering Team" Telegram group:

    "🔄 Daily Standup – Jan 30

    ✅ Yesterday:
    -  Deployed pipeline API v2.1
    -  Fixed CRM sync bug

    🔥 Today:
    -  Performance testing
    -  Docs update

    ⚠️ Blockers: @devlead review needed

    Questions? Reply here!"

    Pin the message.
    ```

2. Customer support poll

    ```text title="Prompt – engagement poll"
    Send to "Support Chat" group:

    "Quick poll: What's your biggest CRM pain point?

    A) Lead qualification  
    B) Pipeline visibility
    C) Forecasting accuracy
    D) Reporting

    Vote + comment! 📊"

    Anonymous poll, 24h duration.
    ```

---

## 2. Channel broadcasting

### Mass communication

**Capabilities:** Post to public/private channels, schedule messages.  

**What it does:** Reaches large audiences instantly.

1. Product launch broadcast

    ```text title="Prompt – channel post"
    Post to "@PipelinePros" Telegram channel:

    "🚀 Pipeline Velocity v2.1 Live!

    New features:
    -  Real‑time deal scoring
    -  Cross‑CRM workflow sync  
    -  Mobile pipeline view

    [Demo video.mp4]

    Try free: [linktr.ee/pipelinepros]
    👥 2,847 subscribers"

    Add reaction buttons 👍/🔥/💬
    ```

2. Weekly newsletter

    ```text title="Prompt – scheduled update"
    Schedule post to channel for next Monday 9AM:

    "📊 This Week in Pipeline:

    Top wins:
    -  Customer X: 45% cycle reduction
    -  New integration: HubSpot

    Coming soon:
    -  AI conversation insights

    Questions? @support"

    ```

---

## 3. Bot automation

### Command and inline interactions

**Capabilities:** Send commands to bots, use inline keyboards.  

**What it does:** Triggers workflows and gets instant responses.

1. CRM data pull

    ```text title="Prompt – bot query"
    Send to @CRM‑Bot: "/pipeline today"

    Forward the response summary to "Sales Team" group.
    If deals > $100K, notify @manager.
    ```

2. Task creation

    ```text title="Prompt – create task"
    Message @TaskBot: "/new Pipeline dashboard fix
    Priority: High
    Due: Feb 2
    @designer @devlead"

    Confirm task ID received.
    ```

---

## 4. File and media sharing

### Rich content delivery

**Capabilities:** Send documents, images, audio, locations, contacts.  

**What it does:** Shares resources efficiently.

1. Resource package

```text title="Prompt – share assets"
Send to "New Team Members" group:

"📚 Onboarding Kit:

📖 Pipeline Playbook [playbook.pdf]
🎥 Quickstart Video [tutorial.mp4]  
📋 Task Templates [excel.xlsx]

Questions? @onboarding"

Compress as ZIP if possible.
```

---

## 5. Group and channel management

### Moderation and organization

**Capabilities:** Add/remove members, promote admins, set permissions.  

**What it does:** Maintains community health.

1. Welcome new members

```text title="Prompt – onboarding automation"
For 5 new members in "Sales Team" group:
-  Send welcome message with resources
-  Add to "Sales Resources" channel
-  Restrict messages for 24h (new member mode)

Notify @admin of additions.
```

---

## Best practices for Telegram

- **Channels for broadcast.** 1‑way communication to large audiences.  
- **Groups for discussion.** 30–200 active members max.  
- **Bots for automation.** Handle repetitive tasks/status checks.  
- **Polls for engagement.** Quick feedback > long discussions.

To connect Telegram, open **Settings → Connections → Telegram** (bot token for channels, user session for groups). Then run prompts directly from Chat Mode.