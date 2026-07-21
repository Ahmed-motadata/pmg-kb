# About this folder

Functional documentation of the **Task Management** admin section of Motadata ServiceOps
(Task Types, Task Form, Task Form Rule, Task Status), captured live from PMG ServiceOps
(`http://172.16.15.185`) on 2026-07-21 using the `/functional-kb` skill. One file per
page under `docs/`; `README.md` is the index.

## Maintaining these docs

- Facts come from the live product, not guesses. To update, open the page in the app and
  re-check before editing.
- Keep the product's exact vocabulary and list fixed choice-sets completely.
- Plain English, short sentences, tables for fields, no opinions.
- The Task Types list and the Task Status set include tenant data ("Maintainance"
  spelling is the product's; the 6 statuses are the shipped set) — verify before assuming
  they are universal.

## Known gaps (deliberate, stated in the docs)

- The Edit Field dialog was captured for a built-in field (Duration); custom-field
  editors follow the same shape but their per-type option panels were not each
  enumerated.
- The condition/action builders in Task Form Rule take the form's own fields; exact
  option lists were not enumerated.
