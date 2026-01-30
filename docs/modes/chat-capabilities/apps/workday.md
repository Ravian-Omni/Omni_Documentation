# Workday in Chat Mode

Connecting Workday lets you **request vacations, check absence balances, manage job postings, summarize interview feedback, and handle HR workflows directly from chat** via cloud ERP for HCM, finance, and analytics.

Use it for time-off management, recruiting, employee data, and performance insights.

---

## What Workday can do 

Once Workday is connected (Settings → Connections → Workday), you can:

- Submit absence requests (vacation, sick time).
- Retrieve balance summaries, open job postings.
- Access feedback/interview data, worker details.
- Manage recruiting, onboarding, reports.

---

## 1. Time and absence 

### Vacation and balances

**Capabilities:** Request time off, check absence balance.  

**What it does:** Manages PTO.

1. Vacation request

    ```text title="Prompt – time off"
    Request vacation: Feb 10-14, 2026 (5 days).
    Type: Vacation, all-day.
    Submit for approval.
    ```

2. Balance check

    ```text title="Prompt – PTO status"
    Get my current absence balance.
    List upcoming requests.
    ```

---

## 2. Recruiting and jobs 

### Postings and interviews

**Capabilities:** Find open job postings, summarize feedback.  

**What it does:** Hiring workflows.

1. Job postings

    ```text title="Prompt – recruiting"
    Find all open job postings I manage.
    List titles, locations, status.
    ```

2. Interview feedback

    ```text title="Prompt – candidate review"
    Summarize feedback from recent interviews.
    Extract top candidates, strengths/weaknesses.
    ```

---

## 3. Employee management 

### Workers and reports

**Capabilities:** Get worker details, generate reports.  

**What it does:** HR data.

1. Employee lookup

```text title="Prompt – team overview"
Get details for employee ID 12345: position, manager, start date.
List team members reporting to me.
```

---

## 4. Onboarding and approvals 

### New hires

**Capabilities:** Onboarding tasks, approval workflows.  

**What it does:** Streamlines starts.

1. New hire setup

```text title="Prompt – onboarding"
Create onboarding task for "New Developer".
Assign laptop, training, approvals.
Check approval status.
```

---

## 5. Analytics and reports 

### Insights

**Capabilities:** Custom reports, HCM analytics.  

**What it does:** Business intelligence.

1. Turnover report

```text title="Prompt – HR metrics"
Generate Q1 turnover report.
Filter department: Engineering.
Export CSV.
```

---

## Best practices for Workday 

- **Permissions strict.** HR admin for sensitive ops.  
- **IDs precise.** Worker/posting ID for actions.  
- **Workflows follow.** Submit → approve chain.  
- **Combine with email.** Workday request → Outlook notify.

To connect Workday, open **Settings → Connections → Workday** (OAuth/MCP auth). Then run prompts directly from Chat Mode.