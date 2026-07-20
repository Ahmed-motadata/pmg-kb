---
id: admin-network-scan
title: "Admin: Network Scan"
url: /admin/asset-management/discovery?tab=networkscan
area: Admin / Discovery And Agents / Discovery
page_type: settings
captured: live; re-validated on 172.16.12.224 (PMG ServiceOps)
source_server: 172.16.12.224 (also seen on 172.16.13.8)
---

# Admin — Network Scan

## Purpose
Define scans that **scan on-prem networks to identify devices and assets** (agentless discovery over an IP range).

## Access / Navigation
Admin → **Discovery And Agents → Discovery → Network Scan**. URL: `/admin/asset-management/discovery?tab=networkscan`.

## List
**Import Ip network** + **Create Network scan** buttons; search. Table columns: **Name · IP Range Type · Discovery Scan · Polling Scan · Ping Scan · Created By · Actions**. The Discovery/Polling/Ping Scan columns show each schedule (e.g. "Not Scheduled"). Per-row **Actions**: schedule (📅), run-now, search/scan, copy, and a kebab (⋮) menu.

### Configured data (172.16.12.224)
3 network scans, all **Specific set of IPs**, created by shraddha, with Discovery/Polling/Ping Scan = **Not Scheduled**:
| Name | IP Range Type | Created |
|---|---|---|
| 172.16.13.46 | Specific set of IPs | Mon, Jul 20 2026 |
| Test 13.6 | Specific set of IPs | Mon, Jul 20 2026 |
| 11.1818 | Specific set of IPs | Sat, Jul 18 2026 |

## Create Network Scan Form (drawer)
- **Name** *(required)*
- **IP Range Type** — radio: **Entire Network / Specific IP Range / Specific set of IPs**
- **Authentication Preference** — radio: **Credential-Based / Credential-Less**
- **IP Range Start** *(required)*
- **Location** · **Department** — dropdowns
- **Exclude IPs** — textarea (+ **Import**)
- **Protocol Type** — radio: **STATIC / DHCP**
- **Description**
- **Credentials** — select (+ **Create Credentials**)
- **Poller** — select
- Actions: **Save** / **Cancel**

## Relationships
- Runs via Discovery Service — [Admin: Discovery Service](01-discovery-service.md)
- Credentials — [Admin: Credentials](../13-credentials.md)
- Poller — [Admin: Discovery Poller](../agent/06-discovery-poller.md)
- IP Range Location — [Admin: IP Range Location](../16-ip-range-location.md)
- Discovers endpoints — [Endpoint (Patch Computers)](../../../patches/03-patch-endpoints.md)
