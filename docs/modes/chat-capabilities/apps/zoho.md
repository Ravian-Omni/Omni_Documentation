# Zoho in Chat Mode

Connecting Zoho lets you **manage CRM leads/deals, send emails, handle accounting invoices/contacts, and inventory directly from chat**, integrating CRM, Mail, Books, and more via unified API.

Use it for sales pipelines, billing automation, customer communication, and financial tracking.

---

## What Zoho can do 

Once Zoho is connected (Settings → Connections → Zoho), you can:

- CRM: Create/update leads, contacts, deals, notes.
- Mail: Send emails, list messages/groups, domain ops.
- Books: Invoices, estimates, sales orders, contacts, payments.
- Inventory: Items, orders (via related kits).

---

## 1. CRM operations 

### Leads and deals

**Capabilities:** CRM tools like create lead/contact/deal.  

**What it does:** Manages sales funnel.

1. New client onboarding

    ```text title="Prompt – sales pipeline"
    Create lead "Tech Startup Inc", assign to sales rep.
    Convert to contact + deal "Annual Subscription" $10K.
    Add note "Discussed features Jan 30".
    ```

2. Pipeline update

    ```text title="Prompt – deal progress"
    List open deals >$5K, update "Tech Startup" stage to "Proposal Sent".
    Email proposal attachment via Zoho Mail.
    ```

---

## 2. Email and communication

### Zoho Mail

**Capabilities:** `ZOHO_MAIL_DOMAIN_OPERATIONS`, send messages, groups.  

**What it does:** Business email.

1. Client follow-up

```text title="Prompt – bulk emails"
Send email to 50 contacts: "Q1 Service Update", attach newsletter.pdf.
List inbox unread from support@domain.com.
Delete old group "Newsletter Subscribers".
```

---

## 3. Accounting and invoicing 

### Zoho Books

**Capabilities:** `ZOHO_BOOKS_CREATE_INVOICE`, `ZOHO_BOOKS_LIST_CONTACTS`, `ZOHO_BOOKS_EMAIL_INVOICE`, `ZOHO_BOOKS_CREATE_CONTACT`.  

**What it does:** Billing workflows.

1. Invoice generation

```text title="Prompt – monthly billing"
Create invoice for "Tech Startup Inc": $2,500 services, items: Consulting (20h), Hosting.
Email invoice, mark sent.
List unpaid invoices this month.
```

2. Contact billing

```text title="Prompt – vendor setup"
Create contact "Freelance Designer", mark active.
List currencies, create sales order for design work.
```

---

## 4. Inventory and orders

### Stock management

**Capabilities:** Inventory create/list items, orders.  

**What it does:** Tracks products.

1. Product catalog

```text title="Prompt – item management"
Create item "Premium Widget" SKU PW-001, price $49.
List sales orders pending shipment.
Update stock for "Basic Widget".
```

---

## 5. Reporting and lists 

### Overviews

**Capabilities:** `ZOHO_BOOKS_LIST_SALES_ORDERS`, `ZOHO_BOOKS_LIST_USERS`, `ZOHO_BOOKS_LIST_INVOICE_PAYMENTS`.  

**What it does:** Dashboards.

1. Financial summary

```text title="Prompt – reports"
List invoice payments Q1 2026.
List users/roles.
Get estimates for active clients.
```

---

## Best practices for Zoho 

- **Unified auth.** One OAuth covers CRM/Mail/Books.  
- **Workflows chain.** CRM deal → Books invoice → Mail send.  
- **Bulk limits.** Paginate large lists.  
- **Combine kits.** Zoho CRM + Books for full finance.

To connect Zoho, open **Settings → Connections → Zoho** (OAuth for domain). Then run prompts directly from Chat Mode.