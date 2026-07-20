---
id: admin-registry-templates
title: "Admin: Registry Templates"
url: /admin/registry-template
area: Admin / Patch Management
page_type: settings
captured: live (172.16.15.185, PMG ServiceOps)
---

# Admin — Registry Templates

## Purpose
Define reusable **registry configurations applied to endpoints**. These templates are the payload picked in the Registry Deployments "Add Templates" step — each encapsulates a Windows registry change (typically to disable a vendor's auto-update).

## Access / Navigation
Admin → **Patch Management → Registry Templates**. URL: `/admin/registry-template`.

## List
Search + **Add Registry Template** button. Table columns: **Name · Description · Actions** (edit). **23 predefined templates** captured, including:
- Disables Microsoft Reboot Notification · Disable Winzip Updater · Disable Windows OS Upgrade · Disable Windows Error Reporting · Disable Windows 10 Peer to Peer Update · Disable Windows 10 Notification · Disable Skype Updater · Disable Office 365 Updates · Disable CCleaner Updater · Disable Automatic Updates · Disable Automatic Java Updates · Disable Automatic Delivery of IE 11 · Disable Automatic Delivery of IE 10 · Disable Automatic App Updates · Disable Auto Update of Google Chrome · Disable Adobe Reader 9 updater · … (23 total).

## Add / Edit Registry Template
Opens an editor with **Name**, **Description**, and the registry key/value/type definition applied to the endpoint. (Edit icon per row.)

## Relationships
- Feed Registry Deployments (Add Templates) — [Registry Deployments](../../packages/02-registry-deployments.md)
- Applied to endpoints — [Endpoint (Package Scope)](../../packages/03-package-endpoints.md)
- Packages (sibling config) — [Admin: Packages (Builder)](13-packages.md)
