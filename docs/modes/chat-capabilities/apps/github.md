# GitHub in Chat Mode

Connecting GitHub lets Ravian **create issues, review code, and update repos directly from chat**, turning “track this bug” or “open a PR” into real GitHub actions.

Use it to manage tasks, keep documentation in sync, and automate common repository workflows while you stay in a conversational interface.

---

## What Ravian can do with GitHub

Once GitHub is connected (Settings → Connections → GitHub), Ravian can:

- Create and update issues, comments, labels, and milestones.
- Open pull requests, add reviews and comments, and check merge status.
- Create or update files, commits, and branches for simple content changes.
- Manage collaborators, invitations, and basic repository settings.
- Trigger workflows, deployments, and releases (when configured).

!!! note
    For safety, destructive actions (deletes, branch protection changes, etc.) should always be done with explicit confirmation and scoped prompts.

---

## 1. Capture work as issues

### Create and update issues

**Capabilities:** `GITHUB_CREATE_AN_ISSUE, GITHUB_CREATE_AN_ISSUE_COMMENT, GITHUB_ADD_ASSIGNEES_TO_AN_ISSUE, GITHUB_ADD_LABELS_TO_AN_ISSUE, GITHUB_CREATE_A_LABEL, GITHUB_CREATE_A_MILESTONE`  

**What it does:** Creates issues, comments, labels, and milestones, and assigns people so chats turn into trackable work items.

1. Create a detailed bug issue

    ```text title="Prompt – log a bug from chat"
    In the repository "team/app-frontend", create a GitHub issue titled
    "Login form freezes on slow networks". Use this summary:

    - Steps: open login page on 3G, fill email/password, click Sign In
    - Expected: spinner and eventual success/failure
    - Actual: button stays disabled, no error, page never updates

    Tag it with labels "bug" and "priority-medium", assign it to
    @frontend-dev, and add a comment asking for logs from the browser console.
    ```

2. Turn a conversation into a feature request

    ```text title="Prompt – convert chat to issue"
    From our last discussion about improving onboarding, create a
    "Feature: guided first‑run checklist" issue in "team/app-backend".
    Summarize the idea, add acceptance criteria in bullet points,
    label it "enhancement", and put it in the "Onboarding v2" milestone.
    ```

---

## 2. Review and collaborate on code

### Pull requests and reviews

**Capabilities:** `GITHUB_CREATE_A_PULL_REQUEST, GITHUB_CREATE_A_REVIEW_FOR_A_PULL_REQUEST, GITHUB_CREATE_A_REVIEW_COMMENT_FOR_A_PULL_REQUEST, GITHUB_CREATE_A_REPLY_FOR_A_REVIEW_COMMENT, GITHUB_CHECK_IF_A_PULL_REQUEST_HAS_BEEN_MERGED`  

**What it does:** Opens pull requests, adds reviews and comments, replies in threads, and checks whether PRs have been merged.

1. Open a PR from a branch

    ```text title="Prompt – open a PR"
    For the repository "team/docs-site", open a pull request from branch
    "feature/chat-integrations" into "main" titled
    "Add Chat Integrations docs". Use a short summary and mark it as
    ready for review. Add labels "docs" and "ready-for-review".
    ```

2. Add a structured review

    ```text title="Prompt – review a PR"
    On the latest open pull request in "team/docs-site" with
    "chat integrations" in the title, add a review that:

    - Approves the changes if no obvious issues are found.
    - Leaves line comments where examples are unclear.
    - Adds a general comment summarizing key strengths and any follow‑ups.

    If you find blocking problems, change the review to "Request changes"
    and list them explicitly.
    ```

3. Answer a review comment thread

    ```text title="Prompt – reply to review"
    Find the review comment on that PR where a reviewer asks
    "Can we simplify this example?". Reply in the same thread with a
    more concise version of the example, and mention that a longer version
    is available in the advanced section.
    ```

---

## 3. Lightweight content and file changes

### Create or update files

**Capabilities:** `GITHUB_CREATE_OR_UPDATE_FILE_CONTENTS, GITHUB_DELETE_A_FILE, GITHUB_COMMIT_MULTIPLE_FILES, GITHUB_CREATE_A_BRANCH_REFERENCE (via GITHUB_CREATE_A_REFERENCE), GITHUB_CREATE_A_COMMIT`  

**What it does:** Creates, updates, and deletes files, or batches multiple file changes into a single commit for docs and configuration tweaks.

1. Update a README section

    ```text title="Prompt – update README"
    In the repo "team/docs-site", update README.md to add a new section
    called "Chat Integrations" after the introduction. Summarize in 3–4
    bullets what users gain by connecting Gmail, Calendar, and GitHub.
    Create a commit on a new branch "docs/chat-integrations" with a clear
    commit message.
    ```

2. Batch update multiple docs

    ```text title="Prompt – multi-file docs commit"
    In "team/docs-site", in the `docs/modes/chat-capabilities` folder,
    update any pages that still say "Quick Start" to instead say
    "Installation & Setup", including headings and navigation text.

    Make these edits as a single commit on a branch called
    "docs/rename-quick-start", using a commit message that explains the change.
    ```

3. Remove obsolete file (careful)

    ```text title="Prompt – remove obsolete file"
    In "team/docs-site", delete the file `docs/getting-started/quick-start-old.md`
    only if it is not referenced from mkdocs.yml or any other doc files.
    Show me where it's referenced, if anywhere, before deleting.
    ```

!!! warning
    For deletes and large edits, always ask Ravian to show the planned diff or affected files before applying changes.

---

## 4. Repository access and collaborators

### Manage collaborators and invitations

**Capabilities:** `GITHUB_ADD_A_REPOSITORY_COLLABORATOR, GITHUB_ACCEPT_A_REPOSITORY_INVITATION, GITHUB_CHECK_IF_A_USER_IS_A_REPOSITORY_COLLABORATOR`  

**What it does:** Adds collaborators to repos, checks collaborator status, and accepts invitations for the authenticated user.

1. Add a collaborator

    ```text title="Prompt – add collaborator"
    In the repository "team/docs-site", add the user "new-writer"
    as a collaborator with write access. Confirm if they already exist
    as a collaborator before sending a new invitation.
    ```

2. Accept pending invitations

    ```text title="Prompt – accept repo invites"
    Check for any pending repository invitations for my account.
    Accept invitations for repositories under the "team" organization,
    but leave others untouched and list them separately.
    ```

---

## 5. Automation, CI, and deployments

### Trigger workflows and deployments

**Capabilities:** `GITHUB_CREATE_A_WORKFLOW_DISPATCH_EVENT, GITHUB_CREATE_A_REPOSITORY_DISPATCH_EVENT, GITHUB_CANCEL_A_WORKFLOW_RUN, GITHUB_APPROVE_A_WORKFLOW_RUN_FOR_A_FORK_PULL_REQUEST, GITHUB_CREATE_A_DEPLOYMENT, GITHUB_CREATE_A_DEPLOYMENT_STATUS`  

**What it does:** Manually triggers GitHub Actions workflows, approves runs from forks, cancels jobs, and creates deployment records with statuses.

1. Manually trigger a workflow

    ```text title="Prompt – run docs build workflow"
    In the repo "team/docs-site", trigger the GitHub Actions workflow
    named "Build and Deploy Docs" on the `main` branch using the
    `workflow_dispatch` event. Pass an input parameter `environment=preview`.
    Let me know when the run has started and link to its status page.
    ```

2. Approve a workflow from a fork

    ```text title="Prompt – approve fork workflow"
    Find the most recent workflow run triggered by a forked pull request
    in "team/docs-site" that is waiting for approval, and approve it
    so checks can run. Tell me which PR it belongs to.
    ```

3. Mark deployment status

    ```text title="Prompt – mark deployment complete"
    For the latest deployment of "team/docs-site" to the "production"
    environment, update the deployment status to "success" and attach
    a short description like "Docs sync with latest Chat Mode updates".
    Include the URL of the deployed site.
    ```

---

## 6. Releases and project housekeeping

### Create releases

**Capabilities:** `GITHUB_CREATE_A_RELEASE`  

**What it does:** Creates tagged releases with notes, optionally linking to discussions.

```text title="Prompt – create a release"
In "team/docs-site", create a release for tag `v1.2.0-docs`
titled "Docs v1.2 – Chat Integrations". Include a changelog that
summarizes new Chat Mode pages and integration guides, and link
to any related issues and pull requests that were closed.
```

---

## Best practices for GitHub with Ravian

- **Work in branches.** Ask Ravian to create branches for non‑trivial changes so you can review them via PRs.  
- **Keep prompts scoped.** Specify repo, branch, file paths, and labels to avoid ambiguous actions.  
- **Review before merge.** Use Ravian to draft PRs and reviews, but keep final approvals and merges as a deliberate human decision.  
- **Combine with other tools.** Typical flow: summarize an issue from logs → create GitHub issue → open PR with docs update → trigger CI and deployment from Chat Mode.

To connect GitHub, open **Settings → Connections → GitHub** in the Ravian app and complete the sign‑in flow. After that, you can run any of the prompts above directly from Chat Mode.