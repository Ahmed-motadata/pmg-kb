---
id: admin-scope-policies
title: "Admin: Scope Policies"
url: /admin/asset-management/endpoint-management?tab=scope_policies
area: Admin / Discovery And Agents / Endpoint Management
page_type: settings
captured: live (172.16.13.8, PMG ServiceOps)
source_server: 172.16.13.8
---

# Admin — Scope Policies

## Purpose
**Automatically include endpoints into scope based on defined conditions and rules** — the rule engine that auto-adds discovered endpoints to Endpoint Scopes when they match criteria.

## Access / Navigation
Admin → **Discovery And Agents → Endpoint Management → Scope Policies**. URL: `/admin/asset-management/endpoint-management?tab=scope_policies`.

## Settings
- **Auto Add Endpoint in Endpoint Scope** — toggle (on/off; captured = enabled).
- **Condition builder** — rows of *field · operator · value* (e.g. **OS Name · Contains · windows**) with **Add Condition**, **Add Condition Group**, and **Remove All Condition**.
- **Notify To** — recipient select.
- Actions: **Update** / **Cancel**.

## Relationships
- Auto-populates Endpoint Scopes — [Admin: Endpoint Scopes](10-endpoint-scopes.md)
- Policy changes logged in Endpoint Audit / Agent Audit — [Admin: Endpoint Audit](12-endpoint-audit.md) · [Admin: Agent Audit](agent/08-agent-audit.md)
