---
id: admin-patch-audit
title: "Admin: Patch Audit"
url: /admin/patch-management/patch-settings?tab=patch_audit
area: Admin / Patch Management / Patch Administration
page_type: audit-log
captured: live (172.16.15.185, PMG ServiceOps)
---

# Admin — Patch Audit

## Purpose
Track **patch downloads, approvals, and configuration changes** — review patch deployment and sync history as an audit log.

## Access / Navigation
Admin → **Patch Management → Patch Administration → Patch Audit**. URL: `/admin/patch-management/patch-settings?tab=patch_audit`.

## Layout
- **Date-range** selector (e.g. Tue Jul 14 – Sun Jul 19) + **filter** icon + **refresh**.
- Table columns: **Event · Event Time · User · Change Summary · IP Address**.
- Read-only audit history.

## Relationships
- Records changes across Patch Administration settings — [Admin: Patch Repository](01-patch-repository.md) · [Admin: Patch Control](05-patch-control.md) · [Admin: File Server](03-file-server.md)
- Complements the per-patch Audit Trail tab — [Patches](../../patches/01-patches-overview.md)
