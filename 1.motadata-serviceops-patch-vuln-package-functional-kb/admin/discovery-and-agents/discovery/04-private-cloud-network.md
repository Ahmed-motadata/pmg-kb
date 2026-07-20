---
id: admin-private-cloud-network
title: "Admin: Private Cloud Network"
url: /admin/asset-management/discovery?tab=private_cloud_network
area: Admin / Discovery And Agents / Discovery
page_type: settings
captured: live; re-validated on 172.16.12.224 (PMG ServiceOps)
source_server: 172.16.12.224 (also seen on 172.16.13.8)
validation: 172.16.12.224 — no private cloud networks configured; structure/columns confirmed.
---

# Admin — Private Cloud Network

## Purpose
**Discover assets on private cloud environments** (e.g. VMware, Nutanix, OpenStack) via hypervisor/API credentials.

## Access / Navigation
Admin → **Discovery And Agents → Discovery → Private Cloud Network**. URL: `/admin/asset-management/discovery?tab=private_cloud_network`.

## List
**Import Private Cloud Network** + **Create Private Cloud Network** buttons; search. Table columns: **Name · Private Cloud Type · Discovery Scan · Polling Scan · Created By · Actions**.

## Create Private Cloud Network Form
Defines Name, **Private Cloud Type**, connection endpoint, credentials, poller, and scan schedule.

## Relationships
- Runs via Discovery Service — [Admin: Discovery Service](01-discovery-service.md)
- Public Cloud counterpart — [Admin: Public Cloud Network](03-public-cloud-network.md)
- Credentials — [Admin: Credentials](../13-credentials.md)
