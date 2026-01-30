# Apollo in Chat Mode

Connecting Apollo lets you **enrich prospects, manage sequences, and track outreach directly from chat**, building targeted lists and automating follow-ups.

Use it for lead generation, account research, and sales cadence management.

---

## What Apollo can do

Once Apollo is connected (Settings → Connections → Apollo), you can:

- Search/enrich people and accounts by name, title, domain, etc.
- Create/update contacts and accounts with verified data.
- Manage sequences: enroll contacts, track engagement.
- Save lists, add notes/tags, export data.
- Monitor email deliverability and reply rates.

!!! note
    Apollo respects your plan limits (credits/searches) and compliance settings.

---

## 1. Prospect research and enrichment

### Find and enrich leads

**Capabilities:** Search people/accounts, enrich by email/domain, verify data.  

**What it does:** Builds verified contact lists from company or role criteria.

1. Tech leadership at fintechs

    ```text title="Prompt – build prospect list"
    Search Apollo for VP Engineering or CTO at fintech companies
    (headcount 50–500) in US/UK, recent funding rounds.
    Enrich top 25 with verified emails, direct dials, LinkedIn.
    Export as CSV with: name, title, company, email, phone, funding date.
    ```

2. Single account deep dive

    ```text title="Prompt – enrich target account"
    Enrich "Stripe.com": get decision makers (Head of Sales, Partnerships),
    verified emails/phones, recent hires in sales org, funding history.
    Add notes: "Enterprise payments leader, API‑first culture."
    ```

---

## 2. Contact and account management

### Create/update records

**Capabilities:** Create Apollo Contacts/Accounts, add to lists, tag/note.  

**What it does:** Saves enriched data to Apollo CRM.

1. Add enriched prospects

    ```text title="Prompt – save prospects"
    Create Apollo Contacts from this list:
    1. Jordan Lee, Head of Ops, peakperformance.co, jordan@...
    2. Sarah Chen, VP Sales, techco.com, sarah@...

    Add to List "Q1 Fintech Pipeline", tag "verified-email",
    note "Enriched Jan 30 – demo interest expressed".
    ```

2. Update engagement status

    ```text title="Prompt – mark engaged"
    Find Contacts in "Q1 Fintech Pipeline" list who opened emails
    last 7 days. Update custom field "Engagement Score" +20,
    move to "Warm Leads" list, add note "Email opens detected."
    ```

---

## 3. Sales sequences and cadences

### Enroll and track outreach

**Capabilities:** Create/enroll in sequences, monitor performance.  

**What it does:** Automates multi‑touch campaigns.

1. Start sequence for new leads

    ```text title="Prompt – enroll in cadence"
    Enroll the 10 most recently added contacts in "Q1 Fintech Pipeline"
    into sequence "Fintech Demo Cadence" (7 emails + 3 LinkedIn touches).
    Personalize first email subject: "[Name], automate your ops workflows?"
    Set daily send limit: 5.
    ```

2. Sequence performance

    ```text title="Prompt – outreach analytics"
    Show performance of "Fintech Demo Cadence" sequence:
    -  Total enrolled, replies, meetings booked
    -  Top performing emails by open/reply rate
    -  Best time to send (day/hour)
    Suggest A/B test for next email.
    ```

---

## 4. Lists and segmentation

### Build and manage lists

**Capabilities:** Create/save lists, segment/filter contacts.  

**What it does:** Organizes prospects for campaigns.

1. High‑intent segment

```text title="Prompt – create buying signal list"
Create Apollo List "Hot Leads Q1" with Contacts who:
-  Opened 3+ emails last 30 days
-  Visited pricing page
-  Company domain ends in .io or fintech.com
Export enriched details for top 20.
```

---

## 5. Account‑based selling

### ABM targeting

**Capabilities:** Account search, buying committee mapping.  

**What it does:** Maps decision makers at target accounts.

1. Buying committee map

```text title="Prompt – ABM research"
For accounts "fintech-a.com", "fintech-b.com", "fintech-c.com":
Map buying committee: CRO, VP Sales, Head of RevOps.
Enrich emails/LinkedIn, note influencers/champions.
Create shared list "ABM Target Committees".
```

---

## Best practices for Apollo

- **Batch enrichment wisely.** Enrich 25–50 at a time to respect credits.  
- **Personalize sequences.** Reference specific account pain points.  
- **Track engagement signals.** Monitor opens/replies before advancing.  
- **Combine with email/CRM.** Flow: Apollo enrich → HubSpot create deal → Gmail sequence → Notion research notes.

To connect Apollo, open **Settings → Connections → Apollo**, enter your API key. Then run prompts directly from Chat Mode.