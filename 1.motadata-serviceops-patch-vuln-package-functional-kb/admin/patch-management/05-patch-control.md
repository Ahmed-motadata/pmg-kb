---
id: admin-patch-control
title: "Admin: Patch Control"
url: /admin/patch-management/patch-settings?tab=patch_control
area: Admin / Patch Management / Patch Administration
page_type: settings
captured: live (172.16.15.185, PMG ServiceOps)
---

# Admin — Patch Control

## Purpose
Approve, block, or defer specific patches — **define rules for approving patches and excluding (declining) patches**. Sets the global patch-approval mode and per-computer-group decline policies.

## Access / Navigation
Admin → **Patch Management → Patch Administration → Patch Control**. URL: `/admin/patch-management/patch-settings?tab=patch_control`.

## Tabs (2)
1. **Approval Policy** — **Patch Approval Policy** (radio, choose one):
   - **Pre Approved**
   - **Manually Approve**
   - **Test and Approve**
   Actions: **Update** / **Cancel**. (This drives the Approval Status seen on patches in the [Patches](../../patches/01-patches-overview.md) module.)
2. **Decline Policy** — **Create Patch Decline Policy** button; table columns **Name · Description · Computer Group · Action**. Decline policies exclude matching patches for a given computer group.

## Recommended Action
- **Deployment Management** card → **Configure**.

## Relationships
- Automatic Patch Test (Test and Approve path) — [Automatic Patch Test](../../patches/04-automatic-patch-test.md)
- Computer Group (decline policy scope) — [Admin: Computer Group](11-computer-group.md)
- Drives patch Approval Status — [Patches](../../patches/01-patches-overview.md)
- Deployment Management — [Admin: Deployment Policies](09-deployment-policies.md)
