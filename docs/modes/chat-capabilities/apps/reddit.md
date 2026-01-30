# Reddit in Chat Mode

Connecting Reddit lets you **post content, comment, search subreddits/posts, manage flair, and monitor communities directly from chat**, automating social engagement.

Use it for community building, content discovery, sentiment analysis, and viral campaigns.

---

## What Reddit can do 

Once Reddit is connected (Settings → Connections → Reddit), you can:

- Create/edit/delete posts and comments.
- Search subreddits/posts/users, retrieve listings.
- Get top/hot/random posts, rules, flairs, user info.
- Check usernames, preferences, subreddit metadata.

---

## 1. Content creation 

### Posts and comments

**Capabilities:** `REDDIT_CREATE_REDDIT_POST`, `REDDIT_POST_REDDIT_COMMENT`, `REDDIT_EDIT_REDDIT_COMMENT_OR_POST`.  

**What it does:** Publishes to subreddits.

1. New post

    ```text title="Prompt – publish article"
    Create post in r/MachineLearning:
    Title: "Scaling ML Pipelines: Lessons from Production"
    Type: self, body: 800-word article + key takeaways.
    Flair: "Project", nsfw: false.

    Share link after posting.
    ```

2. Comment thread

    ```text title="Prompt – engage discussion"
    Post comment on post t3_abc123 (article ID):
    "Excellent overview! We achieved 3x speedup with similar batching."
    Edit if typo, add "Follow-up questions?".
    ```

---

## 2. Content discovery 

### Search and listings

**Capabilities:** `REDDIT_GET`, `REDDIT_GET_R_TOP`, `REDDIT_SEARCH_ACROSS_SUBREDDITS`, `REDDIT_GET_RANDOM`.  

**What it does:** Finds trending content.

1. Top posts

    ```text title="Prompt – trending research"
    Get top posts r/MachineLearning past week, limit 20.
    Extract titles, scores, comments count.
    Filter score >100 for summary.
    ```

2. Subreddit search

    ```text title="Prompt – find communities"
    Search subreddits: "data engineering pipelines".
    List top 5 with subscribers, description.
    Get rules for r/dataengineering.
    ```

---

## 3. Comments and replies 

### Thread analysis

**Capabilities:** `RETRIEVE_POST_COMMENTS`, `RETRIEVE_SPECIFIC_COMMENT`, `REDDIT_DELETE_REDDIT_COMMENT`.  

**What it does:** Monitors discussions.

1. Post comments

```text title="Prompt – analyze thread"
Retrieve comments for post t3_xyz789.
Summarize top-level sentiments, extract questions.
Delete my spam comment ckz456.
```

---

## 4. Moderation and management 

### Flair and rules

**Capabilities:** `GET_R_SUBREDDIT_LINK_FLAIR_V2`, `GET_SUBREDDIT_RULES`, `REDDIT_DELETE_REDDIT_POST`.  

**What it does:** Maintains content.

1. Flair check

```text title="Prompt – post prep"
Get link flairs for r/science.
Check rules before posting.
Delete my post t3_old123 if low engagement.
```

---

## 5. User and account 

### Profiles and prefs

**Capabilities:** `GET_REDDIT_USER_ABOUT`, `GET_ME_PREFS`, `GET_USERNAME_AVAILABLE`, `GET_USER_FLAIR`.  

**What it does:** User insights.

1. Profile lookup

```text title="Prompt – influencer research"
Get info for u/MLResearcherPro: karma, gold status.
Check username "DataPipelinesExpert" available.
List my flairs in r/MachineLearning.
```

---

## Best practices for Reddit 

- **Rules first.** Check `GET_SUBREDDIT_RULES` before posting.  
- **Flair required.** Use available templates.  
- **Engage genuinely.** Comment value, not spam.  
- **Paginate results.** Handle large listings.

To connect Reddit, open **Settings → Connections → Reddit** (OAuth app setup). Then run prompts directly from Chat Mode.