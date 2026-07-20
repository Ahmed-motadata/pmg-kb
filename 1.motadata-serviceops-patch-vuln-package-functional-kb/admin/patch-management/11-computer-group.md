---
id: admin-computer-group
title: "Admin: Computer Group"
url: /admin/patch-management/deployment-management?tab=computer_groups
area: Admin / Patch Management / Deployment Management
page_type: settings
detail_route: /admin/patch-management/create-computer-groups
captured: live (172.16.15.185, PMG ServiceOps)
---

# Admin — Computer Group

## Purpose
Group endpoints into named sets for **targeted patch deployment** (and for scoping decline policies). A computer group is a reusable collection of managed computers.

## Access / Navigation
Admin → **Patch Management → Deployment Management → Computer Group**. URL: `/admin/patch-management/deployment-management?tab=computer_groups`.

## List
**Create** button. Table columns: **Name · Description · Total Computers · Actions** (edit / delete). Example rows: **Head Office** — "Group of Head Office machines." · **Motadata**.

## Create / Edit Form — `/admin/patch-management/create-computer-groups`
Full-page form. Fields:
- **Name** *(required)*
- **Description** (textarea)
- **Managed Computers** *(required)* — table (Endpoint ID · Host Name · IP Address · Poller · Agent Credential Profile · OS Name · Version · Service Pack · Architecture · Remote Office · Actions) + **Add Computers**
- Action: **Create**

## Relationships
- Referenced by Patch Control decline policies — [Admin: Patch Control](05-patch-control.md)
- Targets for deployments — [Patch Deployment](../../patches/02-patch-deployment.md) · [Automatic Patch Deployment](../../patches/05-automatic-patch-deployment.md)
- Members are endpoints — [Endpoint (Patch Computers)](../../patches/03-patch-endpoints.md)
- Remote Offices — [Admin: Remote Offices](10-remote-offices.md)
