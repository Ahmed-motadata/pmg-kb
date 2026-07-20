---
id: admin-patch-repository
title: "Admin: Patch Repository"
url: /admin/patch-management/patch-settings?tab=patch_repository
area: Admin / Patch Management / Patch Administration
page_type: settings
captured: live (172.16.15.185, PMG ServiceOps)
---

# Admin — Patch Repository

## Purpose
Manage the local repository of downloaded patches. **Patch Repository synchronises the local patch database with the Motadata Central Patch Repository** — pulling the latest patch vulnerability data for the selected OS platforms and configured Patch Categories, plus third-party application patch data (from Application Updates). An up-to-date patch database is required **before endpoints can be scanned for missing patches and before any Patch Deployment can be initiated.**

## Access / Navigation
Admin → **Patch Management → Patch Administration → Patch Repository**. URL: `/admin/patch-management/patch-settings?tab=patch_repository`.

## Page Layout
Header status strip: **Last Sync** timestamp · **Last Sync status** (e.g. "Failed - Manual") · **Update Now** button. Main "Set Up the Patch Database" form. Right side: **Patch Repository Guide** panel (Overview, Prerequisites). Bottom: **Recommended Action** card.

## Set Up the Patch Database (form)
- **Enable** — toggle
- **Notify To** — recipient select
- **Proxy Server** — dropdown
- **Patch Categories** *(required)* — multi-select. Options (**9**): Service Packs · Feature Packs · Updates · Security Updates · Critical Updates · Definition Updates · Hotfix · Update Rollups · Tools (with "Select All Items").
- **Patch Sync for OS** *(required)* — multi-select (Windows + others; e.g. Windows +1)
- Actions: **Update** / **Cancel**

## Header Actions
- **Update Now** — trigger an immediate sync with the central repository.

## Recommended Action
- **File Server** card → **Configure** (link to File Server settings for patch storage/distribution).

## Guide Panel
Right-side **Patch Repository Guide**: **Overview** (description above) and **Prerequisites** (expandable setup requirements for patch sync).

## Relationships
- File Server (patch storage) — [Admin: File Server](03-file-server.md)
- Application Updates (third-party patch sync) — [Admin: Application Updates](02-application-updates.md)
- Feeds the Patches module — [Patches](../../patches/01-patches-overview.md)
- Required before Patch Deployment — [Patch Deployment](../../patches/02-patch-deployment.md)
