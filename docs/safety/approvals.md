# Human Approvals

Ravian AI is designed to be **autonomous but supervised**, giving you the final say before it performs sensitive actions such as sending emails, submitting forms, or accessing protected systems.

Human approvals let you balance speed with control, especially in enterprise or high‑risk environments.

---

## Why approvals matter

Autonomous agents can execute long workflows, which may include steps that:

- Communicate with external parties (email, chat, messaging).
- Modify or delete important data and files.
- Trigger financial or legal consequences, such as purchases or contract changes.

Ravian’s approval system ensures that you remain in control of these high‑impact decisions.

!!! note
    You decide which actions require approval; routine low‑risk operations can still run fully autonomously.

---

## How approvals work

When a workflow reaches a step marked as **sensitive**, Ravian:

1. Pauses execution and creates an approval request.
2. Summarizes what it intends to do, including context and key parameters (for example, recipients, amount, or target system).
3. Presents options such as **Approve**, **Edit**, or **Reject**.

If you approve, the workflow resumes and the action is executed; if you reject, Ravian either skips the action or asks you how to proceed.

---

## Configuring approval rules

You can configure approvals at different levels:

- **By action type** – for example, sending email, submitting web forms, or updating records.
- **By destination** – such as specific domains, applications, or folders.
- **By risk level** – only require approvals when certain thresholds are crossed (for example, monetary limits).

These rules can be adjusted over time as you gain confidence in Ravian’s behavior.

!!! warning
    For shared or production systems, keep approvals enabled for irreversible operations, even if the workflow has run successfully in the past.

---

## Example: Email approvals

1. You start a task like:

    ```text
    Draft and send follow-up emails to everyone I met at last week's conference, using my notes as context.
    ```

2. Ravian drafts personalized emails and queues them for review instead of sending immediately.

3. In the approval view, you can scan subject lines, recipients, and excerpts, then approve, edit, or cancel each message.

4. Only the emails you approve are actually sent; Ravian logs which ones were dispatched.

This pattern applies equally to job applications, invoices, or any outbound communication.