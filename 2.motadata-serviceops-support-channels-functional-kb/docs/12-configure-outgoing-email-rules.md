# Configure Outgoing Email Rules — dialog

Opened by the **Configure Outgoing Email Rules** button on the Outgoing Email Servers
page. Routes records of a module through a chosen outgoing email server when conditions
match.

## Layout

A dialog titled **Configure Outgoing Email Rules** with a close (×) button, one tab per
module, the rules for the active tab, and **Update** / **Cancel** at the bottom.
Nothing is saved until Update.

Module tabs (8, fixed): **Request · Problem · Change · Release · Asset · CMDB ·
Contract · Purchase**. Each module keeps its own list of rules.

## A rule

**Add Outgoing Email Rules** adds a rule block containing:

- a reorder handle and a **Delete** button for the rule;
- **Enabled** — toggle;
- **Outgoing Email** — required picker ("Outgoing Email field is required" when left
  empty); it picks one of the outgoing email servers configured on this page;
- **Conditions** — a condition builder:
  - **Add Condition Group** adds a group; inside a group, a field picker (searches the
    module's fields) plus **Add Condition** for more rows in the group and a delete
    button per row;
  - **Remove All Condition** clears the builder.

Multiple rules can be stacked per module tab. In this environment no rules were
configured; the exact option lists of the field picker follow the active module's
fields.
