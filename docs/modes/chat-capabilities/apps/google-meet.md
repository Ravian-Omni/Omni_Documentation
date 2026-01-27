# Google Meet in Chat Mode

Connecting Google Meet lets Ravian **create, manage, and analyze video meetings directly from chat**, turning “set up / review this call” into concrete Meet spaces and summaries.

Use it for quickly spinning up meeting links, ending sessions, and reviewing transcripts and participation from past calls.

***

## What Ravian can do with Google Meet

Once Google Meet is connected (Settings → Connections → Google Meet), Ravian can:

- Create Meet spaces and share links for upcoming calls.
- End active conferences when a session is over.
- Retrieve details, recordings, and transcripts for past meetings.
- Inspect who joined, when they joined, and how long they stayed.
- Update Meet space configuration (access type, entry rules).

!!! note
    Google Meet works especially well together with Google Calendar and Gmail for end‑to‑end scheduling, invites, and follow‑ups.

***

## 1. Create and manage live meetings

### Create a Meet space

**Capabilities:** `GOOGLEMEET_CREATE_MEET`  

**What it does:** Creates a new Google Meet space, optionally with specific access settings, and returns a join link and identifiers.

1. Quick ad‑hoc meeting

    ```text title="Prompt – instant stand‑up room"
    Create a new Google Meet for a quick 15‑minute stand‑up with the team.
    Give me the join link and a short message I can paste into Slack.
    ```

2. Controlled access meeting

    ```text title="Prompt – restricted strategy call"
    Create a Google Meet space for a "Strategy Deep‑Dive" with restricted access
    so only invited participants can join. Share the meeting link and list any
    settings you configured so I can review them.
    ```

***

### End an active conference

**Capabilities:** `GOOGLEMEET_END_ACTIVE_CONFERENCE`  

**What it does:** Ends an ongoing conference in a specific Meet space.

```text title="Prompt – end running meeting"
Find the active Google Meet session for today's “Design Review”
and end the conference once everyone has left the call.
Confirm which meeting you’re ending before you do it.
```

***

## 2. Inspect past meetings

### List and inspect conference records

**Capabilities:** `GOOGLEMEET_LIST_CONFERENCE_RECORDS, GOOGLEMEET_GET_MEET, GOOGLEMEET_GET_CONFERENCE_RECORD_FOR_MEET`  

**What it does:** Lists past conferences and retrieves details for a specific Meet space or conference record.

1. Recent meetings overview

    ```text title="Prompt – recent meetings summary"
    Show me all Google Meet conferences from the last 7 days,
    grouped by title. For each, include date, duration, and approximate
    number of participants.
    ```

2. Details for a specific call

    ```text title="Prompt – inspect a single call"
    Find the conference record for the meeting titled
    "Quarterly Metrics Review" held this week and summarize:
    start/end time, total duration, and total number of unique participants.
    ```

***

## 3. Participants and engagement

### Participant sessions

**Capabilities:** `GOOGLEMEET_LIST_PARTICIPANT_SESSIONS, GOOGLEMEET_GET_PARTICIPANT_SESSION`  

**What it does:** Lists join/leave sessions per participant and provides detailed engagement data.

1. Attendance report

    ```text title="Prompt – attendance for a workshop"
    For the last "Customer Onboarding Workshop" meeting, generate
    an attendance report that shows, for each participant:
    - Display name
    - Time joined and time left
    - Total minutes in the meeting

    Highlight anyone who joined more than 10 minutes late or left early.
    ```

2. Deep‑dive on one participant

    ```text title="Prompt – participant engagement"
    For the same workshop, show me the join/leave history for
    the participant with email product.manager@example.com and any
    notes about multiple join sessions (reconnects).
    ```

***

## 4. Recordings and transcripts

### Get recordings

**Capabilities:** `GOOGLEMEET_GET_RECORDINGS_BY_CONFERENCE_RECORD_ID`  

**What it does:** Retrieves recordings associated with a specific conference record.

```text title="Prompt – locate recordings"
For the "Quarterly Metrics Review" meeting, find any associated
recordings and provide:
- The recording links
- File sizes
- Where they are stored (Drive locations if available)
```

***

### Work with transcripts

**Capabilities:** `GOOGLEMEET_GET_TRANSCRIPTS_BY_CONFERENCE_RECORD_ID, GOOGLEMEET_LIST_TRANSCRIPT_ENTRIES, GOOGLEMEET_GET_TRANSCRIPT_ENTRY`  

**What it does:** Lists available transcripts for a meeting and retrieves structured transcript entries (speaker, text, timestamps).

1. Meeting summary from transcript

    ```text title="Prompt – summarize transcript"
    Using the transcript from the latest "Roadmap Planning" Google Meet,
    summarize the meeting into:
    - 5 key decisions
    - 5 open questions
    - Action items grouped by owner

    Keep it concise enough to paste into a Notion page.
    ```

2. Extract a specific segment

    ```text title="Prompt – find pricing discussion"
    From that same transcript, find the segment where pricing strategy
    was discussed. Quote the key statements with timestamps and identify
    who was speaking.
    ```

***

## 5. Configure Meet spaces

### Update Meet space settings

**Capabilities:** `GOOGLEMEET_UPDATE_SPACE`  

**What it does:** Updates configuration of a Meet space, such as access type and entry rules.

```text title="Prompt – adjust access"
For the recurring Meet space used for the “Weekly Product Sync”,
update the settings so that only invited participants can join directly.
Everyone else should wait in the lobby until admitted.
Then summarize the final configuration in plain language.
```

***

## Best practices for Google Meet with Ravian

- **Name meetings clearly.** Use descriptive titles so prompts like “metrics review” or “design retro” are easy to resolve.  
- **Leverage transcripts.** After important calls, ask Ravian to turn transcripts into summaries, action lists, and follow‑up emails.  
- **Combine with Calendar and Gmail.** Typical flow: propose time in Calendar → create Meet → send invite or recap via Gmail – all orchestrated from Chat Mode.

To connect Google Meet, open **Settings → Connections → Google Meet** in the Ravian app and complete the sign‑in flow. After that, you can run any of the prompts above directly from Chat Mode.