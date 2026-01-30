# Twitter (X) in Chat Mode

Connecting Twitter lets you **post threads, engage conversations, and monitor trends directly from chat**, amplifying your voice and staying connected to your audience.

Use it for real-time updates, audience engagement, trend monitoring, and automated posting.

---

## What Twitter can do

Once Twitter is connected (Settings → Connections → Twitter), you can:

- Post tweets, threads, images, videos, polls.
- Reply, retweet, like, bookmark content.
- Search tweets/users/hashtags, monitor keywords.
- Manage lists, mute/block accounts.
- Analyze your tweets and audience.

!!! note
    Actions respect Twitter API rate limits and your account verification status.

---

## 1. Content creation and threads

### Post tweets and threads

**Capabilities:** Create single tweets, threads, media tweets, polls.  

**What it does:** Publishes native Twitter content with optimal formatting.

1. Announcement thread

    ```text title="Prompt – launch thread"
    Post 4‑tweet thread announcing new feature:

    Tweet 1: "🚀 Just shipped automated pipeline velocity tool! 2x your sales cycle speed."

    Tweet 2: "Key features:
    -  AI‑driven next‑best actions
    -  Cross‑CRM workflow sync
    -  Real‑time engagement scoring"

    Tweet 3: "Beta users seeing 40% faster deal cycles already."

    Tweet 4: "Try it free → [link] 
    Who's speeding up their pipeline? 👇 #SaaS #Sales"

    Add relevant image to Tweet 1.
    ```

2. Quick poll

    ```text title="Prompt – audience poll"
    Tweet: "Sales teams: What's your biggest pipeline bottleneck?
    A) Lead qualification (1h)
    B) Demo scheduling (2h) 
    C) Proposal delays (3h)
    D) Contract negotiation (4h)

    Vote + comment! #Sales"

    4 options, 24h duration.
    ```

---

## 2. Engagement and conversation

### Reply, retweet, like

**Capabilities:** Reply to tweets, retweet/quote, like/bookmark, search replies.  

**What it does:** Builds relationships through authentic interaction.

1. Strategic replies

    ```text title="Prompt – engage trending tweet"
    Find 3 recent tweets mentioning "#SalesPipeline" with 100–1K likes.
    Reply to each with value‑add comment:
    "This + workflow automation = 2x velocity 🚀"

    Include link to relevant resource, use thread emoji.
    ```

2. Curate retweets

    ```text title="Prompt – weekly roundup"
    Search tweets from sales influencers last 7 days containing "pipeline".
    Quote retweet top 3 with commentary:
    "Gold from [author]: [key insight] 
    Saved this for Monday execution 👏"

    Tag original authors.
    ```

---

## 3. Research and monitoring

### Search and track conversations

**Capabilities:** Keyword/hashtag/user search, advanced filters (date, engagement, location).  

**What it does:** Surfaces trends, mentions, and opportunities.

1. Brand monitoring

    ```text title="Prompt – mention tracking"
    Search tweets mentioning "[yourcompany]" or "yourproduct" last 24h.
    Show:
    -  Sentiment (positive/neutral/negative)
    -  Most engaged mentions
    -  Influencer conversations

    Suggest 3 replies to amplify positive ones.
    ```

2. Competitor intel

    ```text title="Prompt – competitive search"
    Search tweets: "competitorX OR competitorY pipeline" from verified users,
    last 30 days, min 50 likes.
    Summarize 5 emerging pain points customers mention.
    ```

---

## 4. Profile and audience management

### Follow, mute, lists

**Capabilities:** Follow/unfollow, create/manage lists, mute keywords/accounts.  

**What it does:** Curates your feed and grows followers.

1. Targeted following

    ```text title="Prompt – network expansion"
    Search "VP Sales" at SaaS companies (50–500 employees), US.
    Follow top 20 active posters (tweeting weekly).
    Add to private list "SaaS Sales Leaders".
    Like their 3 most recent tweets.
    ```

2. Content curation list

    ```text title="Prompt – create watchlist"
    Create Twitter List "SaaS Founders to Watch" (private).
    Add: @patel, @naval, @sahilbloom, @levelsio.
    Tweet: "Curating SaaS founder insights → [list link]"
    ```

---

## 5. Analytics and scheduling

### Performance tracking

**Capabilities:** View tweet analytics, schedule tweets.  

**What it does:** Measures impact and plans content calendar.

1. Content performance

```text title="Prompt – tweet analysis"
Show my last 10 tweets: impressions, engagements, link clicks.
Which hashtags drove most reach? Best posting time (day/hour)?
Suggest format for next week's content based on winners.
```

---

## Best practices for Twitter

- **Thread for depth.** 3–7 tweets max, strong hook first tweet.  
- **Engage daily.** 15–30min authentic interaction > broadcasting.  
- **Hashtags strategically.** 1–3 relevant, searchable ones.  
- **Combine with tools.** Flow: Apollo research → Twitter engage → HubSpot log → Notion notes.

To connect Twitter, open **Settings → Connections → Twitter** and authorize via OAuth. Then run prompts directly from Chat Mode.