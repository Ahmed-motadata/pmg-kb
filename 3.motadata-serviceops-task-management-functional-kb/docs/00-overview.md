# Task Management — Overview

Task Management is an admin section of Motadata ServiceOps that configures how **tasks**
work across the product. Tasks are the checklist-style units of work attached to
requests, problems, changes, and releases. This section defines the vocabulary and shape
of those tasks: their types, the fields on the task form, the rules that show/hide/require
those fields, and the statuses a task moves through.

This guide describes the PMG ServiceOps environment at `http://172.16.15.185` as of
21 July 2026. All labels and options are copied from the live product.

## Where it sits

Open **Admin** (the technician portal's admin area). In the left sidebar under **Service
Desk**, the **Task Management** group holds four pages:

```
Task Management
├── Task Types      /admin/organization/task-type   (also linked as "Task Types")
├── Task Form       /admin/form/task
├── Task Form Rule  /admin/form-rules/task
└── Task Status     /admin/status?type=task
```

(The Task Types page lives under the `/admin/organization/...` path but appears in the
Task Management sidebar group.)

## How the pieces relate

- **Task Types** are the labels that classify a task (Implementation, Testing, and so
  on). A task picks one type; the type is used for organization and reporting.
- **Task Form** is the layout of the create/edit form for a task — the built-in fields
  (Subject, Assignee, dates, Status, Priority, and so on) plus any custom fields dragged
  in from the palette.
- **Task Form Rule** makes the form dynamic: based on conditions, a rule can show, hide,
  or require fields when the form loads, when a field changes, or on submit.
- **Task Status** is the lifecycle — the set of statuses (Open, In Progress, Pending,
  Rejected, Resolved, Closed) a task can be in, with their colors and enabled state.

## Patterns shared across these pages

- Every page has a title, a one-line description, and a **View Setup Guide** link that
  opens the matching page of the product documentation (docs.motadata.com) in a new tab.
- Task Status shares the same screen as the other modules' statuses: a row of module
  tabs (Request · Problem · Change · Release · Asset · CMDB · Task) sits at the top and
  the **Task** tab is selected here.
- Required fields carry a red asterisk and show "<Field> field is required" when left
  empty.
- Small add forms (a task type, a status) appear inline with **Save** / **Cancel**;
  larger ones (a form rule) open a dialog with **Create** / **Cancel**.

## Files in this guide

See the README index one level up. One file per page.
