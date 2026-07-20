---
id: admin-ip-range-location
title: "Admin: IP Range Location"
url: /admin/asset-management/ip-range-location
area: Admin / Discovery And Agents
page_type: settings
captured: live (172.16.13.8, PMG ServiceOps)
source_server: 172.16.13.8
---

# Admin — IP Range Location

## Purpose
**Map IP address ranges to physical locations** — so discovered devices are automatically assigned a Location based on which IP range they fall in.

## Access / Navigation
Admin → **Discovery And Agents → IP Range Location**. URL: `/admin/asset-management/ip-range-location`.

## List
Search + import + **Add IP Range Location** button. Table columns: **From IP · To IP · Location · Actions** (edit / delete).

## Add IP Range Location
Defines **From IP**, **To IP**, and the **Location** the range maps to.

## Relationships
- Auto-assigns Location on discovered assets — [Admin: Network Scan](discovery/02-network-scan.md) · [Admin: Discovery Service](discovery/01-discovery-service.md)
- Location also selectable directly on a Network Scan — [Admin: Network Scan](discovery/02-network-scan.md)
