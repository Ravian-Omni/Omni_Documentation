# Excel in Chat Mode

Connecting Excel lets you **create, analyze, and automate spreadsheets directly from chat**, performing complex calculations and data manipulation conversationally.

Use it for financial models, sales forecasting, data analysis, and dashboards.

---

## What Excel can do

Once Excel is connected (Settings → Connections → Excel), you can:

- Create new workbooks/sheets from data or templates.
- Read cell ranges, tables, named ranges.
- Write formulas, update values, format cells.
- Create charts, pivot tables, conditional formatting.
- Perform bulk operations, data validation.
- Export/share workbooks.

---

## 1. Data entry and tables

### Populate spreadsheets

**Capabilities:** Create sheets, insert tables, populate from data.  

**What it does:** Builds structured data instantly.

1. Sales pipeline tracker

    ```text title="Prompt – create pipeline sheet"
    Create Excel workbook "Q1 Pipeline Forecast.xlsx", Sheet "Deals":

    Columns A–H: Deal Name | Account | Stage | Amount | Probability | Close Date | Weighted | Owner

    Data:
    Peak Perf | Peak Performance | Proposal | 24000 | 70% | 2/15/26 | =D2*E2 | Sarah
    TechCo | TechCo Inc | Demo | 45000 | 50% | 2/28/26 | =D3*E3 | Jordan

    Auto‑format currency/dates, add totals row.
    ```

2. Monthly P&L

    ```text title="Prompt – financial table"
    In new "Jan P&L.xlsx", create table:

    Revenue | Cost | Gross Profit | % Margin
    SaaS | 45000 | 12000 | =B2-C2 | =D2/B2
    Services | 18000 | 4500 | =B3-C3 | =D3/B3

    Format % margins green/red conditional, bold totals.
    ```

---

## 2. Formulas and calculations

### Advanced computations

**Capabilities:** Complex formulas, lookups, financial functions.  

**What it does:** Builds dynamic models.

1. Forecasting model

    ```text title="Prompt – sales forecast"
    In "Forecast 2026.xlsx", Sheet "Monthly":

    Row 1: Jan | Feb | Mar | ... | Dec
    Row 2: Pipeline | 24000 | 45000 | 32000 | ...
    Row 3: Close Rate | 25% | 28% | 30% | ...
    Row 4: Forecast | =B2*B3 | =C2*C3 | ...

    Add YoY growth column, sparkline charts per month.
    ```

2. Cohort analysis

    ```text title="Prompt – customer cohorts"
    Create cohort table from customer data:
    Rows: Signup Month (Jan, Feb...)
    Columns: Retention Month (1, 2, 3...)
    Values: % retained customers

    Use array formula for matrix calculation.
    Heatmap conditional formatting.
    ```

---

## 3. Charts and visualization

### Graphs and dashboards

**Capabilities:** Create charts (bar/line/pie/scatter), sparklines.  

**What it does:** Visualizes data instantly.

1. Pipeline funnel chart

    ```text title="Prompt – visualization"
    In "Pipeline Dashboard.xlsx":

    Data:
    Stage | Deals | Amount
    Lead | 120 | $1.2M
    Demo | 45 | $850K
    Proposal | 18 | $450K
    Closed | 9 | $320K

    Create stacked bar chart (count + value).
    Dashboard title, source legend.
    ```

2. KPI dashboard

    ```text title="Prompt – executive summary"
    Create Sheet "KPIs" with:
    -  ARR gauge chart (target vs actual)
    -  Monthly revenue line chart (12 months)
    -  Top customers pie (top 5)
    -  Pipeline sparkline trend

    Dynamic titles with TODAY() date.
    ```

---

## 4. Data manipulation

### Pivot tables and filters

**Capabilities:** Pivot tables, slicers, data validation.  

**What it does:** Analyzes large datasets.

1. Sales rep performance pivot

```text title="Prompt – pivot analysis"
Create pivot table from "Sales Data":
Rows: Rep Name
Columns: Month
Values: Sum Amount, Count Deals, Avg Deal Size

Add slicers: Region, Product Type.
Top 5 reps highlight.
```

---

## 5. Automation and sharing

### Templates and collaboration

**Capabilities:** Named ranges, data validation, sharing.  

**What it does:** Creates reusable tools.

1. Deal calculator template

```text title="Prompt – interactive calculator"
Create "Deal Calculator.xlsx":

Inputs: ARR | Expansion % | Discount | Term Months
Formulas: Monthly | Annualized | NPV
Data validation: Discount 0–25%

Share with sales team (edit), protect formulas.
```

---

## Best practices for Excel

- **Named ranges.** Reference "PipelineData" vs A1:Z100.  
- **Dynamic formulas.** Use OFFSET/INDIRECT for growing data.  
- **Conditional formatting.** Visual alerts > manual review.  
- **Combine with Sheets.** Excel for models → Google Sheets for collab → Docs report.

To connect Excel, open **Settings → Connections → Microsoft Excel** (OneDrive/SharePoint OAuth). Then run prompts directly from Chat Mode.