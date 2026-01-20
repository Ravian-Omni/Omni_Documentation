# Google Sheets in Chat Mode

Connecting Google Sheets lets Ravian **create, read, update, and analyze spreadsheets directly from chat**, turning “do this in Sheets” into executed actions.

Use it for quick data entry, reporting, lightweight analytics, and syncing tables with other tools.

---

## What Ravian can do with Google Sheets

Once Google Sheets is connected (Settings → Connections → Google Sheets), Ravian can:

- Create spreadsheets and sheets, and organize them in Drive.
- Append rows, update ranges, clear data, and format cells.
- Run SQL‑like queries and aggregations over tables.
- Build charts and dashboards from live data.
- Upsert rows for CRM / inventory syncs without duplicating data.

!!! note
    Google Sheets works especially well when combined with Gmail, Drive, and Notion in the same workflow.

---

## 1. Create and organize spreadsheets

### Create spreadsheets and sheets

**Capabilities:** `GOOGLESHEETS_CREATE_GOOGLE_SHEET1, GOOGLESHEETS_ADD_SHEET, GOOGLESHEETS_CREATE_SPREADSHEET_ROW/COLUMN`

**What it does:** Creates new spreadsheets and tabs, and inserts rows/columns where you need them.

1. Create a spreadsheet

    ```text title="Prompt – create a spreadsheet"
    Create a new Google Sheet called "Ravian Job Tracker" in my Drive.
    Add sheets named "Pipeline", "Applied", and "Interviews".
    ```

2. Add rows/columns

    ```text title="Prompt – add rows/columns"
    In the "Ravian Job Tracker" sheet, add a column called "Status"
    after the "Company" column, and insert 5 empty rows at the top
    of the "Pipeline" tab.
    ```

---

## 2. Append, update, and clear data

### Append and update ranges

**Capabilities:** `GOOGLESHEETS_SPREADSHEETS_VALUES_APPEND, GOOGLESHEETS_VALUES_UPDATE, GOOGLESHEETS_BATCH_UPDATE`

**What it does:** Appends new rows or overwrites existing cell ranges with fresh data.

1. Append new data

    ```text title="Prompt – append new data"
    Open the "Ravian Job Tracker" sheet, tab "Pipeline", and append these rows:

    Company | Role | Source
    Acme Corp | Senior Data Scientist | LinkedIn
    Beta Labs | AI Engineer | Naukri
    ```

2. Overwrite a range

    ```text title="Prompt – overwrite a range"
    In "Ravian Job Tracker" → "Applied" tab, update the range A1:D1
    to the headers: Company, Role, Date Applied, Status.
    Make sure the existing header row is replaced, not duplicated.
    ```

### Clear values without losing formatting

**Capabilities:** `GOOGLESHEETS_CLEAR_VALUES, GOOGLESHEETS_SPREADSHEETS_VALUES_BATCH_CLEAR`

**What it does:** Clears values from ranges while keeping formatting, notes, and validation rules.


```text title="Prompt – clear old data"
In the "Ravian Job Tracker" sheet, clear all values in the range
Applied!A2:D100 but keep the headers and formatting.
```

---

## 3. Treat Sheets like a database

### Query and aggregate data

**Capabilities:** `GOOGLESHEETS_EXECUTE_SQL, GOOGLESHEETS_QUERY_TABLE, GOOGLESHEETS_AGGREGATE_COLUMN_DATA`

**What it does:** Runs SQL‑style or filtered queries and aggregations over tables to answer questions from your data.

1. SQL-style query

    ```text title="Prompt – SQL-style query"
    On the "Sales_Data" sheet in the file "Q4_Sales", run a query to
    show total revenue and average deal size by region for Q4 2025.
    Return the results as a table and also paste them into a new sheet
    called "Region Summary".
    ```

2. Aggregate a column

    ```text title="Prompt – aggregate a column"
    In "Marketing_Campaigns" sheet, calculate the total spend and
    average CTR for rows where CampaignType is "Email".
    Summarize the result in bullets and update a small summary table
    on the sheet.
    ```

### Upsert rows (smart sync)

**Capabilities:** `GOOGLESHEETS_UPSERT_ROWS`

**What it does:** Updates existing rows by key and inserts new ones, avoiding duplicates when syncing from other systems.

```text title="Prompt – CRM-style upsert"
In the "Leads" sheet of "Ravian_CRM", upsert these rows using
Email as the key column:

Email, Name, Stage
jane@example.com, Jane Doe, Qualified
rahul@example.in, Rahul Mehta, Contacted

Update existing rows if the email already exists; otherwise
append as new leads.
```

---

## 4. Find, filter, and restructure

### Find & replace, lookups, and filters

**Capabilities:** `GOOGLESHEETS_FIND_REPLACE, GOOGLESHEETS_LOOKUP_SPREADSHEET_ROW, GOOGLESHEETS_SET_BASIC_FILTER, GOOGLESHEETS_CLEAR_BASIC_FILTER`

**What it does:** Searches for values, replaces them in bulk, looks up rows by key, and applies/clears basic filters.

1. Fix a typo everywhere

    ```text title="Prompt – fix a typo everywhere"
    In the "Product_Analytics" sheet, replace all occurrences of
    "Ravain" with "Ravian" in every tab. Show me how many cells
    you changed before and after.
    ```

2. Lookup a row

    ```text title="Prompt – lookup a row"
    In the "Ravian Job Tracker" → "Pipeline" tab, find the row where
    Company equals "Acme Corp" and show me the full row contents.
    Then move that row to the "Applied" tab and set Status to "Applied".
    ```

3. Temporary filter

    ```text title="Prompt – temporary filter"
    On the "Transactions" tab in "Finance_2025", apply a filter to show
    only rows where Amount > 50000. Sort by Date descending, then tell
    me how many such transactions there are. Clear the filter when done.
    ```

---

## 5. Formatting, validation, and structure

### Format cells and conditional rules

**Capabilities:** `GOOGLESHEETS_FORMAT_CELL, GOOGLESHEETS_MUTATE_CONDITIONAL_FORMAT_RULES`

**What it does:** Applies formatting to ranges and manages conditional formatting rules to highlight important data.


```text title="Prompt – highlight important data"
In "Sales_Data", apply conditional formatting to highlight rows
in red where Win/Loss is "Lost" and DealSize > 50000.
Add a soft green background for rows where Win/Loss is "Won".
```

### Data validation and dropdowns

**Capabilities:** `GOOGLESHEETS_SET_DATA_VALIDATION_RULE, GOOGLESHEETS_GET_DATA_VALIDATION_RULES`

**What it does:** Creates and inspects data validation rules, such as dropdowns and custom constraints.

```text title="Prompt – add status dropdown"
In the "Ravian Job Tracker" → "Pipeline" tab, add a dropdown
validation for the Status column with values:
"Applied", "Interviewing", "Offer", "Rejected", "On Hold".
Apply it for rows 2 to 200.
```

---

## 6. Charts and reporting

### Create charts from ranges

**Capabilities:** `GOOGLESHEETS_CREATE_CHART`

**What it does:** Builds charts (line, bar, pie, etc.) based on specified ranges or chart specs.

```text title="Prompt – create a chart"
In the "Sales_Data" sheet, create a line chart of MonthlyRevenue
by Month for 2025 and place it on a new sheet called "Revenue Chart".
Make the chart suitable for an executive presentation.
```

### Build summary sheets from JSON

**Capabilities:** `GOOGLESHEETS_SHEET_FROM_JSON`

**What it does:** Creates a new sheet and populates it from JSON records, automatically inferring headers.

```text title="Prompt – sheet from JSON"
Take this JSON of job applications from the chat and create a new
Google Sheet called "Job_Applications_Overview". Use the keys as
column headers and each object as a row.
```

---

## 7. Sheet and spreadsheet metadata

### Discover structure

**Capabilities:** `GOOGLESHEETS_GET_SHEET_NAMES, GOOGLESHEETS_GET_SPREADSHEET_INFO, GOOGLESHEETS_LIST_TABLES, GOOGLESHEETS_GET_TABLE_SCHEMA`

**What it does:** Lists sheet names, tables, and table schemas so Ravian understands how to work with your file.

```text title="Prompt – understand this file"
Inspect the spreadsheet "Ravian_Analytics_2025" and tell me:
- All sheet names
- Which sheets look like tables (with header rows)
- For each table, a guessed schema (column names and types)
```

---

## Best practices for Google Sheets with Ravian

- **Name things clearly.** Use explicit spreadsheet and sheet names in prompts to avoid acting on the wrong file.  
- **Start read‑only.** Begin with “show/summarize” prompts before asking Ravian to mutate data in important sheets.  
- **Use upserts for sync.** When syncing from CRMs, CSVs, or APIs, prefer upsert‑style prompts instead of repeated appends.  
- **Combine with other tools.** For example: scrape web data → write to Sheets → build chart → export to a Slides deck via Ravian.

To connect Google Sheets, open **Settings → Connections → Google Sheets** in the Ravian app and complete the sign‑in flow. After that, you can run any of the prompts above directly from Chat Mode.