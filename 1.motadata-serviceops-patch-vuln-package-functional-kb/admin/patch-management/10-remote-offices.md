---
id: admin-remote-offices
title: "Admin: Remote Offices"
url: /admin/patch-management/deployment-management?tab=remote_office
area: Admin / Patch Management / Deployment Management
page_type: settings
captured: live (172.16.15.185, PMG ServiceOps)
---

# Admin — Remote Offices

## Purpose
Configure **patch distribution for remote and branch offices**. Each remote office groups managed computers behind a File Server (and optional proxy) for localized patch delivery. This is the source of the "Remote Office" values (e.g. **Local Office**) shown across the endpoint lists.

## Access / Navigation
Admin → **Patch Management → Deployment Management → Remote Offices**. URL: `/admin/patch-management/deployment-management?tab=remote_office`.

## List
**Create Remote office** button. Table columns: **Name · Managed Computer · Proxy Server · File Server · Action**. Example row: **Local Office** · 4 managed computers · Proxy = --- · File Server = flotomate.

## Create / Edit Form (drawer)
- **Name** *(required)*
- **File Server** — dropdown (select the file server serving this office)
- **Description** (textarea)
- **Managed Computer** — table (Endpoint ID · Host Name · IP Address · Poller · …) to assign endpoints to this office.

## Relationships
- File Server — [Admin: File Server](03-file-server.md)
- Network Distribution (relay/bandwidth per office) — [Admin: Network Distribution](04-network-distribution.md)
- Endpoints tagged with Remote Office — [Endpoint (Patch Computers)](../../patches/03-patch-endpoints.md) · [Endpoint (Vulnerability Scope)](../../vulnerabilities/04-vulnerability-endpoints.md) · [Endpoint (Package Scope)](../../packages/03-package-endpoints.md)
- Deployment Policies target offices — [Admin: Deployment Policies](09-deployment-policies.md)
