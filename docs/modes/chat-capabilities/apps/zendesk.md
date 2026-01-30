# Zendesk in Chat Mode

Connecting Zendesk lets you **create/manage tickets, organizations, users, and replies directly from chat**, streamlining customer support workflows with ticketing and helpdesk automation.

Use it for support queues, customer onboarding, ticket triage, and org grouping.

---

## What Zendesk can do 

Once Zendesk is connected (Settings → Connections → Zendesk), you can:

- Create/update/delete tickets, organizations, users.
- List/search tickets/users/orgs, count orgs.
- Reply to tickets, get details/status.
- Bulk delete orgs, get about me.

---

## 1. Ticket management 

### Create and update tickets

**Capabilities:** `ZENDESK_CREATE_ZENDESK_TICKET`, `ZENDESK_UPDATE_ZENDESK_TICKET`, `ZENDESK_DELETE_ZENDESK_TICKET`.  

**What it does:** Handles support requests.

1. New support ticket

    ```text title="Prompt – ticket creation"
    Create Zendesk ticket:
    Subject: "Billing Issue - Overcharge Jan 2026"
    Requester email: customer@company.com
    Priority: high, type: question
    Description: "Double charged $500, invoice #12345".
    ```

2. Ticket update

    ```text title="Prompt – status change"
    Get ticket 123456, update status to "solved".
    Set priority urgent, assignee support@team.com.
    Delete if spam confirmed.
    ```

---

## 2. Ticket listing and search 

### Monitor queues

**Capabilities:** `ZENDESK_LIST_ZENDESK_TICKETS`, `ZENDESK_GET_ZENDESK_TICKET_BY_ID`, `ZENDESK_REPLY_ZENDESK_TICKET`.  

**What it does:** Views and responds.

1. Open tickets

```text title="Prompt – queue overview"
List open tickets last 7 days, limit 50.
Filter assignee:me, status:pending.
Reply to ticket 789012: "Fixed, login reset sent.".
```

---

## 3. Organizations 

### Company grouping

**Capabilities:** `ZENDESK_CREATE_ZENDESK_ORGANIZATION`, `ZENDESK_GET_ALL_ZENDESK_ORGANIZATIONS`, `ZENDESK_UPDATE_ZENDESK_ORGANIZATION`, `ZENDESK_COUNT_ZENDESK_ORGANIZATIONS`.  

**What it does:** Manages customer orgs.

1. Client org setup

```text title="Prompt – org creation"
Count orgs, create "Tech Corp Ltd" domain techcorp.com.
Get org 456, update notes "VIP client".
Bulk delete test orgs 999-1005.
```

---

## 4. Users 

### Customer/agent accounts

**Capabilities:** `ZENDESK_CREATE_ZENDESK_USER`, `ZENDESK_SEARCH_ZENDESK_USERS`, `ZENDESK_GET_ABOUT_ME`.  

**What it does:** Onboards users.

1. User search/add

```text title="Prompt – user management"
Search users email: john@techcorp.com.
Create user "Jane Doe" verified:true, org_id:456.
Get about me profile.
```

---

## 5. Bulk and advanced 

### Cleanup operations

**Capabilities:** `ZENDESK_DESTROY_MANY_ORGANIZATIONS`, `ZENDESK_GET_ZENDESK_ORGANIZATION`.  

**What it does:** Scales ops.

1. Org cleanup

```text title="Prompt – maintenance"
Get org "Inactive Co", bulk destroy orgs. [composio](https://composio.dev/toolkits/one_drive/framework/mastra-ai)
List all orgs, count total.
```

---

## Best practices for Zendesk 

- **IDs required.** Get ticket/org/user ID first.  
- **Pagination.** Use for large lists.  
- **Requester verify.** Search users before create.  
- **Combine with email.** Zendesk tickets → Slack alerts.

To connect Zendesk, open **Settings → Connections → Zendesk** (OAuth2 auth config). Then run prompts directly from Chat Mode.