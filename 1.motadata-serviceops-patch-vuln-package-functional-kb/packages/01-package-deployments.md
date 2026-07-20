---
id: package-deployments
title: Package Deployments
url: /remote-deployment/packages_remote_deployment
area: Packages
page_type: list
detail_route: /remote-deployment/packages_remote_deployment/{id}
create_route: /remote-deployment/packages_remote_deployment/create
captured: live (172.16.15.185, PMG ServiceOps)
---

# Package Deployments

## Purpose
Deploy **software packages** (applications) to endpoints via remote deployment jobs — install or uninstall packaged software on a schedule. Uses the same remote-deployment engine as [Patch Deployment](../patches/02-patch-deployment.md) and [Registry Deployments](02-registry-deployments.md).

## Access / Navigation
Sidebar: **Packages → Package Deployments**. URL: `/remote-deployment/packages_remote_deployment`.

## Page Layout
Title **Package Deployments** + view selector ("Pending Deployments ▾"); filter row (★ + active filter chip + search); grid; footer. (Empty on the captured system — "No Data Found".)

## View Selector (saved views)
6 views (each pinnable): **Pending Deployments** (default) · **Draft Deployments** · **Canceled Deployments** · **Expired Deployments** · **All Deployments** · **Archived Deployments**.

## Toolbar & Header Actions
- **Refresh** (↻)
- **Column Selection** (▥)
- **Create Package Deployment** (button)

## Filters
Default filter chip: **Status In [Ready to Deploy, In Progress]** (same status value set as [Patch Deployment](../patches/02-patch-deployment.md): Draft, Ready to Deploy, In Progress, Completed, Expired, Cancelled, Partial Completed).

## Search / Filterable Fields
"Select field to search…" exposes **10** fields: ID · Name · Created By · Last Updated By · Deployment Policy · **Configuration Type** · Created Date · Last Updated Date · Install After · Expiry Date.

## Columns
Default visible: ID · Name · Status · Deployment Policy · Install After · Expiry Date · Created Date. (Column Selection panel for show/hide + reorder.)

## Create Form — `/remote-deployment/packages_remote_deployment/create`
Full-page form. Header actions: **Publish** · **Save as Draft** · **Cancel**.
- **Name** *(required)*
- **Install After** — date/time
- **Expiry Date** — date/time (e.g. "Expires in 15 days")
- **Configuration Type** — toggle **Install / Uninstall**
- **Packages** *(required)* — table (Packages ID · Name · Architecture · Packages Type · User Type · Action) + **Add Packages**
- **Configuration Settings:**
  - **Deployment Policy** *(required)* — select
  - **Notify to** — recipient select
  - **Retry Failed Configuration** — toggle

## Detail Page
Deployment detail (analogous to [Patch Deployment](../patches/02-patch-deployment.md) detail): summary, tabs (Analytics/Endpoint/Packages/Installation/Audit Trail), Other Info. (No records existed on the captured system to open.)

## Relationships
- Registry Deployments (same engine) — [Registry Deployments](02-registry-deployments.md)
- Package Endpoints (deployment targets) — [Endpoint (Package Scope)](03-package-endpoints.md)
- Patch Deployment (same remote-deployment engine) — [Patch Deployment](../patches/02-patch-deployment.md)
