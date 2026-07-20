---
id: admin-public-cloud-network
title: "Admin: Public Cloud Network"
url: /admin/asset-management/discovery?tab=cloudnetwork
area: Admin / Discovery And Agents / Discovery
page_type: settings
captured: live; re-validated on 172.16.12.224 (PMG ServiceOps)
source_server: 172.16.12.224 (also seen on 172.16.13.8)
validation: 172.16.12.224 — no public cloud networks configured; structure/columns confirmed.
---

# Admin — Public Cloud Network

## Purpose
**Discover assets on public cloud networks** (AWS / Azure / GCP etc.) via cloud-provider credentials.

## Access / Navigation
Admin → **Discovery And Agents → Discovery → Public Cloud Network**. URL: `/admin/asset-management/discovery?tab=cloudnetwork`.

## List
**Import Public Cloud Network** + **Create Public Cloud Network** buttons; search. Table columns: **Name · Cloud Type · Discovery Scan · Polling Scan · Created By · Actions**.

## Create Public Cloud Network Form
Create defines Name, **Cloud Type** (provider), provider credentials/keys, poller, and scan schedule (drawer form, same pattern as Network Scan).

## Relationships
- Runs via Discovery Service — [Admin: Discovery Service](01-discovery-service.md)
- Private Cloud counterpart — [Admin: Private Cloud Network](04-private-cloud-network.md)
- Credentials — [Admin: Credentials](../13-credentials.md)
