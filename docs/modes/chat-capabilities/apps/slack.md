# Slack in Chat Mode

Connecting Slack lets Ravian **post updates, manage channels, and search conversations directly from chat**, so team coordination happens without tabbing between apps.

Use it to broadcast status updates, find info from past threads, schedule reminders, and clean up channels while you focus on the conversation.

---

## What Ravian can do with Slack

Once Slack is connected (Settings → Connections → Slack), Ravian can:

- Post messages, threads, and reactions to channels or DMs.
- Create, rename, archive/unarchive channels, and manage members.
- Search messages, files, and users across your workspace.
- Schedule messages, set reminders, and manage status/DND.
- Upload files, pin important messages, and handle Canvas docs.

!!! note
    Ravian respects your Slack permissions and channel memberships – it can only access what your connected account can see.

---

## 1. Communicate with your team

### Post messages and threads

**Capabilities:** `SLACK_SEND_MESSAGE, SLACK_UPDATES_A_SLACK_MESSAGE, SLACK_SEND_EPHEMERAL_MESSAGE, SLACK_SCHEDULE_MESSAGE`  

**What it does:** Posts to channels, DMs, or private groups, supports rich formatting with blocks/attachments, and schedules future posts.

1. Broadcast a status update

    ```text title="Prompt – team update"
    Post this update to #team-updates and #engineering:

    "🚀 Chat Mode docs are live! New pages cover Gmail, Calendar, Drive,
    GitHub, and more integrations. Check the pinned thread for quick
    start links.

    Docs: https://docs-site.team/chat-integrations"

    Thread the message with a bullet list of what's new.
    ```

2. Schedule a weekly reminder

    ```text title="Prompt – schedule reminder"
    In the #product channel, schedule a message for next Monday at 9AM
    saying:

    "📅 Weekly Product Sync – agenda in thread
    -  Pipeline review
    -  Customer feedback
    -  Next sprint planning

    RSVP in reactions below"

    Reply to your own message with the Zoom link.
    ```

3. Send ephemeral help to a user

    ```text title="Prompt – help one person"
    Send an ephemeral message to @new-dev in #engineering with
    a quick guide to the Chat Mode docs and how to connect their first
    integration. Make it friendly and actionable.
    ```

---

## 2. Search and retrieve information

### Find messages, files, and users

**Capabilities:** `SLACK_SEARCH_MESSAGES, SLACK_SEARCH_ALL, SLACK_FIND_CHANNELS, SLACK_FIND_USERS, SLACK_FIND_USER_BY_EMAIL_ADDRESS, SLACK_FETCH_CONVERSATION_HISTORY`  

**What it does:** Searches across messages/files and lists channels/users/users by criteria.

1. Find a specific discussion

    ```text title="Prompt – search past threads"
    Search all Slack messages for "Chat Mode docs" from the last 30 days.
    Show me the 5 most relevant messages with links, who posted them,
    and a one‑line summary of each conversation.
    ```

2. Quick user lookup

    ```text title="Prompt – find a teammate"
    Find the Slack user with email "pm@company.com" and tell me their
    display name, current status, and which channels we share.
    If they are away, suggest when they might be back based on DND.
    ```

3. Channel discovery

    ```text title="Prompt – find project channels"
    List all active Slack channels whose names contain "docs" or "chat",
    sorted by member count. For each, show purpose, member count,
    and whether I'm already in it.
    ```

---

## 3. Manage channels and conversations

### Create, organize, and moderate channels

**Capabilities:** `SLACK_CREATE_CHANNEL, SLACK_RENAME_A_SLACK_CHANNEL, SLACK_ARCHIVE_A_SLACK_CONVERSATION, SLACK_UNARCHIVE_CHANNEL, SLACK_INVITE_USERS_TO_A_SLACK_CHANNEL, SLACK_JOIN_AN_EXISTING_CONVERSATION, SLACK_LEAVE_A_CONVERSATION`  

**What it does:** Creates channels, invites members, archives inactive ones, and manages access.

1. Create a project channel

    ```text title="Prompt – new project channel"
    Create a private Slack channel called "chat-docs-contributors".
    Invite @docs-team, @new-writer, and myself. Set the topic to
    "Collaboration on Chat Mode documentation" and purpose to
    "Writing, reviewing, and publishing integration guides".
    Pin a welcome message with contributor guidelines.
    ```

2. Clean up inactive channels

    ```text title="Prompt – archive stale channels"
    Find Slack channels I have access to with fewer than 5 members
    and no messages in the last 60 days. List them with last activity
    date, then archive the ones that are clearly inactive (no recent
    pinned messages or stars). Confirm each one before archiving.
    ```

---

## 4. Files, reactions, and reminders

### Share files and engage

**Capabilities:** `SLACK_UPLOAD_OR_CREATE_A_FILE_IN_SLACK, SLACK_ADD_REACTION_TO_AN_ITEM, SLACK_REMOVE_REACTION_FROM_ITEM, SLACK_PINS_AN_ITEM_TO_A_CHANNEL, SLACK_LIST_FILES_WITH_FILTERS_IN_SLACK`  

**What it does:** Uploads files, adds/removes reactions, pins important content, and lists files.

1. Share a doc update

    ```text title="Prompt – upload and share file"
    Upload the latest Chat Mode docs PDF to #team-updates, post it
    with caption "📚 Latest Chat Mode docs – now covers Slack integration
    too! Feedback welcome.", and react with :shipit: once posted.
    Pin the message to the channel.
    ```

2. Clean up reactions

    ```text title="Prompt – reaction cleanup"
    In the #engineering channel, find messages with more than 10
    :confused: reactions and more than 20 :thumbsdown: reactions.
    List the top 3 and suggest whether to update the message or
    start a new thread.
    ```

---

## 5. Personal productivity

### Status, reminders, and presence

**Capabilities:** `SLACK_SET_STATUS, SLACK_CLEAR_STATUS, SLACK_CREATE_A_REMINDER, SLACK_DELETE_A_SLACK_REMINDER, SLACK_SET_DND_DURATION, SLACK_GET_USER_PRESENCE_INFO`  

**What it does:** Manages your status, schedules reminders, and checks team availability.

1. Set working status

    ```text title="Prompt – update status"
    Set my Slack status to "📚 Writing Chat Mode docs" with emoji
    :writing_hand: until end of day. If I'm currently in a meeting,
    schedule this status update for after the meeting ends.
    ```

2. Daily reminders

    ```text title="Prompt – recurring reminders"
    Create these reminders for me:
    -  10AM daily: "Check open PRs in docs repo"
    -  EOD weekdays: "Log today's pipeline wins in #wins"

    List all my active reminders afterward.
    ```

---

## 6. Canvas and advanced features

### Work with Slack Canvas docs

**Capabilities:** `SLACK_CREATE_CANVAS, SLACK_EDIT_CANVAS, SLACK_LIST_CANVASES, SLACK_DELETE_CANVAS`  

**What it does:** Creates, edits, lists, and manages Slack Canvas documents.

```text title="Prompt – create project canvas"
Create a new Slack Canvas in #chat-docs-contributors titled
"Chat Mode Docs Roadmap". Add sections for:
1. Current sprint goals
2. Open blockers
3. Contributor guidelines
Share the canvas link in the channel.
```

---

## Best practices for Slack with Ravian

- **Tag channels and users.** Mention exact channel names (#team-updates) and @mentions for precision.  
- **Thread for context.** Ask Ravian to thread detailed updates under a summary message.  
- **Search before posting.** Use search prompts to reference existing threads instead of duplicating info.  
- **Combine with other tools.** Great flow: summarize a Salesforce deal → post pipeline update to Slack → schedule follow‑up task → create GitHub issue for product feedback.

To connect Slack, open **Settings → Connections → Slack** in the Ravian app and complete the sign‑in flow. After that, you can run any of the prompts above directly from Chat Mode.