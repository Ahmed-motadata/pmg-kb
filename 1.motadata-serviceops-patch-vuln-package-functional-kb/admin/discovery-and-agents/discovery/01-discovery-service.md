---
id: admin-discovery-service
title: "Admin: Discovery Service"
url: /admin/asset-management/discovery?tab=discovery_service
area: Admin / Discovery And Agents / Discovery
page_type: settings
captured: live; re-validated on 172.16.12.224 (PMG ServiceOps)
source_server: 172.16.12.224 (also seen on 172.16.13.8)
---

# Admin — Discovery Service

## Purpose
**Configure the service that runs discovery scans.** Central control point that runs the scan jobs defined by the other Discovery pages (Network/Domain/Cloud/SCCM/ChromeOS scans) and tracks their progress and results.

## Access / Navigation
Admin → **Discovery And Agents → Discovery → Discovery Service**. URL: `/admin/asset-management/discovery?tab=discovery_service` (base `/admin/asset-management/discovery` also resolves here).

## Page Layout
- **Poller** — select dropdown (choose which poller/probe runs the scans).
- Tabs: **Running Scan** / **Completed Scan**.

## Tabs
1. **Running Scan** — in-progress scans; **Refresh** + **Stop** controls.
2. **Completed Scan** — search + table columns: **Scan Name · Scan Type · Start Date · End Date · Submitted By · Status · Total Asset/CI · Pingable Asset/CI · Discovered Asset · Not Discovered · Type · Actions** (per-row **View History**).

### Configured data (172.16.12.224)
Two completed **Network** discovery scans (submitted by shraddha):
| Scan Name | Type | Status | Total | Pingable | Discovered | Not Discovered |
|---|---|---|---|---|---|---|
| 172.16.13.46 | Network / Discovery | Completed | 1 | 1 | 1 | 0 |
| Test 13.6 | Network / Discovery | Completed | 1 | 1 | 0 | 1 |

## Relationships
- Runs scans defined by — [Admin: Network Scan](02-network-scan.md) · [Admin: Domain Scan](05-domain-scan.md) · [Admin: SCCM Scan](06-sccm-scan.md) · [Admin: Public Cloud Network](03-public-cloud-network.md) · [Admin: Private Cloud Network](04-private-cloud-network.md) · [Admin: ChromeOS Scan](07-chromeos-scan.md)
- Uses Poller from — [Admin: Discovery Poller](../agent/06-discovery-poller.md)
- Discovers assets into CMDB / endpoints — [Endpoint (Patch Computers)](../../../patches/03-patch-endpoints.md)
- Credentials for scans — [Admin: Credentials](../13-credentials.md)
