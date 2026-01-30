# Airtable in Chat Mode

Connecting Airtable lets you **create, query, update, and analyze bases directly from chat**, treating your data like a conversational database.

Use it for CRM, project tracking, content calendars, and custom workflows.

---

## What Airtable can do

Once Airtable is connected (Settings → Connections → Airtable), you can:

- Query records with filters, sorts, formulas.
- Create/update records across linked tables.
- Batch operations: bulk create/update/delete.
- Manage fields: add formulas, rollups, lookups.
- Attach files, manage views/shares.

---

## 1. Data querying and analysis

### Find and summarize records

**Capabilities:** Filter/sort records, aggregations, linked record lookups.  

**What it does:** Answers complex data questions.

1. Sales pipeline overview

    ```text title="Prompt – pipeline report"
    Query "CRM Pipeline" table in "Sales Base":
    Show Open Deals (Status != "Closed Won/Lost") sorted by Amount DESC.

    Columns: Deal Name, Account, Amount, Stage, Close Date, Owner
    Filter: Close Date this quarter
    Group by Stage, count deals + total Amount.

    Format as table with weighted pipeline column.
    ```

2. Customer health check

    ```text title="Prompt – account analysis"
    From "Accounts" table: find accounts with:
    -  ARR > $10K
    -  Last activity > 90 days ago
    -  NPS score exists

    Show: Account, ARR, Last Touch, NPS, Key Contact.
    Suggest win‑back actions.
    ```

---

## 2. Record creation and updates

### Add and modify data

**Capabilities:** Create records, update fields, link records.  

**What it does:** Populates tables from conversations.

1. New deals from leads

    ```text title="Prompt – create pipeline"
    In "CRM Pipeline" table, create 3 new Deal records:

    1. "Peak Performance Ops" | Amount $24K | Stage "Demo" | Close Mar 15 | Owner Sarah
    2. "TechCo Expansion" | $45K | "Proposal" | Feb 28 | Jordan  
    3. "NewCo Trial" | $8K | "Qualified" | Apr 1 | Me

    Link to respective Account records, set probability.
    ```

2. Bulk opportunity update

    ```text title="Prompt – stage progression"
    Find Deals where Stage = "Demo Complete" AND Days in Stage > 3.
    Update to "Proposal", add note "Proposal sent [today]",
    calculate new Close Date (+30 days).

    Show before/after for top 5 by Amount.
    ```

---

## 3. Linked records and relationships

### Cross‑table operations

**Capabilities:** Create linked records, lookup/rollup formulas.  

**What it does:** Maintains relational integrity.

1. Customer + opportunity linking

```text title="Prompt – relational update"
For new Deals "Peak Performance Ops", "TechCo Expansion":
-  Link to Account records by name
-  Set primary Contact (lookup from Account)
-  Calculate Account Lifetime Value (rollup from Deals)

Verify all links resolved correctly.
```

---

## 4. Automation and workflows

### Field formulas and views

**Capabilities:** Add formula fields, create filtered views.  

**What it does:** Encodes business logic.

1. Risk scoring formula

```text title="Prompt – add calculated field"
In "CRM Pipeline" table, create Formula field "Risk Score":
IF(AND(Days in Stage > 14, Probability < 60%), "High", 
  IF(Days in Stage > 7, "Medium", "Low"))

Create view "High Risk Deals" filtered by Risk Score = "High".
Share view link.
```

---

## 5. Reporting and export

### Summaries and interfaces

**Capabilities:** Grouped views, aggregations, CSV export.  

**What it does:** Generates reports and shares insights.

1. Executive dashboard

```text title="Prompt – leadership report"
Create grouped view in "CRM Pipeline":
Group by Owner, show: Count, Sum Amount, Avg Close Date
Filter: Created this month

Export top 3 Owners by pipeline as PDF summary.
Email to execs@company.com.
```

---

## Best practices for Airtable

- **Explicit table/base names.** "Sales Base.CRM Pipeline" format.  
- **Test filters with COUNT.** Verify before bulk updates.  
- **Linked records first.** Create parents before children.  
- **Combine with calendars.** Flow: HubSpot sync → Airtable analysis → Google Meet → update status.

To connect Airtable, open **Settings → Connections → Airtable** (API key + base ID). Then run prompts directly from Chat Mode.