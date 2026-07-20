---
id: admin-agent-credential-profile
title: "Admin: Agent Credential Profile"
url: /admin/asset-management/agent?tab=agent_credential_profile
area: Admin / Discovery And Agents / Agent
page_type: settings
captured: live (172.16.13.8, PMG ServiceOps)
source_server: 172.16.13.8
---

# Admin — Agent Credential Profile

## Purpose
**Store credentials used by agents to access endpoints** — reusable credential profiles that the agent presents when communicating with / managing target machines.

## Access / Navigation
Admin → **Discovery And Agents → Agent → Agent Credential Profile**. URL: `/admin/asset-management/agent?tab=agent_credential_profile`.

## List
Search + "All" filter + refresh + **Add Credential Profile** button. A status badge shows **"Credential Profile Based Communication: Enforced"**. Table columns: **Name · Description · Enabled · Actions** (copy / edit / delete). Captured rows: **bvh**, **Default** ("Default Credential-Profile"), both enabled.

## Relationships
- Assigned on Agent Installation and Agents — [Admin: Agent Installation](01-agent-installation.md) · [Admin: Agents](04-agents.md)
- Also used by Discovery Poller — [Admin: Discovery Poller](06-discovery-poller.md)
- Distinct from scan Credentials — [Admin: Credentials](../13-credentials.md)
