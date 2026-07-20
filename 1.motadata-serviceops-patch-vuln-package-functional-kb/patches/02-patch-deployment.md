---
id: patch-deployment
title: Patch Deployment
url: /remote-deployment/patch_remote_deployment
area: Patches
page_type: list
detail_route: /remote-deployment/patch_remote_deployment/{id}
captured: live (172.16.15.185, PMG ServiceOps)
---

# Patch Deployment

## Purpose
Create and track **remote deployment jobs** that push approved patches to endpoints. Each deployment (ID prefix **PDR-**) targets a set of endpoints/patches with a policy and schedule, and reports per-endpoint install progress and analytics.

## Access / Navigation
Sidebar: **Patches → Patch Deployment**. URL: `/remote-deployment/patch_remote_deployment`.

## Page Layout
Title **Patch Deployments** + view selector ("Pending Deployments ▾"); filter row (saved-search ★ + active filter chip + search box); grid; footer pagination.

## View Selector (saved views)
6 views (each pinnable): **Pending Deployments** (default) · **Draft Deployments** · **Canceled Deployments** · **Expired Deployments** · **All Deployments** · **Archived Deployments**.

## Toolbar & Header Actions
| Control | Tooltip | Action |
|---------|---------|--------|
| ↻ | Refresh | Reload grid |
| ▥ | Column Selection | Show/hide + reorder columns |
| dark button | **Create Patch Deployment** | Start a new deployment job |

(No Export / Download icons on this page.)

## Filters
Default active filter chip: **Status In [Ready to Deploy, In Progress]**. Clicking it opens an operator + value editor.
**Status filter values (7):** Draft · Ready to Deploy · In Progress · Completed · Expired · Cancelled · Partial Completed.

## Search / Filterable Fields
"Select field to search…" exposes **10** fields: ID · Name · Created By · Last Updated By · Deployment Policy · Task Type · Created Date · Last Updated Date · Install After · Expiry Date.

## Columns
**Pinned:** ID, Name.
**Default visible (5):** Status · Deployment Policy · Total Installations · Install After · Expiry Date.
**Available (6):** Configuration Type · Created Date · Last Updated Date · Task Types · Created By · Last Updated By.
**Default: 7 · Total available: 13.** Panel has drag-reorder, checkboxes, search, **Apply**.

## Row Actions
Row (ID/Name) opens the deployment detail page.

## Create Patch Deployment Form — `/remote-deployment/patch_remote_deployment/create`
Opened by the **Create Patch Deployment** button (full-page form; captured live). Header actions: **Publish** · **Save as Draft** · **Cancel**. Fields:
- **Name** *(required)*
- **Install After** — date/time
- **Expiry Date** — date/time (e.g. "Expires in 15 days")
- **Configuration Type** — toggle **Install / Uninstall**
- **Patches** *(required)* — table (ID · Name · Patch Category · Severity · Approval Status · Application · Release Date · KB Number · Download Size · UUID · Actions) + **Add Patches**
- **Configuration Settings:**
  - **Deployment Policy** *(required)* — dropdown
  - **Notify to** — recipient select
  - **Retry Failed Configuration** — toggle

(Structure mirrors the [Package Deployments](../packages/01-package-deployments.md) create form; targeting is driven by the selected patches rather than an explicit target-computers picker.)

## Pagination
Items-per-page dropdown (default 25); count shown as "Showing X-Y of N Patch Deployments".

## Detail Page — `/remote-deployment/patch_remote_deployment/{id}`
**Header:** back · deployment code (PDR-N) + name · refresh · **⋮ menu → Cancel Deployment**. Sub-header: creator avatar/name · created date · **Configuration Type** tag (e.g. Install).

**Summary fields:** Status · Task Type (e.g. Manual Remote Deployment) · Deployment Policy (e.g. Now) · Install After · Expiry Date.

**Tabs (5)** — all captured live from PDR-3:
1. **Analytics** — KPI tiles **Success / Failed / In Progress / Other**; widgets: **Download Status** (summary + overall success rate), **OS Wise Patching Status**, **Patches Status by Severity**, **Patch Status by Category** (category dropdown, e.g. Tools), **Status by Remote Office** (remote-office dropdown + Total Patches).
2. **Endpoint** — target endpoints; search + table columns **Endpoint ID · Host Name · IP Address · Poller · Agent Credential · OS Name · Version · Service Pack · Architecture · Used By · System Health · Remote Office**. Paginated.
3. **Patches** — the patches bundled in this deployment; search + table columns **ID · Name · Patch Category · Severity · Approval Status · Application · Release Date · KB Number · Download Size · UUID**. Paginated (can be many rows).
4. **Installation** — per-patch-per-endpoint install results; search + table columns **Endpoint ID · Host Name · Patch ID · Name · Severity · Deployed Date · Installation Status · Retry Status · Download Status · Result · Actions** (empty until installs run).
5. **Audit Trail** — event timeline (actor · action · timestamp) with a **date-range filter** and **export**; e.g. "System has changed Status from Ready to Deploy to In Progress.", "yash has created Deployment Request PDR-3." Paginated.

**Other Info side panel:** Notify to (recipient select) · Retry Failed Configuration (Enabled/Disabled) · Retry Count · Last Updated Date · Created By · Last Updated By.

## Relationships
- Patches — [Patches](01-patches-overview.md)
- Patch Endpoints — [Endpoint (Patch Computers)](03-patch-endpoints.md)
- Automatic Patch Deployment — [Automatic Patch Deployment](05-automatic-patch-deployment.md)
- Package Deployments (same remote-deployment engine) — [Package Deployments](../packages/01-package-deployments.md)
- Registry Deployments (same engine) — [Registry Deployments](../packages/02-registry-deployments.md)
