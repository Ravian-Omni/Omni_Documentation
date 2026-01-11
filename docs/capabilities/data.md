# Data Analysis & Visualization

Ravian AI turns raw data into **clean analyses and visual stories**, automating the full workflow from dataset discovery to charts, dashboards, and narratives.

You specify the question and data sources; Ravian handles loading, cleaning, transforming, modeling, and visualizing.

---

## What this capability does

Ravian’s data workflows can:

- Locate and ingest datasets from local files, cloud storage, or public sources.
- Clean and preprocess data, handle missing values, encode categories, and engineer features.
- Run exploratory data analysis (EDA) with descriptive statistics and visual summaries.
- Build and evaluate machine learning models where appropriate, such as classification or regression.
- Generate visual outputs including charts, dashboards, and annotated plots for stakeholders.

!!! note
    Ravian executes Python and related tools behind the scenes while keeping notebooks, scripts, and outputs on your machine.

---

## Typical workflows

Examples of data workflows:

- Exploring a newly received CSV and producing an EDA report.
- Building a churn‑prediction model and summarizing its performance.
- Comparing cohorts or segments with visual breakdowns.
- Creating management‑ready dashboards from operational data.

Ravian can also convert finished analyses into presentations or written briefings as part of the same task.

---

## Example: EDA and model from a public dataset

1. Ask Ravian something like:

    ```text title="prompt"
    Find a public telecom churn dataset, run a full EDA, train a simple model, and create a short HTML report of findings.
    ```

2. Ravian discovers the dataset, downloads it, cleans columns, and runs EDA.

3. It trains a model, evaluates metrics, and generates plots embedded in an HTML or notebook report saved locally.

You can then request a slide deck summarizing the same analysis without re‑running the workflow.