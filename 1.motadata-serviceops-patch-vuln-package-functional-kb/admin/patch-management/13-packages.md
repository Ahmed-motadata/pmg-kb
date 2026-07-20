---
id: admin-packages
title: "Admin: Packages (Builder)"
url: /admin/packages
area: Admin / Patch Management
page_type: settings
detail_route: /admin/packages/create
captured: live (172.16.15.185, PMG ServiceOps)
---

# Admin — Packages (Builder)

## Purpose
**Build and deploy custom software packages** to managed endpoints. This is the package catalog (ID prefix **PKG-**) that feeds the Package Deployments "Add Packages" picker.

## Access / Navigation
Admin → **Patch Management → Packages**. URL: `/admin/packages`.

## List
Search + **Add Package** button. Table columns: **ID · Name · Version · Architecture · Package Type · Vendor · OS Platform · Actions** (edit / delete). Example rows: **PKG-2** Zoho Assist (64 BIT · EXE · Windows), **PKG-1** Spotify (64 BIT · EXE · Windows).

## Add Package Form — `/admin/packages/create`
Full-page form. Header: **Add** / **Cancel**. Fields:
- **Name** *(required)* · **OS Platform** *(required)* (e.g. Windows)
- **Description**
- **Architecture** *(required)* · **Version** · **Vendor**
- **Package Details:**
  - **Package Type** — toggle: **MSI/MSP · EXE · Script · Zip** (form adapts to type)
  - **Package Location** — toggle: **Shared Directory · Local Directory**
  - **Shared Drive File Path** *(required)* — **Add Path**
- **MSI/MSP Installation** — MSI/MSP File Name *(required)* · Property Argument
- **MSI/MSP Uninstallation** — MSI/MSP File Name *(required)* · Property Argument
- **Pre Deployment** — **Add Pre Deployment Action**
- **Post Deployment** — post-install actions (continues below the fold)

## Relationships
- Packages feed Package Deployments (Add Packages) — [Package Deployments](../../packages/01-package-deployments.md)
- Deployed to endpoints — [Endpoint (Package Scope)](../../packages/03-package-endpoints.md)
- Registry Templates (sibling config) — [Admin: Registry Templates](14-registry-templates.md)
