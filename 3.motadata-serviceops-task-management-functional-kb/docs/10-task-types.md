# Task Types

**Path:** Admin → Service Desk → Task Management → Task Types
(`/admin/organization/task-type`)

The labels used to classify a task. The page description reads: "Classify tasks for
organization and reporting."

## Page layout

```
Task Types
Classify tasks for organization and reporting.  View Setup Guide ↗

⊕ Add Task Type

┌───────────────────────────────────────────────┐
│ Implementation                              ✎ │
├───────────────────────────────────────────────┤
│ Install/Uninstall                           ✎ │
│ …                                             │
└───────────────────────────────────────────────┘
```

- **View Setup Guide** opens the product documentation for task types in a new tab.
- **⊕ Add Task Type** opens an inline add row.
- Each type is a row. Rows are draggable (a "cursor-move" handle) so their order can be
  rearranged. Hovering a row shows a **pencil** (edit) icon; editing turns the row into
  an inline text box with a green check (confirm) and a red cross (cancel).

## The types in this environment

Nine task types ship here, in this order:

1. Implementation
2. Install/Uninstall
3. Maintainance
4. Planning
5. Release
6. Replacement/Repair
7. Testing
8. Troubleshooting
9. Milestone

## Add / edit a task type

**Add Task Type** shows a small inline form with a single required **Name** field and
**Save** / **Cancel**. Saving with the name empty shows "Name field is required".
Editing a row (pencil) reuses the same inline pattern, pre-filled with the current name,
confirmed with the green check or discarded with the red cross.
