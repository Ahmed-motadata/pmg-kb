---
id: admin-domain-scan
title: "Admin: Domain Scan"
url: /admin/asset-management/discovery?tab=domainscan
area: Admin / Discovery And Agents / Discovery
page_type: settings
captured: live; re-validated on 172.16.12.224 (PMG ServiceOps)
source_server: 172.16.12.224 (also seen on 172.16.13.8)
validation: 172.16.12.224 — no domain scans configured; structure/columns confirmed.
---

# Admin — Domain Scan

## Purpose
**Scan Active Directory or LDAP domains for users and devices** — directory-based discovery.

## Access / Navigation
Admin → **Discovery And Agents → Discovery → Domain Scan**. URL: `/admin/asset-management/discovery?tab=domainscan`.

## List
Search + **Create Domain scan** button. Table columns: **Name · Domain Name · Domain Controller Name · Discovery Scan · Polling Scan · Created By · Actions**.

## Create Domain scan Form
Defines Name, Domain Name, Domain Controller Name, credentials, poller, and scan schedule.

## Relationships
- Runs via Discovery Service — [Admin: Discovery Service](01-discovery-service.md)
- Credentials — [Admin: Credentials](../13-credentials.md)
- Imports users/devices — [Endpoint (Patch Computers)](../../../patches/03-patch-endpoints.md)
