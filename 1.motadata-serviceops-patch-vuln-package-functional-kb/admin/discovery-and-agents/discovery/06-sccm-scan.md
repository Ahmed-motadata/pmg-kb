---
id: admin-sccm-scan
title: "Admin: SCCM Scan"
url: /admin/asset-management/discovery?tab=sccmscan
area: Admin / Discovery And Agents / Discovery
page_type: settings
captured: live; re-validated on 172.16.12.224 (PMG ServiceOps)
source_server: 172.16.12.224 (also seen on 172.16.13.8)
validation: 172.16.12.224 — no SCCM scans configured; structure/columns confirmed.
---

# Admin — SCCM Scan

## Purpose
**Import assets from Microsoft SCCM or MECM** (Configuration Manager) rather than scanning the network directly.

## Access / Navigation
Admin → **Discovery And Agents → Discovery → SCCM Scan**. URL: `/admin/asset-management/discovery?tab=sccmscan`.

## List
Search + **Create Sccm scan** button. Table columns: **Name · Authentication Type · Host name · Discovery Scan · Polling Scan · Created By · Actions**.

## Create Sccm scan Form
Defines Name, SCCM/MECM host, **Authentication Type**, credentials, poller, and scan schedule.

## Relationships
- Runs via Discovery Service — [Admin: Discovery Service](01-discovery-service.md)
- Credentials — [Admin: Credentials](../13-credentials.md)
- Imports assets/endpoints — [Endpoint (Patch Computers)](../../../patches/03-patch-endpoints.md)
