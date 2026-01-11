# Web Automation & Browsing

Ravian AI acts as a **hands‑on operator** for the web, eliminating manual clicking, form filling, and copy‑paste across sites.

You describe the outcome; Ravian navigates pages, fills forms, scrapes data, and orchestrates flows across multiple web apps.

---

## What this capability does

Web automation allows Ravian to:

- Open and navigate websites, log in where authorized, and follow links.
- Fill and submit forms, upload or download files, and manage paginated results.
- Extract structured data from tables, lists, and detail pages.
- Move information between tools, such as copying leads into a CRM or tickets into an issue tracker.
- Combine web actions with email, calendars, and files as part of a single workflow.

!!! warning
    Only grant Ravian access to accounts and sites you trust. For sensitive systems, configure human approvals before actions like sending messages or submitting forms.

---

## Typical workflows

Examples of web automation workflows:

- Filling repetitive forms across job boards or portals.
- Scraping product, pricing, or listing data into a spreadsheet.
- Booking logistics such as flights and hotels based on preferences.
- Synchronizing records between SaaS tools where native integrations are limited.

Because Ravian maintains context, it can handle branching logic, retries, and error handling dynamically.

---

## Example: Automated form‑based workflow

1. Ask Ravian, for example:

    ```text title="prompt"
    Apply to 10 suitable data scientist roles on these job boards using my resume and this cover letter template.
    ```
    
2. Ravian searches for relevant roles, opens listings, and fills out forms using your provided information and constraints.

3. When needed, it pauses for approvals (for example, before submitting an application) if you have enabled human‑in‑the‑loop controls.

4. It generates a log of completed applications and saves it to your workspace.

This pattern extends to vendor sign‑ups, surveys, lead capture, and other high‑volume web tasks.