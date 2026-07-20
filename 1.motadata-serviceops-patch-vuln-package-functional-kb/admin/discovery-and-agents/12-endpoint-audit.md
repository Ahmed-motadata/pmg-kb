---
id: admin-endpoint-audit
title: "Admin: Endpoint Audit"
url: /admin/asset-management/endpoint-management?tab=endpoint_audit
area: Admin / Discovery And Agents / Endpoint Management
page_type: audit-log
captured: live (172.16.13.8, PMG ServiceOps)
source_server: 172.16.13.8
---

# Admin — Endpoint Audit

## Purpose
Audit log for the endpoint-scope area — "Define and manage endpoints included for operations across available modules." Tracks endpoint-scope additions/removals and scope-policy changes.

## Access / Navigation
Admin → **Discovery And Agents → Endpoint Management → Endpoint Audit**. URL: `/admin/asset-management/endpoint-management?tab=endpoint_audit`.

## Layout
**Date-range** + **filter** + **refresh** + **download**. Table columns: **Event · Event Time · User · Change Summary · IP Address**. Read-only.

Captured (172.16.13.8): **50 events**, e.g. "Endpoint Scope Policy Updated — Enable Auto Add Endpoint Scope updated as Enabled…", "Update Endpoint Scope — Endpoint EP-24 has been added to Endpoint Scope."

## Relationships
- Records changes to Endpoint Scopes & Scope Policies — [Admin: Endpoint Scopes](10-endpoint-scopes.md) · [Admin: Scope Policies](11-scope-policies.md)
- Overlaps Agent Audit — [Admin: Agent Audit](agent/08-agent-audit.md)
