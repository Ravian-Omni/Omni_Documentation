# Discord in Chat Mode

Connecting Discord lets you **post messages, manage servers/channels/roles, moderate communities, and engage members directly from chat**, powering your Discord presence.

Use it for server announcements, member onboarding, moderation, and events.

---

## What Discord can do

Once Discord is connected (Settings → Connections → Discord), you can:

- Send messages/embeds to channels, DMs, threads.
- Create/manage channels/categories/roles/permissions.
- Moderate: timeout/ban/kick, manage messages.
- Post webhooks, slash commands, interactions.
- Retrieve member lists, server info, message history.

!!! note
    Bot token with required permissions needed for server management.

---

## 1. Community announcements

### Channel messaging

**Capabilities:** Text, embeds, files, polls to channels/threads.  

**What it does:** Communicates with server members.

1. Server update

    ```text title="Prompt – general announcement"
    Post to #announcements in "Pipeline Community" Discord:

    ```
    🚀 Pipeline Dashboard v2.1 Live!

    ✅ New features:
    • Real‑time velocity scoring
    • CRM sync status  
    • Custom widgets

    📊 Beta testers: share feedback in #feedback

    [Join beta](https://beta.pipeline.com)
    ```

    Rich embed with image, green color.
    ```

2. Quick poll

    ```text title="Prompt – member engagement"
    Post to #general:

    "Quick poll: Favorite CRM? 

    🔘 HubSpot
    🔘 Salesforce
    🔘 Pipedrive
    🔘 Other (reply)

    Vote with reactions!"

    Add 4 reaction emojis.
    ```

---

## 2. Server moderation

### Member and content management

**Capabilities:** Timeout/ban/kick, delete messages, manage roles.  

**What it does:** Maintains community health.

1. New member welcome

    ```text title="Prompt – onboarding flow"
    For 10 users who joined "Pipeline Community" last 24h:
    -  DM each: "Welcome! 🚀 Read #rules, introduce yourself in #introductions"
    -  Add role "New Member"
    -  Remove role after 7 days if active

    Post summary in #moderation‑log.
    ```

2. Spam cleanup

    ```text title="Prompt – content moderation"
    In #general channel, delete messages containing obvious spam
    (keywords: "free money", 10+ links, @everyone abuse) from last 24h.
    Timeout offending users 1h, warn in DM.
    Log actions in #mod‑log.
    ```

---

## 3. Server organization

### Channels, roles, categories

**Capabilities:** Create channels/categories, manage roles/permissions.  

**What it does:** Structures communities.

1. Event channels

    ```text title="Prompt – temporary channels"
    Create Discord category "Live Events" under it:
    -  #pipeline‑workshop‑feb5 (text + voice)
    -  #networking‑lounge (voice only)

    Set permissions: @everyone read‑only, @premium full access.
    Auto‑delete channels Feb 7.
    ```

2. Role hierarchy

    ```text title="Prompt – access control"
    Create role "Premium Member" (purple color):
    -  Access to #premium‑content, #vip‑voice
    -  Higher message priority

    Assign to 50 most active members (100+ messages).
    ```

---

## 4. Bot and webhook interactions

### Automation triggers

**Capabilities:** Send slash commands, webhooks, bot messages.  

**What it does:** Integrates Discord with workflows.

1. Status bot command

```text title="Prompt – bot interaction"
In #status channel, run @PipelineBot `/pipeline‑today`

Forward summary to #leadership with highlights.
If pipeline > $2M, notify @execs.
```

---

## 5. Member insights

### Analytics and lists

**Capabilities:** Member lists, message history, server stats.  

**What it does:** Monitors growth and engagement.

1. Community health

```text title="Prompt – engagement report"
Analyze "Pipeline Community" Discord last 7 days:
-  New members, total active
-  Top channels by messages
-  Most active roles/users
-  Voice hours by channel

Growth trends? Churn signals?
```

---

## Best practices for Discord

- **Clear channel topics.** Purpose + rules in topic/pinned.  
- **Roles > @everyone.** Permission tiers reduce noise.  
- **Threads for discussions.** Keeps channels scannable.  
- **Bots for scale.** Status, moderation, engagement automation.

To connect Discord, open **Settings → Connections → Discord** (bot token + server permissions). Then run prompts directly from Chat Mode.