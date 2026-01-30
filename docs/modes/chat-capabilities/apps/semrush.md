# Semrush in Chat Mode

Connecting Semrush lets you **perform keyword research, competitor analysis, backlink audits, and SEO audits directly from chat**, accessing comprehensive regional databases for SEO/PPC insights.

Use it for content strategy, link building, ad optimization, and performance tracking.

---

## What Semrush can do 

Once Semrush is connected (Settings → Connections → Semrush), you can:

- Keyword overview/difficulty, organic/paid positions.
- Backlinks, anchors, referring domains/IPs overview.
- Competitor comparison, ad copies/history.
- Batch analysis, historical data, categories.

---

## 1. Keyword research 

### Volume and difficulty

**Capabilities:** `SEMRUSH_KEYWORD_OVERVIEW_ONE_DATABASE`, `SEMRUSH_KEYWORD_DIFFICULTY`, `SEMRUSH_BATCH_KEYWORD_OVERVIEW`.  

**What it does:** Assesses keyword potential.

1. Keyword analysis

    ```text title="Prompt – keyword metrics"
    Get overview for "SEO tools" in US database: volume, CPC, KD.
    Batch check 10 keywords: "best SEO software", "keyword research tool" etc.
    List top opportunities (volume >1000, KD <50).
    ```

2. Related questions

    ```text title="Prompt – content ideas"
    Get phrase questions for "machine learning tutorial".
    Filter for long-tail variants.
    ```

---

## 2. Competitor analysis 

### Organic and paid

**Capabilities:** `SEMRUSH_COMPETITORS_IN_ORGANIC_SEARCH`, `SEMRUSH_DOMAIN_ORGANIC_SEARCH_KEYWORDS`, `SEMRUSH_DOMAIN_VS_DOMAIN`.  

**What it does:** Benchmarks rivals.

1. Organic competitors

    ```text title="Prompt – traffic share"
    Get organic competitors for example.com.
    Pull top keywords for #1 competitor.
    Compare example.com vs competitor.com (organic).
    ```

2. Paid landscape

    ```text title="Prompt – PPC rivals"
    Get paid search competitors for "SEO agency".
    Domain paid keywords for top rival.
    ```

---

## 3. Backlink profile 

### Links and domains

**Capabilities:** `SEMRUSH_BACKLINKS`, `SEMRUSH_REFERRING_DOMAINS`, `SEMRUSH_BACKLINKS_OVERVIEW`.  

**What it does:** Audits link health.

1. Full backlinks

    ```text title="Prompt – link audit"
    Get backlinks overview for example.com.
    Pull 1000 referring domains, filter dofollow.
    CSV: domain, anchor, authority score.
    ```

2. Anchor text

    ```text title="Prompt – anchor distribution"
    Get anchors for example.com, top 50.
    Batch compare 3 domains.
    ```

---

## 4. Advertising insights 

### Ads and copies

**Capabilities:** `SEMRUSH_ADS_COPIES`, `SEMRUSH_DOMAIN_AD_HISTORY`, `SEMRUSH_PLA_COPIES`.  

**What it does:** Reverse-engineers campaigns.

1. Ad copy spy

```text title="Prompt – competitor ads"
Get ad copies for rival.com (US).
Domain ad history last 12 months.
PLA copies for ecommerce rival.
```

---

## 5. Site audits and content 

### Categories and pages

**Capabilities:** `SEMRUSH_DOMAIN_ORGANIC_PAGES`, `SEMRUSH_CATEGORIES`, `SEMRUSH_INDEXED_PAGES`.  

**What it does:** Content gap analysis.

1. Ranking pages

```text title="Prompt – content audit"
Get organic pages for example.com.
Categories profile, top topics.
Indexed pages count.
```

---

## Best practices for Semrush 

- **Database specific.** US/EU/UK etc. for accuracy.  
- **Date format.** YYYYMM15 for historical.  
- **Limits aware.** display_limit/offset for large reports.  
- **Batch wisely.** Up to 100 keywords/domains.

To connect Semrush, open **Settings → Connections → Semrush** (API key auth). Then run prompts directly from Chat Mode.