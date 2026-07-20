---
id: admin-os-vendor-patches
title: "Admin: OS Vendor Patches"
url: /admin/patch-management/patch-settings?tab=os_vendor_patches
area: Admin / Patch Management / Patch Administration
page_type: settings
captured: live (172.16.15.185, PMG ServiceOps)
---

# Admin — OS Vendor Patches

## Purpose
Configure **vendor-specific patch sources and policies** for Windows, macOS, and Linux — specifically RedHat and SUSE Enterprise Linux patch subscriptions/preferences.

## Access / Navigation
Admin → **Patch Management → Patch Administration → OS Vendor Patches**. URL: `/admin/patch-management/patch-settings?tab=os_vendor_patches`.

## Tabs (2)
1. **RedHat Patch Setting**
   - **RedHat Patch Preference** — radio: **Agent Nomination** / **RedHat Satellite Server**
   - Nomination table columns: **Endpoint ID · Host Name · Nomination Category · Last Sync Time · Repo Sync Status · Actions** (edit). Two nomination categories: **Server**, **Workstation**.
2. **SUSE Enterprise Linux Setting**
   - Setup guide: "Configure Suse Subscription" (sign in to SUSE Customer Center at scc.suse.com/subscriptions, select subscription (Desktop or Server), copy the Registration Code, paste it under the Action column).
   - Sub-tabs: **Configuration** / **Available Repositories**.
   - Configuration table columns: **OS Variant · Name · Expiry At · Last Sync Time · Actions**. OS Variants: **Server**, **Desktop**.

## Relationships
- Patch Repository (patch sync per OS) — [Admin: Patch Repository](01-patch-repository.md)
- Patch Endpoints (Linux endpoints) — [Endpoint (Patch Computers)](../../patches/03-patch-endpoints.md)
