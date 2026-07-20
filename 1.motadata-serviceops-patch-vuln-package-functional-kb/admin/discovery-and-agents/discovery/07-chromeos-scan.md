---
id: admin-chromeos-scan
title: "Admin: ChromeOS Scan"
url: /admin/asset-management/discovery?tab=chromeos
area: Admin / Discovery And Agents / Discovery
page_type: settings
captured: live; re-validated on 172.16.12.224 (PMG ServiceOps)
source_server: 172.16.12.224 (also seen on 172.16.13.8)
validation: 172.16.12.224 — no ChromeOS scans configured; structure/columns confirmed.
---

# Admin — ChromeOS Scan

## Purpose
**Discover and inventory ChromeOS devices** (via Google Admin / ChromeOS management API).

## Access / Navigation
Admin → **Discovery And Agents → Discovery → ChromeOS Scan**. URL: `/admin/asset-management/discovery?tab=chromeos`.

## List
Search + **Create Chromeos scan** button. Table columns: **Name · Discovery Scan · Polling Scan · Created By · Actions**.

## Create Chromeos scan Form
Defines Name, Google/ChromeOS API credentials, poller, and scan schedule.

## Relationships
- Runs via Discovery Service — [Admin: Discovery Service](01-discovery-service.md)
- Credentials — [Admin: Credentials](../13-credentials.md)
