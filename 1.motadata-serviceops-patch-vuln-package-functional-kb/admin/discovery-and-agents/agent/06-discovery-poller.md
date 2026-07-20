---
id: admin-discovery-poller
title: "Admin: Discovery Poller"
url: /admin/asset-management/agent?tab=discovery_poller
area: Admin / Discovery And Agents / Agent
page_type: list
captured: live (172.16.13.8, PMG ServiceOps)
source_server: 172.16.13.8
---

# Admin — Discovery Poller

## Purpose
**Configure the pollers that collect data from remote sites** — the probe machines that execute discovery scans and agent operations against a network segment/site.

## Access / Navigation
Admin → **Discovery And Agents → Agent → Discovery Poller**. URL: `/admin/asset-management/agent?tab=discovery_poller`.

## List
Search + download + **Poller Build** + **Settings** buttons. Table columns: **ID (POLLER-) · Host Name · IP Address · OS · Poller Version · Nmap Status · Last Sync Date · Agent Credential Profile · Actions** (delete). Each row has an online/offline status dot.

Captured row: **POLLER-1** · DESKTOP-K99KL00 · 10.20.41.210 · Microsoft Windows 10 Pro · Poller Version 8.7.500 · Nmap Status = Enabled (7.98) · Default credential profile.

## Relationships
- Poller selected on scans and agent jobs — [Admin: Discovery Service](../discovery/01-discovery-service.md) · [Admin: Network Scan](../discovery/02-network-scan.md) · [Admin: Agent Installation](01-agent-installation.md) · [Admin: Agents](04-agents.md)
- Poller Build = the poller binary (like Agent Build) — [Admin: Agent Build](02-agent-build.md)
