---
id: admin-file-server
title: "Admin: File Server"
url: /admin/patch-management/patch-settings?tab=file_server
area: Admin / Patch Management / Patch Administration
page_type: settings
captured: live (172.16.15.185, PMG ServiceOps)
---

# Admin — File Server

## Purpose
Configure the **file servers used to distribute patches** to endpoints, manage patch cleanup/storage alerts, credential profiles for the servers, and the file-server build binaries.

## Access / Navigation
Admin → **Patch Management → Patch Administration → File Server**. URL: `/admin/patch-management/patch-settings?tab=file_server`.

## Tabs (4)
1. **Configuration** — cleanup & alert toggles:
   - **Remove Superseded Patches** — toggle
   - **Remove Older Patches** — toggle
   - **Notify On Space Over Utilization** — toggle
   - Actions: **Update** / **Cancel**
2. **Server List** — registered file servers. Search + "All" filter + refresh. Table columns: **Name · Host Name · IP Address · File Server Url · OS · Last Sync Date · Credential Profile · Version · Local File Server · Actions** (sync / edit / delete). Example row: flotomate · 172.16.15.185 · Ubuntu 24.04.1 LTS · v8.7.500 · Local File Server = Yes.
3. **Credential Profile** — **Add Credential Profile** button; search + "All" filter. Table columns: **Name · Description · Enabled · Actions** (copy / edit / delete). Example: Default — "Default File Server Credential-Profile".
4. **File Server Build** — **History** button; table columns: **Platform · Build · Actions**. Rows per platform (**Unix**, **Windows**) with **Attach Files** action to upload the build binary.

## Recommended Action
- **Patch Control** card → **Configure** (define rules for approving/excluding patches).

## Relationships
- Patch Repository (recommends File Server) — [Admin: Patch Repository](01-patch-repository.md)
- Patch Control — [Admin: Patch Control](05-patch-control.md)
- Distributes patches to endpoints for — [Patch Deployment](../../patches/02-patch-deployment.md)
