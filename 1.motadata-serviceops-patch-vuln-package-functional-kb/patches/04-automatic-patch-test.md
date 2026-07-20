---
id: automatic-patch-test
title: Automatic Patch Test
url: /patch/auto-patch-test
area: Patches
page_type: list
captured: live (172.16.15.185, PMG ServiceOps)
---

# Automatic Patch Test

## Purpose
Define automated **test policies** (ID prefix **APT-**) that deploy patches to a pilot/test set of endpoints, observe them for a defined period, and track approval before patches are rolled out broadly. This is the validation gate that feeds Automatic Patch Deployment.

## Access / Navigation
Sidebar: **Patches → Automatic Patch Test**. URL: `/patch/auto-patch-test`.

## Page Layout
Simple configuration list (no view selector, search, or column-selection tools). Title **Automatic Patch Tests** + **Create** button; grid; footer pagination.

## Toolbar & Header Actions
- **Create** — create a new automatic patch test policy.

## Columns
| Column | Notes |
|--------|-------|
| ID | APT-N |
| Name | test policy name |
| Total Tests | count |
| Pending Tests | count |
| Completed Tests | count |
| Last Execution Time | timestamp / --- |
| Next Execution Time | timestamp / --- |
| Enable | on/off toggle (per row) |
| Actions | **Edit** (✎) · **Delete** (🗑) · **View** (👁) |

## Row Actions
- **Enable** toggle — activate/deactivate the policy inline.
- **Edit** — opens the test detail drawer (see below).
- **Delete** — remove the policy.
- **View** — view the policy.

## Detail Drawer (Edit/View)
Titled "APT-N: <name>". Two tabs:
1. **Patch Deployment** — search box + a status filter (default **Pending**, with a filter icon). Table columns: ID, Name, Status, Test Status, Created Date, Observation Start Date, Remaining Approval (days), Actions.
2. **Analytics** — test outcome analytics.
Footer: **Done**.

## Pagination
Items-per-page dropdown (default 25); "Showing X-Y of N items".

## Relationships
- Patches — [Patches](01-patches-overview.md)
- Automatic Patch Deployment (consumes tested/approved patches) — [Automatic Patch Deployment](05-automatic-patch-deployment.md)
- Patch Deployment — [Patch Deployment](02-patch-deployment.md)
- Patch Endpoints (test targets) — [Endpoint (Patch Computers)](03-patch-endpoints.md)
