# LinkedIn in Chat Mode

Connecting LinkedIn lets you **post updates, engage connections, and manage your professional presence directly from chat**, building your network and content strategy conversationally.

Use it for content publishing, connection outreach, profile optimization, and engagement tracking.

---

## What LinkedIn can do

Once LinkedIn is connected (Settings → Connections → LinkedIn), you can:

- Post text, articles, images, carousels, and videos to your feed.
- Send connection requests with personalized notes.
- Comment, react, and share existing posts.
- Search profiles, companies, and content.
- Update profile sections (headline, about, experience).
- Manage messaging and notifications.

!!! note
    Actions respect LinkedIn rate limits and your account permissions (personal vs company page).

---

## 1. Content publishing

### Post updates and articles

**Capabilities:** Share text posts, images, carousels, videos, articles to feed.  

**What it does:** Creates native LinkedIn content with hashtags and visibility controls.

1. Professional announcement

    ```text title="Prompt – share achievement"
    Post to my LinkedIn feed:

    "Thrilled to share that our team just closed our biggest Q1 deal! 🎉

    Key wins:
    -  $450K ARR expansion with enterprise client
    -  Deployed custom automation workflows
    -  40% faster ops for their team

    Grateful for the amazing team making this possible.

    #Sales #SaaS #Automation"

    Add image if available, target connections + followers.
    ```

2. Carousel post

    ```text title="Prompt – slide deck share"
    Create LinkedIn carousel post from these 5 slides about "5 CRM Hacks":
    1. Slide 1: Title + hook
    2. Slide 2–4: Each hack with bullet points
    3. Slide 5: CTA + contact info

    Hashtags: #CRM #SalesTips, visibility: anyone.
    ```

---

## 2. Network building

### Connection requests and messaging

**Capabilities:** Send personalized connection requests, InMail, follow companies.  

**What it does:** Grows your network with targeted outreach.

1. Strategic connection

    ```text title="Prompt – connect with VP"
    Find Jordan Lee (VP Operations at Peak Performance) and send
    connection request:

    "Hi Jordan, enjoyed our ops automation discussion last week.
    Would love to stay connected as we both tackle workflow challenges!

    Best,
    [Your Name]"

    If already connected, send DM instead with meeting recap.
    ```

2. Company following

    ```text title="Prompt – follow targets"
    Follow these companies on LinkedIn: Stripe, HubSpot, Apollo.io,
    Notion, Supabase. For each, find and follow their Head of Sales.
    Share a post in comments: "Excited to follow your growth!"
    ```

---

## 3. Engagement and amplification

### React, comment, share

**Capabilities:** Like/react, comment on posts, share/repurpose content.  

**What it does:** Boosts visibility through authentic engagement.

1. Strategic commenting

    ```text title="Prompt – engage influencers"
    Find 5 recent posts from sales leaders (mentioning "pipeline" or "CRM")
    with 50–500 likes. Add thoughtful comments like:
    "Love this – we saw 30% pipeline velocity using similar automation."
    Include relevant emoji and hashtag.
    ```

2. Curate content

    ```text title="Prompt – weekly roundup"
    Find 3 great sales posts from last week. Create roundup post:
    "3 sales insights from last week:
    1. [Link + quote]
    2. [Link + quote] 
    3. [Link + quote]

    What did you learn this week?"

    Tag original authors.
    ```

---

## 4. Profile optimization

### Update professional presence

**Capabilities:** Edit headline, about section, experience, skills.  

**What it does:** Keeps your profile current and keyword‑optimized.

1. Headline refresh

    ```text title="Prompt – optimize headline"
    Update my LinkedIn headline to:
    "Head of Revenue Ops | Helping SaaS teams 2x pipeline velocity | 
    Automation + CRM expert | ex-HubSpot"

    Keep it under 220 characters, add emojis strategically.
    ```

2. Experience update

    ```text title="Prompt – add achievement"
    Add to my current role experience:
    -  "Q1 2026: Closed $2.3M pipeline, 145% of quota"
    -  "Built custom automation saving 20h/week across team"

    Format as bullet achievements with metrics.
    ```

---

## 5. Research and discovery

### Profile and company search

**Capabilities:** Search people/companies, view profiles/posts.  

**What it does:** Surfaces prospects and intelligence.

1. Account intelligence

```text title="Prompt – company deep dive"
Research "Peak Performance Consulting" on LinkedIn:
-  Key employees (titles, tenure)
-  Recent posts/activity
-  Hiring trends
-  Company updates

Summarize top 3 hiring signals or expansion clues.
```

---

## Best practices for LinkedIn

- **Personalize outreach.** Reference shared context in connection notes.  
- **Engage before pitching.** Comment meaningfully 2–3x before DMs.  
- **Post consistently.** 3–5 times/week with varied formats.  
- **Combine with CRM.** Flow: LinkedIn research → Apollo enrich → HubSpot deal → sequence.

To connect LinkedIn, open **Settings → Connections → LinkedIn** and authorize via OAuth. Then run prompts directly from Chat Mode.