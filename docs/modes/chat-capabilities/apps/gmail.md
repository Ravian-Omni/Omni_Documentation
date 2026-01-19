# Gmail in Chat Mode

Connecting Gmail lets Ravian **read, draft, label, and send email directly from the chat**, with your approval on every outbound action.

Use it to clear your inbox, run small campaigns, manage labels, and keep communication in sync with the rest of your workflows.

---

## What Ravian can do with Gmail

Once Gmail is connected (Settings → Connections → Gmail), Ravian can:

- Draft and send emails and replies.
- Create, update, and delete drafts.
- Apply, remove, and manage labels.
- Search, fetch, and summarize messages and threads.
- Move messages to trash or permanently delete them.
- Work with contacts and people data for personalization.

!!! warning
    Ravian always asks for approval before **sending** or **deleting** emails. You stay in control.

---

## 1. Drafting and sending emails

### Create a fresh email

**Capabilities:** `GMAIL_CREATE_EMAIL_DRAFT`, `GMAIL_SEND_EMAIL`

**What it does:** Create drafts and send messages with subject, body, recipients, and attachments.

**Example prompts:**

1. Create a draft

    ```text title="Prompt – create a draft"
    Draft an email from my Gmail to hr@acme.com with subject
    "Ravian AI Documentation Update" and a short summary of the new docs.
    Don't send yet, just save it as a draft.
    ```

2. Send the draft

    ```text title="Prompt – send the draft"
    Find the draft you just created about the Ravian AI documentation update
    and send it to hr@acme.com after fixing any obvious grammar issues.
    Ask for my approval before sending.
    ```

---

### Reply or forward threads 
**capabilities** `GMAIL_REPLY_TO_THREAD, GMAIL_FORWARD_MESSAGE`

**What it does:** Reply in existing threads or forward messages to new recipients.

1. Reply in a thread

    ```text title="Prompt – reply in a thread"
    Reply to the latest email in the thread with subject
    "Ravian onboarding" and say:

    "Thanks for the update. The docs structure looks good. I'll share
    the first draft by Friday EOD."

    Keep the tone professional and friendly, and queue the reply for my approval.
    ```

2. Forward

    ```text title="Prompt – forward"
    Find the email from support@vendor.com about "billing update"
    and forward it to finance-team@mycompany.com with a short note
    on top asking them to review the changes.
    ```

---

## 2. Inbox triage and search

### Fetch and summarize emails
**capabilities** `GMAIL_FETCH_EMAILS, GMAIL_FETCH_MESSAGE_BY_THREAD_ID`

**What it does:** Search and list emails by query, label, or time, then summarize.

1. Summarize today's inbox

    ```text title="Prompt – summarize today's inbox"
    Scan my unread emails from today that mention "Ravian" or "documentation".
    Group them by topic and summarize each group in 2–3 bullets.
    Propose replies where a response is needed.
    ```

2. Inspect one thread

    ```text title="Prompt – inspect one thread"
    Open the full thread with subject containing "Naukri job application"
    and summarize the conversation so far, highlighting any pending actions.
    ```

---

### Smart cleanup
**capabilities** `GMAIL_BATCH_DELETE_MESSAGES, GMAIL_MOVE_TO_TRASH`

**What it does:** Move messages to trash or permanently delete in bulk.

1. Move to trash safely

    ```text title="Prompt – move to trash safely"
    Identify promotional emails from the last 30 days that I have never opened
    and move them to Trash. Do not touch anything from my company domain
    or recruitment platforms.
    Show me a count before you act and ask for confirmation.
    ```

2. Hard delete

    ```text title="Prompt – hard delete (use carefully)"
    Find all unread emails older than 1 year in the Promotions tab and
    permanently delete them after confirming with me.
    ```

!!! warning
    Use destructive prompts sparingly. Always require a confirmation step before bulk deletes.

---

## 3. Labels and organization

### Manage labels
**capabilities** `GMAIL_CREATE_LABEL, GMAIL_ADD_LABEL_TO_EMAIL, GMAIL_BATCH_MODIFY_MESSAGES`

**What it does:** Create labels and apply/remove them on messages or threads.

1. Create a label

    ```text title="Prompt – create a label"
    Create a Gmail label called "Ravian Docs" if it does not already exist.
    ```

2. Label important messages
    ```text title="Prompt – label important messages"
    Find emails from my manager in the last 14 days that mention "documentation"
    or "release notes", apply the label "Ravian Docs", and mark them as important.
    Give me a short list of what you labeled.
    ```

3. Bulk label

    ```text title="Prompt – bulk label"
    For all emails from github.com in the last month, add the label "GitHub Notifications"
    and mark them as read, but leave anything with "security" in the subject unread.
    ```

---

## 4. Draft management

### List, update, and delete drafts
**capabilities** `GMAIL_LIST_DRAFTS, GMAIL_DELETE_DRAFT, GMAIL_SEND_DRAFT`

**What it does:** Work with existing drafts so you can refine and send them from chat.

1. List drafts

    ```text title="Prompt – list drafts"
    List my Gmail drafts created in the last 7 days and summarize each in one line
    (subject + first sentence).
    ```

2. Improve and send a draft
    ```text title="Prompt – improve and send a draft"
    Take the draft about "Ravian AI job automation demo" created yesterday,
    make the writing clearer and more concise, then send it to the original recipients
    after I approve the final version.
    ```

3. Clean up drafts

    ```text title="Prompt – clean up drafts"
    Find drafts older than 3 months that were never sent and propose which ones
    can be deleted. After my confirmation, delete the ones I mark as safe to remove.
    ```

---

## 5. Contacts and personalization

### Use contacts / people data
**capabilities** `GMAIL_GET_CONTACTS, GMAIL_GET_PEOPLE, GMAIL_SEARCH_PEOPLE`

**What it does:** Look up people in your Google contacts to personalize messages.

1. Personalized outreach

    ```text title="Prompt – personalized outreach"
    Using my Google contacts, find up to 5 people with data roles or AI titles.
    Draft a short, personalized email to each inviting them to try the latest
    Ravian AI beta. Include one sentence referencing how we know each other
    if that information is available in contacts.
    Queue all emails for my approval.
    ```

2. Prepare follow-ups

    ```text title="Prompt – prepare follow-ups"
    Search my contacts for people at 'acme.com' and prepare a list of names,
    roles, and emails. Draft a single follow-up template that I can customize
    for each person.
    ```

---

## 6. Settings insights (IMAP/POP/vacation/profile)

### Check profile and vacation status
**capabilities** `GMAIL_GET_PROFILE, GMAIL_GET_VACATION_SETTINGS`

**What it does:** Read metadata about your account and auto‑reply configuration.

1. Check vacation responder

    ```text title="Prompt – check vacation responder"
    Tell me whether my Gmail vacation responder is currently on.
    If it is enabled, summarize the current auto-reply message and dates.
    ```

2. Profile sanity check

    ```text title="Prompt – profile sanity check"
    Show my Gmail profile info (primary address, total messages, and threads)
    and let me know if anything looks unusual compared to last month.
    ```

---

## Best practices for Gmail with Ravian

- **Always approve sends and deletes.** Make it a habit to require confirmation in your prompts.  
- **Be explicit about scope.** Mention time ranges, labels, and domains to avoid touching the wrong emails.  
- **Use labels as building blocks.** Ask Ravian to apply labels first, then act on labeled sets (easier to reason about).  
- **Combine with other apps.** For example: summarize a Notion page → draft Gmail update → schedule follow‑up in Calendar.

To connect Gmail, open **Settings → Connections → Gmail** in the Ravian app and complete the sign‑in flow. Once connected, all of the prompts above can be run directly from Chat Mode.