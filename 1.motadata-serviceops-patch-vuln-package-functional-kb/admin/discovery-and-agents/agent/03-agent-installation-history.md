---
id: admin-agent-installation-history
title: "Admin: Agent Installation History"
url: /admin/asset-management/agent?tab=agent_installation_history
area: Admin / Discovery And Agents / Agent
page_type: settings
captured: live (172.16.13.8, PMG ServiceOps)
source_server: 172.16.13.8
---

# Admin — Agent Installation History

## Purpose
**Review the history of agent installs and upgrades** — monitor running and completed agent-installation jobs.

## Access / Navigation
Admin → **Discovery And Agents → Agent → Agent Installation History**. URL: `/admin/asset-management/agent?tab=agent_installation_history`.

## Page Layout
- **Poller** — select dropdown.
- Tabs: **Running Agent Installation** / **Completed Agent Installation**.

## Tabs
1. **Running Agent Installation** — in-progress installs; **Refresh** + **Stop** controls.
2. **Completed Agent Installation** — history table of finished installs/upgrades.

## Relationships
- Tracks jobs created by Agent Installation — [Admin: Agent Installation](01-agent-installation.md)
- Uses Poller — [Admin: Discovery Poller](06-discovery-poller.md)
