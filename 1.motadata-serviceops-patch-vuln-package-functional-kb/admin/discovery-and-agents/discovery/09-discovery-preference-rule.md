---
id: admin-discovery-preference-rule
title: "Admin: Discovery Preference Rule"
url: /admin/asset-management/discovery?tab=discovery_preference_rule
area: Admin / Discovery And Agents / Discovery
page_type: settings
captured: live (172.16.12.224, PMG ServiceOps)
source_server: 172.16.12.224
note: Present on 172.16.12.224 (9-item Discovery menu); absent from 172.16.13.8 (8-item menu — version difference).
---

# Admin — Discovery Preference Rule

## Purpose
**Define how discovered records are merged and updated** — the dedup/creation rules that decide whether a newly discovered device creates a new Asset/CI or updates an existing one, and by what matching preference.

## Access / Navigation
Admin → **Discovery And Agents → Discovery → Discovery Preference Rule**. URL: `/admin/asset-management/discovery?tab=discovery_preference_rule`.

## List
Tabs: **Asset** / **CI**. **Add Discovery Preference Rule** button. Table columns: **Name · Asset Type · CI Type · Creation Preference · Actions**.

## Add Discovery Preference Rule
Defines Name, target **Asset Type** / **CI Type**, and the **Creation Preference** (match/merge criteria that govern create-vs-update on discovery).

## Relationships
- Governs records created by all discovery scans — [Admin: Discovery Service](01-discovery-service.md) · [Admin: Network Scan](02-network-scan.md) · [Admin: Domain Scan](05-domain-scan.md)
- Feeds Assets/CIs into CMDB — [Endpoint (Patch Computers)](../../../patches/03-patch-endpoints.md)
