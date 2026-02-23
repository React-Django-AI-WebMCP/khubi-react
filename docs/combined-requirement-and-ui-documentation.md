# Combined Requirement & UI Documentation

**Design reference:** [02.1 Time Tracker — Nexus](https://www.figma.com/design/4Qf2rnpZ0qrOpR6vilPUQ3/02.1-Time-Tracker---Nexus?node-id=12568-210659) (Figma node `12568-210659`).

**Context:** Timesheet management tool with calendar integration. Timesheet entries can be edited by drag and drop.

---

## 1. Functional Requirements

### 1.1 Timesheet management

- The system must allow users to view and manage timesheet entries (time logged against work).
- The system must allow users to edit timesheet entries by **drag and drop**. **Drag applies only to logged entries** (not to mentioned or integrated). Only the **time** of the entry changes (e.g. move to a different time or day). Users cannot drag to change project/task or to split entries — rescheduling only.

### 1.2 Calendar as view and Google Calendar

- **Calendar as view:** The calendar is how time entries are displayed; entries are internal to the system.
- **Google Calendar:** The system integrates with Google Calendar to **fetch** the user’s scheduled meetings only. Sync is one-way (from Google into this system). Editing an entry in this portal does **not** edit Google Calendar.

### 1.3 Date range and views

- **Weekly view only** — it is the single and default view. No month or custom-range view in scope.

### 1.4 Projects and tasks

- The system must support associating time entries with projects and tasks. Projects and tasks are **managed internally** in this tool. Hierarchy is **project → task**.

### 1.5 Workflow and user roles

- **No submit/approve/reject workflow** — only recording and editing of time entries.
- This module is accessible **only to employees**.

### 1.6 Scope

- Scope is limited to the **calendar-related screen(s)** in the linked Figma node (`12568-210659`), not the whole file “02.1-Time-Tracker---Nexus”.

---

## 2. UI Documentation

*The following should be validated and refined against the Figma design at the link above; exact layout, labels, and components are defined there.*

### 2.1 Screen: Time Tracker / Timesheet (primary)

**Node ID:** `12568-210659`  
**Design file:** 02.1-Time-Tracker---Nexus

#### Layout sections

- **Header:** Area at top of the screen (title, navigation, or primary actions). Exact content to be taken from Figma.
- **Main content:** Area where the timesheet/calendar is shown (weekly view; grid or list of time entries).
- **Right sidebar:** Used for creating and editing time entries — user fills in details (description, project/task, time, date, attendees, etc.) here. The Figma file defines multiple states for this flow.
- **Footer (if present):** Optional bottom area for actions or summary. Confirm presence and contents in Figma.

#### Visible actions

- **Click:** Buttons, links, week selectors, and other controls; click on empty calendar area to add a new entry (opens form in right sidebar). Exact labels and targets to be taken from Figma.
- **Drag:** **Logged entries only** can be dragged to change **time only** (reschedule); mentioned and integrated entries cannot be dragged. No drag-to-change project/task or split. Exact drag targets and feedback to be taken from Figma.
- **Toggle:** Any toggle or switch shown in the design (e.g. filter toggles for entry types). Confirm in Figma.
- **Hover:** Hover states on interactive elements where shown in Figma.

#### UI components

- Buttons (primary, secondary, icon, etc. as in design).
- Inputs (e.g. time, duration, project/task selectors).
- Lists or rows representing time entries.
- Calendar or date-grid components (if present).
- Right-sidebar form/panel for add/edit entry (per design).
- Any tabs, toggles, or dropdowns shown in the design.

#### Data displayed

- Time entries (date, time range, duration, project/task, description).
- Weekly date range (weekly view only).
- Labels, totals, or status indicators shown in the design.
- Fetched Google Calendar meetings (read-only in this UI).

#### Visual states

- **Default:** Normal state of all components as in Figma.
- **Hover:** Hover states for interactive elements where designed.
- **Active / Selected:** Selected date, entry, or control where designed.
- **Disabled:** Disabled controls or states if shown in Figma.
- **Drag:** Visual feedback during drag-and-drop (e.g. placeholder, cursor) as in Figma.

#### Explicit unknowns

- Exact list of layout sections and all interactive elements and their labels to be validated with Figma.

### 2.2 Additional states (right sidebar and others)

- The Figma file contains **multiple states**; the main ones are in the **right sidebar**, where the user fills in details while creating or editing a time entry.
- Other states (e.g. empty state, different sidebar steps) should be listed and documented using the same structure (Layout sections, Visible actions, UI components, Data displayed, Visual states) once identified from Figma.

### 2.3 Figma notes

- If the design contains visible text layers labeled **REQ:**, **RULE:**, or **EDGE:**, quote them verbatim here and treat as potential requirements; mark as NEEDS CLARIFICATION if they conflict with the UI or are ambiguous.

---

*End of document. For full product requirements and behaviour, see [Requirement.md](../Requirement.md) in the repo root.*
