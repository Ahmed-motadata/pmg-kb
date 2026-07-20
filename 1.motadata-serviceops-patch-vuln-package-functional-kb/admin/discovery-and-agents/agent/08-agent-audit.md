---
id: admin-agent-audit
title: "Admin: Agent Audit"
url: /admin/asset-management/agent?tab=agent_audit
area: Admin / Discovery And Agents / Agent
page_type: audit-log
captured: live (172.16.13.8, PMG ServiceOps)
source_server: 172.16.13.8
---

# Admin — Agent Audit

## Purpose
**Track agent activity and configuration changes** — audit log of agent installs/upgrades, endpoint-scope changes, and agent policy updates.

## Access / Navigation
Admin → **Discovery And Agents → Agent → Agent Audit**. URL: `/admin/asset-management/agent?tab=agent_audit`.

## Layout
**Date-range** selector + **filter** + **refresh** + **download**. Table columns: **Event · Event Time · User · Change Summary · IP Address**. Read-only.

Captured (172.16.13.8): active log with **147 events**, e.g. "Endpoint Scope Policy Updated — Enable Auto Add Endpoint Scope updated as Enabled…", "Update Endpoint Scope — Endpoint EP-24 has been added to Endpoint Scope." (by bhautik, IP 10.20.41.121).

## Relationships
- Records changes across the Agent section — [Admin: Agent Installation](01-agent-installation.md) · [Admin: Agents](04-agents.md) · [Admin: Agent Credential Profile](07-agent-credential-profile.md)
- Endpoint-scope events relate to Endpoint Management — [Admin: Endpoint Scopes](../10-endpoint-scopes.md)
- Complements Patch/Vulnerability Audit — [Admin: Patch Audit](../../patch-management/08-patch-audit.md) · [Admin: Vulnerability Audit](../../vulnerability-management/02-vulnerability-audit.md)
