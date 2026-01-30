# HubSpot in Chat Mode

Connecting HubSpot lets you **create, update, and track CRM records directly from chat**, keeping deals, contacts, and activities current without opening the CRM.

Use it to log interactions, progress pipelines, and surface insights while staying in conversation.

---

## What HubSpot can do

Once HubSpot is connected (Settings → Connections → HubSpot), you can:

- Create/update Contacts, Companies, Deals, and Tickets.
- Log calls, emails, meetings, and notes against records.
- Search/filter CRM data by status, owner, or date.
- Associate records (link contacts to deals/companies).
- Retrieve timelines and engagement history.

!!! note
    Actions follow your HubSpot permissions and property definitions in your portal.

---

## 1. Capture contacts and companies

### Create contacts and companies

**Capabilities:** Create/update Contact and Company records.  

**What it does:** Turns conversation details into structured CRM records.

1. New lead from outreach

    ```text title="Prompt – create contact"
    Create a HubSpot Contact for "Jordan Lee" at "Peak Performance Consulting".
    Email: jordan@peakperformance.co, Phone: +1-555-0123.
    Company: "Peak Performance Consulting" (create if missing).
    Lifecycle Stage: "Lead", Lead Source: "LinkedIn Outreach".
    Add note: "Expressed interest in API automation during intro call."
    ```

2. Update contact details

    ```text title="Prompt – enrich contact"
    Find the HubSpot Contact "Jordan Lee" and update:
    -  Job Title: "Head of Operations"
    -  Recent Activity: "Discovery call completed 30 mins ago"
    -  Next Step: "Send case study"
    -  Score: +15 points for demo interest
    ```

---

## 2. Manage deals and pipeline

### Create and move deals

**Capabilities:** Create/update Deal records, associate with Contacts/Companies.  

**What it does:** Opens opportunities and advances them through stages.

1. Create a new deal

    ```text title="Prompt – new opportunity"
    Create a HubSpot Deal "Peak Performance – Operations Automation"
    Amount: $24,000, Close Date: March 15, Deal Stage: "Qualified to Buy".
    Associate with Contact "Jordan Lee" and Company "Peak Performance Consulting".
    Owner: current user, Probability: 60%.
    ```

2. Pipeline progression

    ```text title="Prompt – advance deals"
    Find all my Deals in "Qualified Lead" stage with no activity in 7 days.
    Move qualified ones to "Customer Proposal", add note "Follow‑up call completed",
    and set Close Date to 30 days from now.
    List exactly which deals moved and why.
    ```

---

## 3. Log activities and engagements

### Calls, emails, meetings, notes

**Capabilities:** Create activity records (Call, Email, Meeting, Note, Task).  

**What it does:** Documents interactions against contacts/deals for timeline accuracy.

1. Log a discovery call

    ```text title="Prompt – log call"
    Log a HubSpot Call activity against Deal "Peak Performance – Operations Automation":
    Duration: 25 minutes, Outcome: "Positive", Notes:
    "Discussed current workflow pain points. Budget approved.
    Demo scheduled for Feb 5."
    Associated Contact: Jordan Lee.
    ```

2. Create follow‑up tasks

    ```text title="Prompt – schedule tasks"
    For all Deals I own closing this month in "Proposal" stage,
    create Tasks: "Prepare custom demo + proposal deck", due 3 days from now,
    Priority: High. Associate each task with its primary contact.
    ```

---

## 4. Search and analyze CRM data

### Find records and timelines

**Capabilities:** Search Contacts/Companies/Deals, retrieve timelines/properties.  

**What it does:** Surfaces records and engagement history.

1. Pipeline snapshot

    ```text title="Prompt – my deals overview"
    Show my top 8 open Deals by amount this quarter. For each:
    -  Company/Contact
    -  Stage/Probability
    -  Close Date
    -  Last Activity
    -  Next Step

    Highlight any stalled >14 days.
    ```

2. Contact engagement history

    ```text title="Prompt – contact timeline"
    Get the HubSpot timeline for Contact "Jordan Lee" showing last 10 activities.
    Summarize key interactions and suggest next best action.
    ```

---

## 5. Support tickets and service

### Create and manage tickets

**Capabilities:** Create/update Ticket records.  

**What it does:** Captures issues and tracks resolutions.

1. Customer support ticket

```text title="Prompt – create ticket"
Create a HubSpot Ticket "API rate limit confusion" for Contact "Jordan Lee":
Priority: Medium, Source: Email, Category: "Technical".
Description: "Customer unclear on API limits during onboarding."
Assign to default support queue.
```

---

## Best practices for HubSpot

- **Use specific identifiers.** Reference names, emails, or IDs to target exact records.  
- **Include key properties.** Mention Lifecycle Stage, Deal Stage, amounts, dates for completeness.  
- **Preview bulk operations.** Ask to "list first" before updating multiple records.  
- **Link with email/calendar.** Flow: call → log HubSpot activity → email proposal → create task.

To connect HubSpot, open **Settings → Connections → HubSpot** and authorize access. Then run prompts directly from Chat Mode.