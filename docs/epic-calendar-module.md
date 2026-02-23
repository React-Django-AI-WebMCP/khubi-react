# Epic: Calendar Module (Time Tracking & Calendar View)

**Source:** Requirement Document only. Design reference: [Figma 02.1 Time Tracker — Nexus](https://www.figma.com/design/4Qf2rnpZ0qrOpR6vilPUQ3/02.1-Time-Tracker---Nexus?node-id=12568-210659) (node `12568-210659`).

---

## Goal

Enable employees to log work time, see meetings and activities, and collaborate with teammates in a simple, visual way. Time tracking is easy, visual, and trustworthy—no submit/approve workflow; only recording and editing of time entries.

---

## In Scope

- **Weekly calendar view only** — single and default view for time-based entries. No month or custom-range view.
- **Three entry types:** Logged (user-created, full control), Mentioned (suggestions when another user mentions you), Integrated (fetched from Google Calendar, read-only in this system).
- **Add entry:** User clicks empty calendar area → form opens in right sidebar. Fields: Description (required), Project : Task (required), Time (required; start/end OR duration), Date (required), Select Attendees (optional). Duration auto-calculated when start and end time are provided.
- **Edit entries:** Only logged entries. Editing affects only that entry. Drag-and-drop to change **time only** (reschedule to different time or day); no drag-to-change project/task, no split entries.
- **Duplicate:** User can duplicate a logged entry; duplicated entry opens in edit mode; user must save to confirm.
- **Delete:** User can delete own logged entries; deleted entries removed from calendar.
- **Convert Google Calendar entry to logged entry:** User can manually convert an integrated (Google Calendar) entry into a logged entry; once converted it is editable, duplicable, deletable.
- **Filter visibility:** By default all types visible; user can hide or show Logged, Mentioned, Integrated. Hiding affects visibility only—no data removed.
- **Projects and tasks:** Managed internally; hierarchy Project → Task. Each project has a fixed color; calendar entries use the same color as the selected project.
- **Entry detail on hover/click:** Show Description, Project and task, Time, Attendees.
- **Validations:** Required fields must be filled before saving. If time overlaps another entry, show warning (do not block). Google Calendar sync issues must not block usage.
- **Time zone:** Times stored in UTC; displayed in IST in calendar and forms.
- **Scope:** Only calendar-related screen(s) in Figma node `12568-210659`. UI states (including right sidebar for create/edit) as defined in design.
- **Access:** Module accessible only to employees.

---

## Out of Scope

- Month view, custom date-range view.
- Submit / approve / reject timesheet workflow.
- Manager or non-employee access to this module.
- Drag-and-drop to change project or task, or to split entries.
- Editing Google Calendar from this system (one-way sync: fetch only; editing in Nexus does not edit Google Calendar).
- Any feature or screen outside the linked Figma node.

---

## NEEDS CLARIFICATION

- None from the Requirement Document for this epic. Exact layout, labels, and interactive elements to be validated against Figma where needed.
