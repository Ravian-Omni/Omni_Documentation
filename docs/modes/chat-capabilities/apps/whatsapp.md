# WhatsApp in Chat Mode

Connecting WhatsApp lets you **send messages, manage broadcasts, and automate customer conversations directly from chat**, scaling 1:1 communication.

Use it for customer support, sales follow‑ups, appointment reminders, and team coordination.

---

## What WhatsApp can do

Once WhatsApp is connected (Settings → Connections → WhatsApp), you can:

- Send text, images, documents, audio, location messages.
- Create/manage broadcast lists and labels.
- Send templated messages (pre‑approved for Business API).
- Read message history and contact details.
- Manage groups and participants.

!!! warning
    WhatsApp Business API required for automation. Comply with 24h messaging window.

---

## 1. 1:1 customer conversations

### Send messages and media

**Capabilities:** Text, images, documents, audio, video, location, contacts.  

**What it does:** Delivers rich messages to individual contacts.

1. Sales follow‑up

    ```text title="Prompt – customer follow‑up"
    Send WhatsApp message to +1-555-0123 (Jordan from Peak Performance):

    "Hi Jordan! 👋

    Quick follow‑up on our ops automation discussion:

    ✅ Demo recording ready
    ✅ Custom pricing prepared  
    ✅ Onboarding timeline outlined

    [Attach proposal.pdf]

    Best time for 15min review call this week? 📅"

    ```

2. Order confirmation

    ```text title="Prompt – transactional message"
    Send to +1-555-9876 (Sarah Chen):

    "✅ Order #ORD‑123 confirmed!

    📦 Wireless Headphones Pro (Matte Black)
    💰 $129.99
    🚚 Ships tomorrow, arrives by Feb 2
    📱 Track: [tracking link]

    Questions? Reply here!"

    Attach order summary image.
    ```

---

## 2. Broadcast and templates

### Scale messaging with templates

**Capabilities:** Pre‑approved message templates, broadcast lists.  

**What it does:** Reaches many contacts compliantly.

1. Abandoned cart recovery

    ```text title="Prompt – cart reminder"
    Send WhatsApp template "abandoned_cart" to 50 customers
    who abandoned >$100 carts in last 24h:

    "Hi [FirstName]! Your cart is waiting 😊

    [Product image] Wireless Headphones Pro
    Offer expires in 24h: 10% off code SAVE10

    Complete checkout? 👆 [link]"

    Personalize with name/product.
    ```

2. Appointment reminder

    ```text title="Prompt – calendar sync"
    Send "appointment_reminder" template to tomorrow's bookings:

    "Reminder: Your consultation with [Business Name]
    📅 [Date] [Time]
    📍 [Location/Link]

    Cancel? Reply STOP. Questions? We're here!"

    ```

---

## 3. Team coordination

### Group messaging

**Capabilities:** Send to groups, manage participants.  

**What it does:** Coordinates internal teams.

1. Team standup broadcast

```text title="Prompt – daily team update"
Send to "Sales Team" WhatsApp group:

"📊 Daily Pipeline Update – Jan 30

🔥 New: 3 qualified demos booked
💰 Pipeline: $2.1M (+12% WoW)
⚠️ Blockers: 2 proposals pending legal

Wins today:
-  Sarah C. → enterprise POC approved
-  Jordan L. → budget confirmed

Questions? @mention me."

```

---

## 4. Customer support automation

### Ticket escalation and FAQs

**Capabilities:** Read incoming messages, send templated responses.  

**What it does:** Handles common support flows.

1. FAQ response

```text title="Prompt – auto‑reply support"
Customer +1-555‑3456 asked "How do I reset password?"

Reply: "🔑 Password Reset:

1️⃣ [Login link]
2️⃣ 'Forgot Password'
3️⃣ Check email inbox + spam
4️⃣ Follow reset link (expires 1h)

Still stuck? Reply with screenshot."

Escalate to human if no reply in 30min.
```

---

## 5. Business metrics

### Message analytics

**Capabilities:** Track delivery/read rates, response times.  

**What it does:** Optimizes messaging strategy.

1. Campaign performance

```text title="Prompt – messaging report"
Show WhatsApp metrics last 7 days:
-  Messages sent/delivered/read
-  Response rate by template
-  Top performing send times
-  Customer segments by engagement

Best template for cart recovery?
```

---

## Best practices for WhatsApp

- **Personal > Generic.** Use names/products in templates.  
- **24h window.** Free messaging only within 24h of customer message.  
- **Rich media.** Images/documents boost engagement 3x.  
- **Combine flows.** Flow: Shopify abandoned cart → WhatsApp reminder → HubSpot ticket.

To connect WhatsApp, open **Settings → Connections → WhatsApp Business API** (phone number verification required). Then run prompts directly from Chat Mode.