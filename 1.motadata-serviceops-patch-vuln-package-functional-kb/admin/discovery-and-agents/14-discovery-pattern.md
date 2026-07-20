---
id: admin-discovery-pattern
title: "Admin: Discovery Pattern"
url: /admin/workflow-definition
area: Admin / Discovery And Agents
page_type: settings
captured: live (172.16.13.8, PMG ServiceOps)
source_server: 172.16.13.8
---

# Admin — Discovery Pattern

## Purpose
**Define patterns to identify and classify network devices** during discovery — the rules/probes that classify a discovered host (by protocol/behaviour) and drive how it is discovered.

## Access / Navigation
Admin → **Discovery And Agents → Discovery Pattern**. URL: `/admin/workflow-definition` (built on the workflow-definition engine).

## List
Search + "All" filter + **Create Discovery Pattern** button. Tabs: **Classification** / **Discovery**. Table columns: **Name · Description · Updated Date · Enabled · Actions** (copy).

Captured **Classification** patterns (all enabled):
- **SSH Classification** — identifies machines using SSH to execute remote commands.
- **WMI Classification** — identifies machines using WMI / WinRM to execute remote commands.
- **Nmap Classification** — identifies machines using Nmap.

## Relationships
- Applied by discovery scans to classify devices — [Admin: Network Scan](discovery/02-network-scan.md) · [Admin: Discovery Service](discovery/01-discovery-service.md)
- Uses the same underlying engine as Workflow (Automation)
