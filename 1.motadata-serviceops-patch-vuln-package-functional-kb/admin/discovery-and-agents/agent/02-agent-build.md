---
id: admin-agent-build
title: "Admin: Agent Build"
url: /admin/asset-management/agent?tab=agent_build
area: Admin / Discovery And Agents / Agent
page_type: settings
captured: live (172.16.13.8, PMG ServiceOps)
source_server: 172.16.13.8
---

# Admin — Agent Build

## Purpose
**Package and version agent builds for deployment** — manage the agent installer binaries per platform/architecture that Agent Installation pushes to endpoints.

## Access / Navigation
Admin → **Discovery And Agents → Agent → Agent Build**. URL: `/admin/asset-management/agent?tab=agent_build`.

## Layout
Table columns: **Platform · Architecture · Agent Build · Actions** (edit to upload/update the build). Each row shows a ✓ + version if a build is present, or ✗ if not.

Captured rows:
| Platform | Architecture | Agent Build |
|---|---|---|
| Mac | All | ✓ 8.7.403 |
| Linux | 32 BIT | ✗ (none) |
| Linux | 64 BIT | ✓ 8.7.500 |
| Windows | 32 BIT | ✗ (none) |
| Windows | 64 BIT | ✗ (none) |

## Relationships
- Builds consumed by Agent Installation — [Admin: Agent Installation](01-agent-installation.md)
- Analogous to File Server Build (patch) — [Admin: File Server](../../patch-management/03-file-server.md)
