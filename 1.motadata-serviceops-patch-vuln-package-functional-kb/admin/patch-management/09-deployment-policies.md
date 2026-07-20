---
id: admin-deployment-policies
title: "Admin: Deployment Policies"
url: /admin/patch-management/deployment-management?tab=deployment_policy
area: Admin / Patch Management / Deployment Management
page_type: settings
captured: live (172.16.15.185, PMG ServiceOps)
---

# Admin — Deployment Policies

## Purpose
Define the **deployment policies** that set rules for **reboot, scheduling, and rollout** of patches. These are the policies selected in the "Deployment Policy" dropdown on Patch / Package / Registry deployment create forms.

## Access / Navigation
Admin → **Patch Management → Deployment Management → Deployment Policies**. URL: `/admin/patch-management/deployment-management?tab=deployment_policy`.

## List
**Create Deployment Policy** button. Table columns: **Name · Description · Actions** (edit / delete). Built-in policies captured live:
- **Now**
- **24x7 Deployment Policy – Startup Triggered** — deploy at system startup or during scan cycles within a continuous 24x7 window.
- **24x7 Deployment Policy – User Intervention Allowed** — 24x7 window, allowing end-users to skip deployment.
- **Business Hours Deployment – No Reboot** — deploy during business hours (10 AM–6 PM); no reboot enforced.

## Create / Edit Form (drawer)
- **Name** *(required)*
- **Description** (textarea)
- **Initial Deployment On** — radio: **System Start Up** / **On Next Scan Cycle**
- **Deployment Day** *(required)* — multi-select days (e.g. Sunday +6 = all days)
- **Deployment Time (From – To)** — start/end time pickers (e.g. 12:00 AM → 11:59 PM)
- **Reboot Policy** — radio: **Reboot** / **ShutDown** / **Do Nothing**
- **Stop system reboot or shutdown while Install/Uninstall process is running** — toggle
- **Show Notification** — toggle
- Actions: **Create** / **Cancel**

## Relationships
- Selected in deployment create forms — [Patch Deployment](../../patches/02-patch-deployment.md) · [Package Deployments](../../packages/01-package-deployments.md) · [Registry Deployments](../../packages/02-registry-deployments.md) · [Automatic Patch Deployment](../../patches/05-automatic-patch-deployment.md)
- Remote Offices — [Admin: Remote Offices](10-remote-offices.md)
- Computer Group — [Admin: Computer Group](11-computer-group.md)
