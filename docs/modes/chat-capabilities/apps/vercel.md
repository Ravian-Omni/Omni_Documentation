# Vercel in Chat Mode

Connecting Vercel lets you **deploy projects, manage deployments/domains/envs, handle teams/members, and fetch logs directly from chat**, streamlining frontend deployment workflows.

Use it for CI/CD automation, production pushes, team access, and monitoring.

---

## What Vercel can do 

Once Vercel is connected (Settings → Connections → Vercel), you can:

- Deploy projects, list/get deployments, promote production.
- Manage domains, env vars, teams/members/invitations.
- Get project details, logs, usage.

---

## 1. Project deployments 

### Deploy and promote

**Capabilities:** Deploy project, list deployments, get deployment, promote.  

**What it does:** Launches updates.

1. Deploy site

    ```text title="Prompt – production deploy"
    Deploy project "my-portfolio" from main branch.
    List recent deployments, promote latest to production.
    Get deployment URL/status.
    ```

2. Rollback

    ```text title="Prompt – fix issues"
    List deployments last 24h for "api-service".
    Promote deployment abc123 (stable version).
    ```

---

## 2. Domains and config 

### DNS and vars

**Capabilities:** List/add domains, manage env vars.  

**What it does:** Customizes setup.

1. Custom domain

```text title="Prompt – domain setup"
List domains for "my-portfolio".
Add domain "portfolio.com", verify DNS.
Set env var API_KEY=prod-value (production scope).
```

---

## 3. Teams and access 

### Collaboration

**Capabilities:** List teams/projects, manage members/invitations.  

**What it does:** Team management.

1. Team ops

```text title="Prompt – member invite"
List my teams/projects.
Invite dev@collab.com to team "Frontend" (member role).
List team members.
```

---

## 4. Logs and monitoring 

### Debug and usage

**Capabilities:** Get logs, usage stats.  

**What it does:** Troubleshooting.

1. Error logs

```text title="Prompt – debug deploy"
Get logs for deployment def456 last 1h.
Check usage for team "Frontend".
```

---

## 5. Project overview 

### Inventory

**Capabilities:** List projects, get project.  

**What it does:** Portfolio view.

1. Project list

```text title="Prompt – inventory"
List all my projects with latest deployment status.
Get details for "ecommerce-app".
```

---

## Best practices for Vercel 

- **Scopes match.** Env vars per env (preview/prod).  
- **Git triggers.** Deploy from branches/PRs.  
- **Team roles.** Owner vs member permissions.  
- **Logs timely.** Check post-deploy.

To connect Vercel, open **Settings → Connections → Vercel** (OAuth/API token). Then run prompts directly from Chat Mode.