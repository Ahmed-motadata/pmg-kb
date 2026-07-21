# About this folder

Functional documentation of the **Support Channels** admin section of Motadata
ServiceOps, captured live from PMG ServiceOps (`http://172.16.15.185`) on 2026-07-20
using the `/functional-kb` skill. One file per page under `docs/`; `README.md` is the
index.

## Maintaining these docs

- Facts come from the live product, not guesses. To update, open the page in the app
  and re-check before editing.
- Keep the product's exact vocabulary — labels, statuses, button text — and list fixed
  choice-sets completely.
- Plain English, short sentences, tables for fields, no opinions or improvement ideas.
- Current toggle states ("On here") describe this tenant at capture time; when the
  tenant changes them, either update or drop the "here" values.
- The app's custom dropdowns only open on real user clicks right after a page render;
  when re-capturing option lists, click the select immediately after a fresh load or a
  form re-render, then read the accessibility tree.

## Known gaps (deliberate, stated in the docs)

- The Microsoft-provider variants of the email server forms need a real Microsoft
  sign-in and were not completed.
- The chat-flow conversation designer (behind a flow's name) was not captured.
- Exact option lists of some search pickers (rules condition/action fields, Technician
  Group, Category, Font Family) were not enumerated.
