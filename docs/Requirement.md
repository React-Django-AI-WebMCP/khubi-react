# Calendar Module – Requirement Document

## 1. Purpose
This calendar module helps users **log their work time**, **see meetings and activities**, and **collaborate with teammates** in a simple and clear way. The goal is to make time tracking easy, visual, and trustworthy — not complicated or technical.

---

## 2. What this module does

The calendar shows time-based entries for a user. These entries can come from different sources but are shown together in one place so the user gets a complete picture of their day, week, or month.

Users can:
- Log their own work or meetings
- See meetings logged by others where they were mentioned
- See events pulled from Google Calendar
- Filter what they want to see

---

## 3. Types of calendar entries

### 3.1 Logged Entries
- These are entries **created and saved by the user**
- They represent confirmed time spent on work or meetings
- The user has full control over these entries

User can:
- Edit the entry
- Duplicate the entry
- Delete the entry

---

### 3.2 Mentioned Entries
- These entries are created when **another user mentions you** in their logged entry
- They act as a **suggestion**, not a confirmed log

Example:
A daily scrum meeting is logged by User A from 9:30–10:00. User A mentions B, C, and D. B, C, and D will see a suggested entry for that time.

For mentioned entries, the user can:
- Accept and save it (it becomes a logged entry)
- Edit it before saving
- Ignore or dismiss it

Mentioned entries do **not** automatically count as logged time.

---

### 3.3 Integrated Entries (Google Calendar)
- **One-way sync:** The system fetches meetings from the user’s Google Calendar. Entries are synced according to the person’s calendar.
- They are shown only for reference (meetings scheduled in Google Calendar).
- They cannot be edited or deleted inside this system.
- **Editing in Nexus does not edit Google Calendar** — changes in this portal stay in this system only.

---

## 4. Calendar view

- **Only the weekly view is in scope** — it is the single and default view. No month or custom-range view.
- By default, all types of entries are visible.
- Users can choose to hide or show:
  - Logged entries
  - Mentioned entries
  - Integrated entries

Hiding entries only affects visibility — no data is removed.

---

## 5. Projects, tasks, and colors

- **Projects and tasks are managed internally** in this tool (not from another system).
- **Hierarchy:** Project → Task (each task belongs to a project).
- Users can see a list of projects and their related tasks.
- Each project has a fixed color.
- Calendar entries use the **same color as the selected project**.

Example:
If a user logs time for Project ABC (green), the calendar entry will also appear in green.

---

## 6. Adding a new entry

### How to add
- User clicks on an empty area in the calendar.
- A form opens (in the **right sidebar**, per the Figma design) to add a new entry.
- The Figma file defines **multiple states** for this flow; the main ones are the right-sidebar states where the user fills in details while creating (or editing) a time entry.

### Fields in the form

- **Description** (Required)
  - What the work or meeting was about
- **Select Attendees** (Optional)
  - Mention other employees
- **Project : Task** (Required)
  - Select the project and then the task
- **Time** (Required)
  - Start and end time OR duration
- **Date** (Required)
  - Date of the entry

The system should automatically calculate duration when start and end time are provided.

---

## 7. Editing entries

- Only logged entries can be edited.
- Editing affects only that specific entry.
- Changes do not affect entries created by other users.

### 7.1 Drag and drop

- Users can edit **logged entries** by **drag and drop**. Drag is **not** available for mentioned or integrated entries — only for logged entries.
- **Only the time of the entry changes** when dragging (e.g. move to a different time or day). There is no drag-to-change project/task and no split-entry feature — rescheduling time only.

---

## 8. Duplicating entries

- User can duplicate a logged entry
- The duplicated entry opens in edit mode
- User must save it to confirm

---

## 9. Deleting entries

- User can delete their own logged entries
- Deleted entries are removed from the calendar

---

## 10. User experience expectations

- Calendar should feel fast and responsive
- Entry types should be easy to visually tell apart
- Hovering or clicking an entry should clearly show:
  - Description
  - Project and task
  - Time
  - Attendees

---

## 11. Errors and validations

- Required fields must be filled before saving
- If time overlaps with another entry, show a warning (do not block)
- Google Calendar sync issues should not block usage

---

## 12. Confirmed decisions

The following points are confirmed and should be treated as final requirements:

- **Google Calendar entries can be converted into logged entries**
  - User can manually convert an integrated (Google Calendar) entry into a logged entry
  - Once converted, it behaves like a normal logged entry (editable, duplicable, deletable)

- **Time zone handling**
  - All times are stored in the backend in **UTC**
  - Users always see times displayed in **IST** in the calendar and forms

- **Mentioned entries editing**
  - Users are allowed to edit mentioned (suggested) entries before saving
  - After saving, the entry becomes a logged entry owned by the user

---

## 13. Scope and design reference

- **In-scope:** Only the calendar-related screen(s) in the linked Figma node (`12568-210659`), not the entire file “02.1-Time-Tracker---Nexus”.
- **UI states:** The Figma file contains multiple states; the main ones are in the **right sidebar**, where the user fills in details while creating or editing a time entry. Layout, actions, and components for these states are defined in the design.

---

## 14. Final note

This module should stay **simple and clear**. If users need training to use it, the design has failed. The focus is speed, clarity, and trust in the data — nothing more.

