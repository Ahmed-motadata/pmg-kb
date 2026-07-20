---
id: admin-relationship-types
title: "Admin: Relationship Types"
url: /admin/asset-management/asset-relationship-types
area: Admin / Discovery And Agents
page_type: settings
captured: live (172.16.13.8, PMG ServiceOps)
source_server: 172.16.13.8
---

# Admin — Relationship Types

## Purpose
**Define dependency relationships between assets and CIs** — the dictionary of relationship types (each a direct + inverse name pair) used to link CMDB records into a dependency map.

## Access / Navigation
Admin → **Discovery And Agents → Relationship Types**. URL: `/admin/asset-management/asset-relationship-types`.

## List
Search + **Add Relationship Type** button. Table columns: **ID · Direct Relationship Name · Inverse Relationship Name · Description · Action**.

Captured (172.16.13.8): **24 relationship types** (out-of-box), each direct ↔ inverse:
Depends On/Used By · Users/Used By · Send Data to/Received Data from · Runs/Runs On · Connected to/Connected to · Subscribes to/Subscribed by · Impacts/Impacted By · Submits/Submitted By · Supports/Supported By · Author of/Written By · Hosted On/Hosts · Enables/Is Enabled By · Includes/Member of · Contains/In Rack · Located In/Houses · Exchanges data with/Exchanges data with · Managed by/Manages · … (24 total).

## Relationships
- Relationships discovered/created on assets & CIs (CMDB) — [Endpoint (Patch Computers)](../../patches/03-patch-endpoints.md)
- Discovered dependencies come from discovery scans — [Admin: Discovery Service](discovery/01-discovery-service.md)
