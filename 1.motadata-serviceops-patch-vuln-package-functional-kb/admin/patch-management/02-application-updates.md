---
id: admin-application-updates
title: "Admin: Application Updates"
url: /admin/patch-management/patch-settings?tab=application_updates
area: Admin / Patch Management / Patch Administration
page_type: settings
captured: live (172.16.15.185, PMG ServiceOps)
---

# Admin — Application Updates

## Purpose
Enable and configure patching of **third-party applications** (non-OS software). Turning this on makes the Patch Repository also sync patch data for third-party apps so they can be scanned and deployed like OS patches.

## Access / Navigation
Admin → **Patch Management → Patch Administration → Application Updates**. URL: `/admin/patch-management/patch-settings?tab=application_updates`.

## Settings
**Third Party Patch Settings**
- **Activate the settings for third-party application patching preferences** — toggle (with an expand arrow that reveals preference options when enabled).
- Actions: **Update** / **Cancel**.

## Relationships
- Patch Repository (syncs third-party patch data) — [Admin: Patch Repository](01-patch-repository.md)
- Patches module — [Patches](../../patches/01-patches-overview.md)
