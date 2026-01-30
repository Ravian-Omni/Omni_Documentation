# Webex in Chat Mode

Connecting Webex lets you **create rooms/teams, send messages, manage memberships/webhooks, and handle people directly from chat**, powering Cisco's video conferencing and collaboration.

Use it for team channels, meeting rooms, messaging automation, and event notifications.

---

## What Webex can do 

Once Webex is connected (Settings → Connections → Webex), you can:

- Create/update/delete rooms, teams, messages, memberships.
- List rooms/teams/messages/memberships/people/webhooks.
- Get details for rooms/teams/messages/memberships/people/webhooks.
- Manage webhooks for events.

---

## 1. Rooms and spaces 

### Meeting and chat rooms

**Capabilities:** `Create Room`, `List Rooms`, `Get Room Details`, `Update Room`, `Delete Room`.  

**What it does:** Manages collaboration spaces.

1. Project room

    ```text title="Prompt – team space"
    Create room "Q1 Product Launch" (group), invite product@company.com.
    List my rooms, get details for "Q1 Product Launch".
    Update title "Q1 Launch - Sprint 1".
    ```

2. Cleanup

    ```text title="Prompt – archive room"
    Delete old room ID Y2K9x123.
    ```

---

## 2. Teams and memberships 

### Group collaboration

**Capabilities:** `Create Team`, `List Teams`, `Get Team Details`, `Update Team`, `Create Team Membership`, `List Team Memberships`, `Update/Delete Membership`.  

**What it does:** Builds teams.

1. New team

```text title="Prompt – dept team"
Create team "Engineering", description "Dev workflow".
Add members: dev1@company.com (member), manager@company.com (moderator).
List team memberships, update dev1 role to moderator.
```

---

## 3. Messaging 

### Send and manage messages

**Capabilities:** `Create Message`, `List Messages`, `Get Message Details`, `Delete Message`.  

**What it does:** Chat automation.

1. Announcement

```text title="Prompt – broadcast"
Create message in room "Q1 Product Launch": "Sprint kickoff Mon 10AM".
Markdown: **Bold** agenda.
List recent messages, delete my test msg ID M8z789.
```

---

## 4. People and users 

### User management

**Capabilities:** `List People`, `Get Person Details`.  

**What it does:** Finds participants.

1. Team roster

```text title="Prompt – member search"
List people emails: @engineering.company.com.
Get details for devlead@company.com.
```

---

## 5. Webhooks and events 

### Notifications

**Capabilities:** `List Webhooks`, `Create Webhook`, `Get Webhook Details`, `Delete Webhook`.  

**What it does:** Real-time alerts.

1. Room events

```text title="Prompt – monitoring"
Create webhook for room "Q1 Product Launch": events messageCreated.
Target URL: https://webhook.site/my-id.
List webhooks, delete test webhook ID W3k456.
```

---

## Best practices for Webex 

- **IDs from lists.** Get room/team/person ID first.  
- **Roles granular.** member/moderator for teams.  
- **Markdown messages.** Rich formatting.  
- **Webhook secure.** HTTPS targets only.

To connect Webex, open **Settings → Connections → Webex** (“Create Webex Auth Config”). Then run prompts directly from Chat Mode.