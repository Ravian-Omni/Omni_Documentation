# Salesforce in Chat Mode

Connecting Salesforce lets Ravian **create, update, and inspect CRM records directly from chat**, so pipeline updates and follow‑ups happen while you talk through the work.

Use it to manage leads, opportunities, accounts, and cases without living in the Salesforce UI all day.

---

## What Ravian can do with Salesforce

Once Salesforce is connected (Settings → Connections → Salesforce), Ravian can:

- Create and update Leads, Contacts, Accounts, and Opportunities.
- Log activities and notes after calls or meetings.
- Search and filter records by status, owner, or timeframe.
- Move deals through stages and keep fields clean.
- Generate summaries and next‑step plans from CRM data.

!!! note
    Exactly which objects and fields Ravian can touch depend on your Salesforce permissions and org configuration.

---

## 1. Capture leads and contacts

### Create leads and contacts

**Capabilities:** Salesforce record‑create / record‑update actions for Lead and Contact objects.  

**What it does:** Turns conversational descriptions into structured lead/contact records with the right fields filled.

1. Create a new lead from a call

    ```text title="Prompt – create a lead"
    Create a new Salesforce Lead for "Aditi Sharma" at "Northbridge Analytics".
    Use aditi.sharma@northbridge.com as the email, mark the Lead Source as
    "Inbound – Demo Request", and add a note that she is interested in
    an automation pilot for the operations team.
    Assign the lead to the current owner of the India SMB territory.
    ```

2. Convert a contact from ad‑hoc notes

    ```text title="Prompt – contact from notes"
    From these meeting notes, create a Salesforce Contact linked to the
    existing account "Aurora Fintech". Include role, phone, and any buying
    signals you detect in the description field.
    ```

---

## 2. Keep pipeline and deals up to date

### Create and update opportunities

**Capabilities:** Salesforce record‑create / record‑update actions for Opportunity and related objects.  

**What it does:** Opens new opportunities, updates stages, amounts, close dates, and links them to accounts and contacts.

1. Open a new opportunity

    ```text title="Prompt – new opportunity"
    Create a new Opportunity called "Aurora Fintech – Automation Rollout"
    for the "Aurora Fintech" account. Set the stage to "Qualification",
    amount to 45,00,000 INR, close date 90 days from now, and owner as
    the current user. Link any known primary contact on the account.
    ```

2. Progress deals through stages

    ```text title="Prompt – stage updates"
    Find all open Opportunities I own that had a meeting in the last
    7 days and are still in "Qualification". For each, move the stage
    to "Proposal" if meeting notes mention a budget or concrete timeline.
    Add a short summary of the rationale in the Opportunity description.
    Show me a list of every deal you changed.
    ```

---

## 3. Search, filter, and summarize records

### Find accounts, opportunities, and cases

**Capabilities:** Salesforce query/search tools for standard objects (Account, Opportunity, Case, Lead, Contact).  

**What it does:** Runs SOQL‑like searches and returns focused lists that Ravian can summarize.

1. Today’s focus list

    ```text title="Prompt – focus opportunities"
    Show me my top 10 open Opportunities in the current quarter
    sorted by amount, where the next activity date is blank or overdue.
    Summarize each in one line and propose who I should contact today.
    ```

2. Account health snapshot

    ```text title="Prompt – account health"
    For the account "Nimbus Retail", pull recent Opportunities, open Cases,
    and last 5 activities. Summarize account health in 5 bullets including
    risk signals and upsell possibilities.
    ```

---

## 4. Log activities and notes

### Tasks, events, and call logs

**Capabilities:** Salesforce create/update actions for Task, Event, and Activity objects.  

**What it does:** Logs follow‑ups, meetings, and notes so CRM stays current after conversations and calls.

1. Log a completed call

    ```text title="Prompt – log call outcome"
    Log a completed call activity on the Opportunity
    "Aurora Fintech – Automation Rollout" with subject
    "Discovery Call – 30 min". Use this chat summary as the call notes,
    mark the outcome as "Positive", and set the due date to today.
    ```

2. Schedule follow‑up tasks

    ```text title="Prompt – follow‑up tasks"
    For all Opportunities closing this month with stage "Proposal",
    create follow‑up Tasks for me:
    - Due in 3 days
    - Subject "Proposal follow‑up"
    - Priority "High"
    Include a short prompt in each task suggesting what to ask the customer.
    ```

---

## 5. Customer support and cases

### Create and manage cases

**Capabilities:** Salesforce Case object create/update/search tools.  

**What it does:** Captures support issues as Cases, updates status and priority, and keeps them linked to Accounts and Contacts.

1. Turn an email into a case

    ```text title="Prompt – email to case"
    From this pasted customer email, create a Salesforce Case under the
    appropriate Account and Contact. Set the priority based on how urgent
    the issue sounds, categorize it under the best matching case type,
    and include the full email body in the description.
    Assign the case to the default support queue.
    ```

2. Triage open cases

    ```text title="Prompt – triage queue"
    Look at all open Cases in the "APAC – Support" queue that are older
    than 3 days. Group them by priority and product, and highlight the
    5 cases that look most at risk of escalation based on status and age.
    Suggest next actions for each.
    ```

---

## Best practices for Salesforce with Ravian

- **Be explicit about objects.** Mention whether you’re working with Leads, Contacts, Accounts, Opportunities, or Cases.  
- **Anchor prompts with names and IDs.** Include account names, opportunity names, or record IDs to avoid ambiguity.  
- **Confirm bulk changes.** For multi‑record updates (many deals or cases), ask Ravian to show a preview list before applying changes.  
- **Blend with email and calendar.** A powerful flow is: summarize a call → update the Opportunity and Case in Salesforce → draft a follow‑up email → schedule the next meeting, all from Chat Mode.

To connect Salesforce, open **Settings → Connections → Salesforce** in the Ravian app and complete the sign‑in flow. After that, you can run any of the prompts above directly from Chat Mode.