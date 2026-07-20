---
id: registry-deployments
title: Registry Deployments
url: /remote-deployment/registry_remote_deployment
area: Packages
page_type: list
detail_route: /remote-deployment/registry_remote_deployment/{id}
create_route: /remote-deployment/registry_remote_deployment/create
captured: live (172.16.15.185, PMG ServiceOps)
---

# Registry Deployments

## Purpose
Deploy **Windows registry changes** to endpoints via remote deployment jobs, using reusable **Registry Templates**. Same remote-deployment engine as [Package Deployments](01-package-deployments.md) and [Patch Deployment](../patches/02-patch-deployment.md). Deployment IDs use the **CDR-** prefix.

## Access / Navigation
Sidebar: **Packages → Registry Deployments**. URL: `/remote-deployment/registry_remote_deployment`.

## Page Layout
Title **Registry Deployments** + view selector ("Pending Deployments ▾"); filter row (★ + active filter chip + search); grid; footer.

## View Selector (saved views)
Same 6 views as the other deployment lists: **Pending / Draft / Canceled / Expired / All / Archived Deployments**.

## Toolbar & Header Actions
- **Refresh** (↻)
- **Column Selection** (▥)
- **Create Registry Deployment** (button)

## Filters
Default filter chip: **Status In [Ready to Deploy, In Progress]** (status values: Draft, Ready to Deploy, In Progress, Completed, Expired, Cancelled, Partial Completed).

## Columns
Default visible: **ID** (CDR-) · Name · Status · Install After · Expiry Date. (Column Selection panel for show/hide + reorder.) Example row: CDR-7 / "awertyu" / Ready to Deploy.

## Search / Filterable Fields
Standard deployment field set (as [Package Deployments](01-package-deployments.md)): ID · Name · Created By · Last Updated By · Deployment Policy · Configuration Type · Created Date · Last Updated Date · Install After · Expiry Date.

## Create Form — `/remote-deployment/registry_remote_deployment/create`
Full-page form. Header actions: **Publish** · **Save as Draft** · **Cancel**.
- **Name** *(required)*
- **Install After** — date/time
- **Expiry Date** — date/time (e.g. "Expires in 15 days")
- **Registry Templates** *(required)* — table (Name · Description · Actions) + **Add Templates** (pick predefined registry key/value templates to push)
- **Configuration Settings:**
  - **Deployment Policy** *(required)* — select
  - **Notify to** — recipient select
  - **Retry Failed Configuration** — toggle

(Unlike Package Deployment, there is no Install/Uninstall Configuration Type toggle — the payload is registry templates.)

## Detail Page — `/remote-deployment/registry_remote_deployment/{id}`
Opened via a CDR- row (captured live from CDR-7).
**Header:** back · deployment code (CDR-N) + name · refresh · **⋮ menu → Update Configuration · Cancel Deployment**. Sub-header: creator avatar/name · created date · **Configuration Type** tag (e.g. Install).

**Summary fields:** Status (e.g. Ready to Deploy) · Task Type (e.g. Manual Remote Deployment) · Deployment Policy (e.g. Now) · Install After · Expiry Date.

**Tabs (5):**
1. **Analytics** — KPI tiles **Success / Failed / In Progress / Other**; widgets: **Download Status** (summary + overall success rate), **OS Wise Registry Status** (N Total Devices Patched), **Status by Remote Office** (remote-office dropdown + Success/Failed/In Progress/Other + Total Installations).
2. **Endpoint** — target endpoints and their per-endpoint status.
3. **Registry** — the registry templates included in this deployment; search + table columns **Name · Description** (e.g. "Disable Winzip Updater" — "Disables the automatic updates of Winzip"); own pagination.
4. **Installation** — installation results/log.
5. **Audit Trail** — change history.

**Other Info side panel:** Notify to · Retry Failed Configuration (Enabled/Disabled) · Retry Count · Last Updated Date · Created By · Last Updated By.

## Relationships
- Package Deployments (same engine) — [Package Deployments](01-package-deployments.md)
- Package Endpoints (deployment targets) — [Endpoint (Package Scope)](03-package-endpoints.md)
- Patch Deployment (same remote-deployment engine) — [Patch Deployment](../patches/02-patch-deployment.md)
