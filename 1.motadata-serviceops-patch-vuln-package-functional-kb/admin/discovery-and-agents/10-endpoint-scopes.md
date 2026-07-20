---
id: admin-endpoint-scopes
title: "Admin: Endpoint Scopes"
url: /admin/asset-management/endpoint-management?tab=endpoint_scopes
area: Admin / Discovery And Agents / Endpoint Management
page_type: list
captured: live (172.16.13.8, PMG ServiceOps)
source_server: 172.16.13.8
---

# Admin — Endpoint Scopes

## Purpose
The master list of **endpoints included in management scope** (up to a licensed limit). "Track and review scope policy changes and automated endpoint inclusion activities via policies." Endpoints here are the machines eligible for patch/vulnerability/package management. Endpoint IDs use the **EP-** prefix.

## Access / Navigation
Admin → **Discovery And Agents → Endpoint Management → Endpoint Scopes**. URL: `/admin/asset-management/endpoint-management?tab=endpoint_scopes`.

## List
Header shows **Total End Points: N/limit** (e.g. 23/10000) + refresh + **Add Endpoints** button. Search ("Select field to search…"). Table columns: **Endpoint ID · Host Name · IP Address · Poller · OS Name · Agent Version · Agent Credential Profile · Service Pack · Architecture · Remote Office · Action** (delete). Each row has an online/offline status dot.

Captured (172.16.13.8): **23 endpoints** (EP-1…EP-24). Some have a full agent footprint (POLLER-1, OS, agent version 8.7.409/8.7.500, Default credential profile, 64 BIT); others are discovered-only (agent fields "---"). All Remote Office = Local Office.

## Relationships
- These are the managed endpoints — [Endpoint (Patch Computers)](../../patches/03-patch-endpoints.md) · [Endpoint (Vulnerability Scope)](../../vulnerabilities/04-vulnerability-endpoints.md) · [Endpoint (Package Scope)](../../packages/03-package-endpoints.md)
- Populated by Agents / Agent Installation — [Admin: Agents](agent/04-agents.md) · [Admin: Agent Installation](agent/01-agent-installation.md)
- Auto-inclusion governed by Scope Policies — [Admin: Scope Policies](11-scope-policies.md)
- Changes logged in Endpoint Audit + Agent Audit — [Admin: Endpoint Audit](12-endpoint-audit.md) · [Admin: Agent Audit](agent/08-agent-audit.md)
