---
id: admin-agents
title: "Admin: Agents"
url: /admin/asset-management/agent?tab=agents
area: Admin / Discovery And Agents / Agent
page_type: list
captured: live (172.16.13.8, PMG ServiceOps)
source_server: 172.16.13.8
---

# Admin — Agents

## Purpose
**View and manage all installed agents** — the inventory of machines running the ServiceOps agent, with health, version, and upgrade status.

## Access / Navigation
Admin → **Discovery And Agents → Agent → Agents**. URL: `/admin/asset-management/agent?tab=agents`.

## Stat Tiles
- **Total Machines** (e.g. 12, with +N in the last 24 hours)
- **Agent Availability** — % + **Online / Offline** counts
- **Active Upgrades** — **In Progress / Queued** counts

## List
Search ("Select field to search…") + "All" filter + download + **Agent Actions** button (bulk actions on selected agents — e.g. upgrade/uninstall). Table columns: **ID (AGENT-) · Asset ID · Host Name · IP Address · Poller · OS · Version · Last Sync Date · Credential Profile · Architecture · Actions** (view / delete). Each row has an online/offline status dot.

Captured: 12 agents (mostly Linux — AlmaLinux, CentOS Stream, Oracle Linux, Debian, Fedora, Ubuntu — plus one Windows), on POLLER-1, agent versions 8.7.409 / 8.7.500, Default credential profile, 64 BIT.

## Agent Actions (drawer)
The **Agent Actions** button opens a drawer listing **batch agent-action jobs** (ID prefix **BAT-**): columns **ID · Name · Created By · Status · Created Date · Start Date** (e.g. BAT-3 "bhautik" Expired, BAT-2 "bhautik" Completed, BAT-1 "cred update" Expired). These are bulk operations run against agents (e.g. credential update, upgrade).

## Relationships
- Installed via Agent Installation — [Admin: Agent Installation](01-agent-installation.md)
- Agent binary from Agent Build — [Admin: Agent Build](02-agent-build.md)
- Uses Poller — [Admin: Discovery Poller](06-discovery-poller.md)
- Uses Agent Credential Profile — [Admin: Agent Credential Profile](07-agent-credential-profile.md)
- Agents = the managed endpoints — [Endpoint (Patch Computers)](../../../patches/03-patch-endpoints.md) · [Endpoint (Vulnerability Scope)](../../../vulnerabilities/04-vulnerability-endpoints.md)
