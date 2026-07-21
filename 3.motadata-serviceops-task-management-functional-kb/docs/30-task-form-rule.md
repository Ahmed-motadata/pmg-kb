# Task Form Rule

**Path:** Admin → Service Desk → Task Management → Task Form Rule
(`/admin/form-rules/task`)

Rules that make the task form dynamic. The page description reads: "Show, hide, or
require fields on task forms based on conditions."

## Page layout

A list page:

- A **Select field to search…** filter box and an **All** filter button.
- A **Create Task Form Rule** button.
- A table with columns: a select checkbox, **Name**, **Rule Execution On**, **Rule
  Applicable For**, **Rule Event**, **Created Date**, **Enabled** (toggle), **Actions**.

Each row has an Enabled switch and action buttons (edit / delete). This environment has
one rule: "1. Task_Project", Rule Execution On "On Create and Edit", Rule Applicable For
"All Users", Rule Event "On Form Load", enabled.

## Create Task Form Rule — dialog

**Create Task Form Rule** opens a dialog with **Create** / **Cancel**. Fields:

| Field | Type | Choices / notes |
|---|---|---|
| Name | Text | The rule's name |
| Description | Multi-line text | |
| Tags | Tag input | |
| Rule Execution On | Radio | **On Create and Edit**, **On Create**, **On Edit** |
| Rule Applicable For | Radio | **All Users**, **All Technicians**, **All Requesters**, **All Logged-in Users** |
| Rule Event | Radio | **On Form Load**, **On Field Change**, **On Form Submit** |
| Conditions | Condition builder | **Add Condition Group** builds groups of field conditions |
| Action | Action builder | **Add Action** adds the actions the rule performs (show / hide / require a field) when the conditions match |

The condition and action builders take the task form's own fields; their exact option
lists depend on the fields configured on the Task Form page.
