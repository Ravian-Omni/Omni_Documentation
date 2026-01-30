# Kaggle in Chat Mode

Connecting Kaggle lets you **access datasets, submit competitions, manage kernels, and explore ML resources directly from chat**, accelerating data science workflows.

Use it for competitions, dataset discovery, kernel execution, and API configuration.

---

## What Kaggle can do 

Once Kaggle is connected (Settings → Connections → Kaggle), you can:

- Download competition datasets and kernel outputs.
- List/search datasets, create/publish new ones.
- Submit competition entries, check statuses.
- Configure Kaggle API (keys, paths, proxies).
- Initialize dataset/kernel metadata.

!!! note
    Kaggle API token (kaggle.json) required for authentication.

---

## 1. Dataset discovery and download 

### Find and access data

**Capabilities:** `LIST_KAGGLE_DATASETS`, `LIST_KAGGLE_DATASET_FILES`, `DOWNLOAD_COMPETITION_DATA_FILES`.  

**What it does:** Locates and retrieves datasets.

1. Titanic competition data

    ```text title="Prompt – competition prep"
    List datasets for "Titanic" competition, download data files to./titanic-data.
    Include train.csv, test.csv, gender_submission.csv.
    Verify download complete, show file sizes/shapes.
    ```

2. COVID trends search

    ```text title="Prompt – dataset search"
    Search Kaggle datasets: "COVID-19 trends 2025–2026".
    Filter: >10K upvotes, <1 year old, CSV format.
    List top 5 with description, file count, usability score.
    Download #1 to./covid-data.
    ```

---

## 2. Dataset creation and publishing 

### Share your data

**Capabilities:** `DATASET_CREATE`, `CREATE_DATASET_VERSION`, `GET_DATASET_STATUS`, `KAGGLE_DATASET_INIT`.  

**What it does:** Publishes datasets.

1. Publish analysis dataset

    ```text title="Prompt – upload dataset"
    Initialize dataset metadata for./my-sales-analysis/.
    Files: cleaned_pipeline.csv, features.csv, readme.md.
    Title: "Sales Pipeline Analysis 2026", description: "Cleaned CRM data..."
    Create dataset, check status, publish version 1.
    ```

2. Update existing dataset

    ```text title="Prompt – version bump"
    Create new version for "my-sales-analysis" dataset.
    Add quarterly_data_q1.csv, update readme with Q1 metrics.
    Push version 2, verify processing complete.
    ```

---

## 3. Competitions and submissions 

### Participate in challenges

**Capabilities:** `SUBMIT_COMPETITION_ENTRY`, `DOWNLOAD_COMPETITION_DATA_FILES`.  

**What it does:** Competes and submits.

1. House prices submission

```text title="Prompt – model submission"
Download "House Prices" competition data.
Submit./predictions.csv (got blob token from upload).
Leaderboard position target: top 20%.
```

---

## 4. Kernels and notebooks 

### Code and outputs

**Capabilities:** `DOWNLOAD_KERNEL_OUTPUT`, `GET_KERNEL_STATUS`, `KAGGLE_KERNEL_INIT`.  

**What it does:** Manages notebooks.

1. Kernel results

```text title="Prompt – notebook output"
Download output from kernel "titanic‑eda‑v3" by username.
Save models/plots to./titanic‑kernels/.
Check status if running.
```

---

## 5. API configuration 

### Setup and management

**Capabilities:** `INITIALIZE_KAGGLE_CONFIGURATION`, `SET_KAGGLE_CONFIGURATION`, `VIEW_KAGGLE_CONFIGURATION`.  

**What it does:** Configures access.

1. API setup

```text title="Prompt – configure Kaggle"
Initialize Kaggle config (~/.kaggle/kaggle.json).
Set competition_download_path =./competitions/.
View current config, verify API token loaded.
```

---

## Best practices for Kaggle 

- **API token secure.** Use kaggle.json, never commit.  
- **Metadata first.** Init dataset/kernel before upload.  
- **Version everything.** Track changes in datasets/kernels.  
- **Combine with notebooks.** Kaggle data → Colab analysis → GitHub.

To connect Kaggle, open **Settings → Connections → Kaggle** (kaggle.json upload or env vars). Then run prompts directly from Chat Mode.