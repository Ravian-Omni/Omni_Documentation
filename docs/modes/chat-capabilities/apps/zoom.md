# Zoom in Chat Mode

Connecting Zoom lets you **schedule meetings, manage webinars, track attendance, and automate video workflows directly from chat**, streamlining virtual events.

Use it for instant meetings, recurring sessions, webinar registration, and participant management.

---

## What Zoom can do

Once Zoom is connected (Settings → Connections → Zoom), you can:

- Create instant/one‑time/recurring meetings and webinars.
- Send invitations with custom agendas/waiting rooms.
- Manage participants: mute, rename, spotlight, breakout rooms.
- Retrieve meeting reports: attendance, duration, recordings.
- Update settings: passwords, registration, alternative hosts.

!!! note
    Requires Zoom Pro/Business account for advanced scheduling features.

---

## 1. Meeting scheduling

### Create and customize meetings

**Capabilities:** Instant, scheduled, recurring meetings with full options.  

**What it does:** Sets up complete meeting configurations.

1. Client demo

    ```text title="Prompt – schedule demo"
    Create Zoom meeting "CRM Pipeline Demo – Jordan Lee"
    Date: Feb 5, 2PM PT, Duration: 45min.
    Agenda: "Live demo + Q&A + next steps"
    Password: auto‑generate
    Registration: required (collect email/company)
    Alternative host: support@company.com
    Send calendar invite to jordan@peakperformance.co
    ```

2. Recurring team sync

    ```text title="Prompt – weekly meeting"
    Create recurring Zoom meeting "Weekly Pipeline Review"
    Every Monday 10AM PT, 60min, no password.
    Waiting room: on, host: current user.
    Auto‑record: cloud, mute participants on entry.
    Share join link in #sales Slack.
    ```

---

## 2. Webinar and large events

### Registration and management

**Capabilities:** Webinars with registration, Q&A, polling.  

**What it does:** Scales to 100–10,000+ attendees.

1. Product workshop

```text title="Prompt – webinar setup"
Create Zoom Webinar "Master Pipeline Velocity – Live Workshop"
Capacity: 500, Date: Feb 12, 11AM PT, 90min.
Registration questions: Company size, Role, Goals.
Agenda: Intro → Demo → Live Q&A → Resources.
Polling: "Current pipeline bottleneck?"
Post to LinkedIn/Eventbrite.
```

---

## 3. Real‑time meeting control

### Participant and session management

**Capabilities:** Mute/rename/spotlight participants, breakout rooms.  

**What it does:** Moderates live sessions.

1. Large team all‑hands control

```text title="Prompt – meeting moderation"
In current "All Hands" Zoom meeting:
-  Mute all non‑presenters
-  Spotlight CEO + demo lead
-  Create 4 breakout rooms by department (10min)
-  Announce: "Breakouts now open – discuss Q1 goals"
-  Share attendance report post‑meeting
```

---

## 4. Reporting and insights

### Attendance and performance

**Capabilities:** Meeting reports, participant lists, recording access.  

**What it does:** Tracks engagement and ROI.

1. Weekly meeting analytics

    ```text title="Prompt – attendance report"
    Generate report for last 7 days Zoom meetings:
    -  Total meetings, total participants
    -  Top no‑shows by frequency
    -  Average duration by meeting type
    -  Recording completion status

    Flag meetings <50% attendance.
    ```

2. Webinar ROI

    ```text title="Prompt – event analysis"
    Analyze "Pipeline Workshop" webinar:
    -  Registrants vs attendees (show rate)
    -  Top industries/roles
    -  Q&A questions/themes
    -  Post‑event survey results

    Calculate cost per lead.
    ```

---

## 5. Automation and workflows

### Recurring patterns and integrations

**Capabilities:** Bulk scheduling, alternative hosts, calendar sync.  

**What it does:** Scales meeting management.

1. Customer onboarding series

```text title="Prompt – drip meetings"
Create 3‑meeting onboarding series for new enterprise clients:
1. Kickoff (Week 1)
2. Training (Week 2) 
3. Review (Week 4)

Alternative host: onboarding@company.com
Auto‑add to Google Calendar, notify via Slack.
```

---

## Best practices for Zoom

- **Agenda clarity.** Always include purpose/duration in title.  
- **24h advance.** Schedule >24h ahead for best attendance.  
- **Record selectively.** Cloud recording for key meetings only.  
- **Combine tools.** Flow: HubSpot deal → Zoom demo → Notion notes → Slack recap.

To connect Zoom, open **Settings → Connections → Zoom** (Pro account + JWT/OAuth). Then run prompts directly from Chat Mode.