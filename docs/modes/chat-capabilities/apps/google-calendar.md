# Google Calendar in Chat Mode

Connecting Google Calendar lets Ravian **schedule, move, and manage events directly from chat**, turning “set up this meeting” into real calendar updates.

Use it for scheduling, rescheduling, availability checks, and keeping your day in sync with the work Ravian does in other tools.

---

## What Ravian can do with Google Calendar

Once Google Calendar is connected (Settings → Connections → Google Calendar), Ravian can:

- Create, update, and delete events on your calendars.
- Find free slots and propose meeting times across calendars.
- Move events between calendars and adjust attendees.
- Query events for specific time ranges or queries.
- Manage calendars and basic sharing settings.

!!! note
    Google Calendar works especially well when combined with Gmail and Google Meet for end‑to‑end meeting workflows.

---

## 1. Create and update events

### Create events

**Capabilities:** `GOOGLECALENDAR_CREATE_EVENT, GOOGLECALENDAR_QUICK_ADD`  

**What it does:** Creates new events with date, time, duration, attendees, and optional Meet links, using either structured data or natural language.

1. Create a structured event

    ```text title="Prompt – create a structured event"
    Create a 60‑minute event called "Ravian docs review" tomorrow at 4pm
    on my primary calendar, with a Google Meet link, and invite
    kingsuk@example.com and john@example.com. Add a short description
    saying we'll review the new documentation pages.
    ```

2. Use natural language (quick add)

    ```text title="Prompt – quick add event"
    On my primary calendar, quickly add an event:
    "Ravian launch retro next Friday at 5pm with the core team".
    Make sure it appears in my time zone.
    ```

---

### Update and patch events

**Capabilities:** `GOOGLECALENDAR_UPDATE_EVENT, GOOGLECALENDAR_PATCH_EVENT`  

**What it does:** Updates all or specific fields on existing events (time, title, attendees, location, description, etc.).

1. Reschedule a meeting

    ```text title="Prompt – reschedule event"
    Find my next event titled "Ravian docs review" and move it to
    tomorrow at 6pm. Keep the same attendees and Meet link.
    Send an update to all participants after I approve the change.
    ```

2. Edit details only

    ```text title="Prompt – update description"
    Update the description of tomorrow's "Ravian launch retro" event
    to include an agenda with three bullet points:
    1) What went well, 2) What can be improved, 3) Action items.
    Do not change the time or attendees.
    ```

---

## 2. Manage and clean up events

### Delete or clear events

**Capabilities:** `GOOGLECALENDAR_DELETE_EVENT, GOOGLECALENDAR_CLEAR_CALENDAR`  

**What it does:** Deletes individual events or clears a primary calendar (deletes all events).

1. Delete a single event

    ```text title="Prompt – delete one event"
    Delete the event named "Test Ravian Calendar" scheduled for today
    at 11am from my primary calendar. Ask me to confirm before deleting.
    ```

2. (Dangerous) Clear a test calendar

    ```text title="Prompt – clear test calendar"
    On my "Ravian Test" calendar only, remove all events for all time.
    This is a test calendar, not my primary one. Show me the calendar
    you found and ask for explicit confirmation before clearing it.
    ```

!!! warning
    Never clear your primary calendar without a backup and explicit confirmation.

---

## 3. Find events and check your schedule

### List and search events

**Capabilities:** `GOOGLECALENDAR_EVENTS_LIST, GOOGLECALENDAR_EVENTS_LIST_ALL_CALENDARS, GOOGLECALENDAR_FIND_EVENT, GOOGLECALENDAR_EVENTS_GET`  

**What it does:** Lists events for a time range, searches by text, and retrieves specific events by ID across one or many calendars.

1. Today’s schedule

    ```text title="Prompt – today's schedule"
    Show me all events across all my calendars for today between 9am and 8pm.
    Group them by calendar and summarize each in one line.
    ```

2. Find a specific event

    ```text title="Prompt – find a specific event"
    Find the next event that contains "Ravian onboarding" in the title
    or description. Show me the time, attendees, and description.
    ```

---

### Free/busy and meeting suggestions

**Capabilities:** `GOOGLECALENDAR_FIND_FREE_SLOTS, GOOGLECALENDAR_FREE_BUSY_QUERY, GOOGLECALENDAR_GET_CURRENT_DATE_TIME`  

**What it does:** Computes free/busy windows and suggests slots for new meetings.

1. Suggest times for a 1:1

    ```text title="Prompt – find free slots"
    Check my calendar and find three 30‑minute free slots this week
    between 2pm and 6pm where both I and kingsuk@example.com are available.
    Propose the best slot and be ready to create a meeting there.
    ```

2. Quick availability summary

    ```text title="Prompt – availability summary"
    Looking at the next 7 days, summarize when I'm generally free
    and when I'm heavily booked. Highlight one or two good blocks
    for deep work sessions.
    ```

---

## 4. Coordinate between calendars

### Move events and work with multiple calendars

**Capabilities:** `GOOGLECALENDAR_EVENTS_MOVE, GOOGLECALENDAR_LIST_CALENDARS, GOOGLECALENDAR_GET_CALENDAR`  

**What it does:** Lists your calendars and moves events between them (e.g., from personal to work).

1. Move an event to another calendar

    ```text title="Prompt – move event"
    Find the "Ravian docs review" meeting scheduled this week on my
    primary calendar and move it to my "Ravian Work" calendar.
    Keep all details and attendees the same.
    ```

2. Inspect calendars

    ```text title="Prompt – list calendars"
    List all calendars I have access to, showing their names and
    whether they are primary, work, personal, or shared.
    Highlight which ones you will use by default when I say
    "my calendar".
    ```

---

## 5. Sharing and access (ACLs)

### Adjust calendar sharing

**Capabilities:** `GOOGLECALENDAR_ACL_INSERT, GOOGLECALENDAR_ACL_PATCH, GOOGLECALENDAR_ACL_DELETE, GOOGLECALENDAR_LIST_ACL_RULES`  

**What it does:** Manages who can see or edit a calendar via access control rules.

1. Grant read access

    ```text title="Prompt – share read-only"
    On my "Ravian Work" calendar, grant read‑only access to
    pm@example.com so they can see all events but not edit them.
    Confirm what you're about to change before applying it.
    ```

2. Review and revoke access

    ```text title="Prompt – clean up sharing"
    Show me who currently has access to my "Ravian Work" calendar
    and what their permission level is. Suggest any access that looks
    unnecessary, then remove only the entries I explicitly approve.
    ```

!!! note
    ACL changes can affect who can see your schedule. Always review the list before modifying permissions.

---

## 6. Notifications and syncing (advanced)

### Watch and sync events

**Capabilities:** `GOOGLECALENDAR_EVENTS_WATCH, GOOGLECALENDAR_SYNC_EVENTS, GOOGLECALENDAR_CHANNELS_STOP`  

**What it does:** Sets up and stops watch channels and keeps an external system in sync with calendar changes.

1. Keep a dashboard in sync (conceptual)

    ```text title="Prompt – sync for dashboard"
    Set up a sync for my primary calendar so that any changes to
    events in the next 30 days are reflected in the Google Sheet
    "Ravian_Calendar_Sync". When events are created, updated, or cancelled,
    update the corresponding rows in the sheet.
    ```

2. Stop a watch channel

    ```text title="Prompt – stop watching"
    Stop any existing watch channels you previously created for my
    calendars and confirm that no active channels remain.
    ```

---

## Best practices for Google Calendar with Ravian

- **Be explicit about time zones.** Mention the time zone if you work across regions to avoid confusion.  
- **Name calendars clearly.** Use specific calendar names in prompts (e.g., “Ravian Work” vs “primary”).  
- **Confirm destructive actions.** Always require confirmation before deleting events or clearing calendars.  
- **Combine with Gmail.** Let Ravian schedule a meeting, then draft and send the invite email or recap automatically.

To connect Google Calendar, open **Settings → Connections → Google Calendar** in the Ravian app and complete the sign‑in flow. After that, you can run any of the prompts above directly from Chat Mode.