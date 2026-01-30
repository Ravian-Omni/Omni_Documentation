# Instantly in Chat Mode

Connecting Instantly lets you **launch cold email campaigns, manage leads, monitor deliverability, and scale outreach directly from chat**, automating sales sequences.

Use it for prospecting, A/B testing, inbox warmup, and campaign analytics.

---

## What Instantly can do 

Once Instantly is connected (Settings → Connections → Instantly), you can:

- Create campaigns, add leads/lists, activate/pause sequences.
- Enrich leads with AI/SuperSearch, verify emails.
- Monitor analytics: opens, replies, deliverability tests.
- Manage accounts, warmups, blocklists, webhooks.
- Bulk operations: assign leads, merge duplicates.

!!! note
    API key authentication; respect send limits and compliance.

---

## 1. Campaign setup 

### Create and launch campaigns

**Capabilities:** `INSTANTLY_CREATE_CAMPAIGN`, `INSTANTLY_ACTIVATE_CAMPAIGN`, `INSTANTLY_ADD_LEADS_BULK`.  

**What it does:** Builds complete outreach sequences.

1. Cold email campaign

    ```text title="Prompt – launch sequence"
    Create Instantly campaign "Q1 Fintech Ops Automation":
    - Name: "Fintech Ops Workflow Outreach"
    - Sequence: 7 emails (intro → value → case study → demo → urgency)
    - Senders: rotate 3 warmed accounts
    - Add 200 leads from CSV (fintech_ops_leads.csv)

    Activate once leads verified, set daily limit 50.
    ```

2. A/B test variant

    ```text title="Prompt – test subject lines"
    Duplicate "Fintech Ops" campaign → "Fintech Ops A/B".
    Update Step 1 subject: "Automate ops?" vs "Ops teams: 40% faster".
    Split leads 50/50, track reply rates.
    ```

---

## 2. Lead management 

### Add/enrich leads

**Capabilities:** `INSTANTLY_CREATE_LEAD`, `INSTANTLY_CREATE_AI_ENRICHMENT`, `INSTANTLY_VERIFY_EMAIL`.  

**What it does:** Builds targeted lists.

1. Bulk import and enrich

    ```text title="Prompt – prospect list"
    Create lead list "Fintech VPs", bulk add 500 from Apollo CSV.
    Run AI enrichment: job title, company revenue, recent funding.
    Verify emails, remove bounces.
    Assign to "Ops Campaign", tag "high-priority".
    ```

2. Interest status update

    ```text title="Prompt – qualify replies"
    Find leads with replies containing "interested/demo".
    Update interest status "Hot", move to "Demo Sequence".
    Notify sales@company.com with email thread.
    ```

---

## 3. Deliverability and warmup 

### Inbox health

**Capabilities:** `INSTANTLY_ENABLE_ACCOUNT_WARMUP`, `INSTANTLY_CREATE_INBOX_PLACEMENT_TEST`, `INSTANTLY_ACCOUNTS_CTD_STATUS_GET`.  

**What it does:** Optimizes sending reputation.

1. Warmup new accounts

```text title="Prompt – sender prep"
Enable warmup for 3 new accounts: ops1@company.com, ops2@company.com.
Set daily volume ramp: 20→50→100 over 2 weeks.
Run inbox placement test to Gmail/Yahoo.
Monitor health score >90%.
```

---

## 4. Analytics and optimization 

### Performance tracking

**Capabilities:** `INSTANTLY_CAMPAIGNS_ANALYTICS_OVERVIEW_GET`, `INSTANTLY_GET_CAMPAIGN_ANALYTICS`.  

**What it does:** Iterates winning sequences.

1. Campaign report

```text title="Prompt – performance dashboard"
Get analytics for "Fintech Ops" campaign:
-  Open/reply rates by step
-  Top performing subject lines
-  Bounce/reply positive keywords
-  Best send days/times

Pause low‑performers, scale winners.
```

---

## 5. Advanced automation 

### Subsequences and webhooks

**Capabilities:** `INSTANTLY_CREATE_SUBSEQUENCE`, `INSTANTLY_CREATE_WEBHOOK`.  

**What it does:** Triggers dynamic follow-ups.

1. Reply‑based branching

```text title="Prompt – smart follow-up"
Create subsequence for "Fintech Ops":
Trigger: reply contains "demo/price"
-  Step 1: Demo recording + pricing
-  Step 2: Calendly link (if no reply 3 days)

Webhook to Slack #sales on positive replies.
```

---

## Best practices for Instantly 

- **Warmup first.** 2–4 weeks before campaigns.  
- **A/B everything.** Subjects, send times, content.  
- **Personalize smartly.** Variables + AI enrichment.  
- **Monitor daily.** Bounce >2%, reply <5% → pause.

To connect Instantly, open **Settings → Connections → Instantly** (API key auth). Then run prompts directly from Chat Mode.