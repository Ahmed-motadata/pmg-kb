---
id: admin-network-distribution
title: "Admin: Network Distribution"
url: /admin/patch-management/patch-settings?tab=network-distribution
area: Admin / Patch Management / Patch Administration
page_type: settings
captured: live (172.16.15.185, PMG ServiceOps)
---

# Admin — Network Distribution

## Purpose
Optimize **patch distribution across remote networks** — configure network settings for patch delivery, including bandwidth throttling and relay-server internet access.

## Access / Navigation
Admin → **Patch Management → Patch Administration → Network Distribution**. URL: `/admin/patch-management/patch-settings?tab=network-distribution`.

## Tabs (2)
1. **Bandwidth Utilization**
   - **Enable Bandwidth Utilization Limit** — toggle. Note: "*Enter 0 for unlimited download speed."
   - Actions: **Update** / **Cancel**
2. **Relay Server Settings**
   - **Allow Relay Server to Download Patch From Internet** — toggle
   - Actions: **Submit** / **Cancel**

## Relationships
- Remote Offices (relay servers per office) — [Admin: Remote Offices](10-remote-offices.md)
- File Server (patch distribution) — [Admin: File Server](03-file-server.md)
- Patch Deployment — [Patch Deployment](../../patches/02-patch-deployment.md)
