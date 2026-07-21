# Task Status

**Path:** Admin → Service Desk → Task Management → Task Status
(`/admin/status?type=task`)

The statuses a task moves through in its lifecycle. The page description reads: "Define
statuses to track the task lifecycle."

## Page layout

This screen is shared with the other modules' statuses. A row of module tabs sits at the
top — **Request · Problem · Change · Release · Asset · CMDB · Task** — and the **Task**
tab is selected here. Below it:

```
[Request] [Problem] [Change] [Release] [Asset] [CMDB] [Task]

⊕ Add Status
┌──────────────────────────────────────────────┐
│ ● Open                                    (⚪) │
│ ● In Progress                          ✎  (⚪) │
│ ● Pending                                 (⚪) │
│ …                                            │
└──────────────────────────────────────────────┘
```

- **⊕ Add Status** opens an inline add form.
- Each status is a row with a colored dot, the status name, an **Edit** (pencil), and a
  toggle. Some statuses also show a **Delete** link (Rejected did here); the built-in
  ones do not.

## The statuses in this environment

Six statuses, each with a color:

| Status | Dot color |
|---|---|
| Open | yellow |
| In Progress | blue |
| Pending | orange |
| Rejected | red |
| Resolved | green |
| Closed | grey |

"Open" is the default status — its toggle is on and locked (disabled). The other
statuses have their own toggles.

## Add / edit a status

**Add Status** shows a small inline form with:

- **Name** (required — "Name field is required" when empty),
- **Color** — a color picker button,
- **Save** / **Cancel**.

Editing a status (pencil) uses the same Name + Color form pre-filled with the status's
current values.
