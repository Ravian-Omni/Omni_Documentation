# Outlook in Chat Mode

Connecting Outlook lets you **send emails, manage inbox, create events/contacts, and automate workflows directly from chat**, with Microsoft Graph API access.

Use it for email campaigns, calendar scheduling, contact CRM, and notification automation.

---

## What Outlook can do 

Once Outlook is connected (Settings → Connections → Outlook), you can:

- Send/read/draft/reply to emails.
- List/search messages, folders, attachments.
- Create/update events, calendars, contacts.
- Manage categories, rules, subscriptions.

---

## 1. Email management 

### Inbox and sending

**Capabilities:** `SEND_MAIL`, `CREATE_DRAFT`, `REPLY_MESSAGE`, `LIST_MESSAGES`.  

**What it does:** Handles mail flow.

1. Send meeting invite

    ```text title="Prompt – outreach email"
    Send email to team@company.com:
    Subject: "Q2 Planning Kickoff"
    Body: Agenda + RSVP request
    Attachments: q2_goals.docx
    From: your.email@company.com
    CC: execs@company.com
    ```

2. Inbox triage

    ```text title="Prompt – process unread"
    List unread emails last 24h, subject "urgent/action".
    Reply to "Budget Approval": "Approved, proceeding."
    Mark all client@company.com as read, move to "Projects".
    ```

---

## 2. Calendar and events 

### Scheduling

**Capabilities:** `CREATE_EVENT`, `LIST_EVENTS`, `UPDATE_EVENT`, `FIND_MEETING_TIMES`.  

**What it does:** Books meetings.

1. Team sync

```text title="Prompt – schedule call"
Create recurring event "Weekly Sync":
Mon 10AM–11AM, next 8 weeks.
Invite sales-team@company.com, all day reminder.
Find free times for "Client Demo" next week (team + client@partner.com).
```

---

## 3. Contacts and people 

### Relationship management

**Capabilities:** `CREATE_CONTACT`, `LIST_CONTACTS`, `GET_CONTACT`.  

**What it does:** Builds address book.

1. Add leads

```text title="Prompt – bulk contacts"
Create contacts from CSV: name, email, company, notes.
"John Doe, john@startup.com, Acme Tech, Prospect Q1".
List recent contacts, phone numbers.
```

---

## 4. Search and organization 

### Find and categorize

**Capabilities:** `SEARCH_MESSAGES`, `CREATE_CATEGORY`, `MOVE_MESSAGE`, `LIST_FOLDERS`.  

**What it does:** Organizes inbox.

1. Email search

```text title="Prompt – find threads"
Search emails: from:sales@company.com "Q1 pipeline" last month.
Move matches to "Sales Archive".
Create category "Hot Leads" (red), apply to new replies.
```

---

## 5. Advanced automation 

### Rules and subscriptions

**Capabilities:** `CREATE_RULE`, `LIST_SUBSCRIPTIONS`, `DISMISS_NOTIFICATION`.  

**What it does:** Automates flows.

1. Auto-responder

```text title="Prompt – vacation rule"
Create inbox rule: if from:external@domain.com and OOO,
Reply: "On leave until Jan 10, contact support@company.com".
List active subscriptions, pause newsletters.
```

---

## Best practices for Outlook 

- **Folders/categories.** Triage before archive.  
- **Templates for drafts.** Reuse common emails.  
- **Calendar buffers.** 15min between meetings.  
- **Combine with Teams.** Outlook events → Teams channels.

To connect Outlook, open **Settings → Connections → Outlook** (Microsoft OAuth). Then run prompts directly from Chat Mode.