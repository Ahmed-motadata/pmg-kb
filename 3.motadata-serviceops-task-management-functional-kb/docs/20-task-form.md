# Task Form

**Path:** Admin → Service Desk → Task Management → Task Form (`/admin/form/task`)

The layout of the create/edit form used for a task. The page description reads:
"Customize form fields to capture task details." This is a drag-and-drop form builder:
a palette of field types on the left, the live form preview on the right.

## Page layout

```
Task Form
Customize form fields to capture task details.  View Setup Guide ↗

┌ Custom Fields ─────────┐   ┌ Task Form ────────────────────────────────┐
│ Text Fields            │   │ Subject *          [ full width ]         │
│  Text Input            │   │ User Group   | Task Type                   │
│  Text Area             │   │ Assignee            [ full width ]        │
│  Rich Text Area        │   │ Duration (Days) | Start Date               │
│ Selection Fields       │   │ End Date        | (…)                       │
│  Dropdown              │   │ Completion (%)      [ full width ]        │
│  Multi-Select Dropdown │   │ Status          | Priority                 │
│  Datetime              │   │ Notify Before   | Estimated Time *         │
│ Input Fields           │   │ Description         [ full width ]        │
│  Number                │   │ Attachment          [ full width ]        │
│  Checkbox              │   └────────────────────────────────────────────┘
│  Radio                 │
│ Special Fields         │
│  Attachment            │
│  Section               │
│  Label                 │
│ Advanced Fields        │
│  Dependent             │
└────────────────────────┘
```

## Custom Fields palette

The left rail lists the field types that can be dragged onto the form, grouped:

| Group | Field types |
|---|---|
| Text Fields | Text Input, Text Area, Rich Text Area |
| Selection Fields | Dropdown, Multi-Select Dropdown, Datetime |
| Input Fields | Number, Checkbox, Radio |
| Special Fields | Attachment, Section, Label |
| Advanced Fields | Dependent |

Each palette item has a drag handle; dropping it onto the preview adds that field.

## The built-in Task Form fields

The form preview ships with these fields (widths: "full" spans the row, "half" sits two
to a row):

| Field | Width | Type | Required | Notes |
|---|---|---|---|---|
| Subject | full | Text | Yes | The task's title |
| User Group | half | Search picker | No | |
| Task Type | half | Choice picker | No | Picks from the Task Types page |
| Assignee | full | Technician picker | No | "Select Technician" |
| Duration (Days) | half | Number | No | Defaults to 0.00 |
| Start Date | half | Date/time picker | No | |
| End Date | half | Date/time picker | No | |
| Completion (%) | full | Slider (0–100) | No | |
| Status | half | Choice picker | No | Picks from Task Status |
| Priority | half | Choice picker | No | |
| Notify Before | half | Number + unit dropdown (Hours) | No | Reminder lead time |
| Estimated Time | half | Number + unit dropdown (Hours) | Yes | |
| Description | full | Rich text editor | No | Has an "Enhance" (AI) action and an Import HTML option |
| Attachment | full | Attachment button | No | |

## Editing a field

Hovering a field on the preview reveals three controls: a **move** handle (drag to
reorder), a **one-column / width** toggle, and a **pencil** (edit). The pencil opens an
**Edit Field** dialog. For a built-in field like Duration (Days) it holds:

- **Name**, **Hint Text**, **Description**;
- a **Requester** section: **View** and **Requester Group Access Level** (a Select with
  Edit) plus a **Required** toggle;
- a **Technician** section with its own **Required** toggle;
- an **AI Accessible** toggle;
- **Update** / **Cancel**.

Custom fields added from the palette open a similar editor where their choices/labels are
set.
