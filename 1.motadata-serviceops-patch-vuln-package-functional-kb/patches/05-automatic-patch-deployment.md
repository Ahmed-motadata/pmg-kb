---
id: automatic-patch-deployment
title: Automatic Patch Deployment
url: /patch/automatic-patch-deployment
area: Patches
page_type: list
captured: live (172.16.15.185, PMG ServiceOps)
---

# Automatic Patch Deployment

## Purpose
Policy-driven, **scheduled automatic deployment** of patches (ID prefix **APD-**). Each policy selects patches by category/severity/application and pushes them to targeted endpoints on a recurring schedule, with optional post-approval delay and retry. This is the "set-and-forget" counterpart to manual Patch Deployment.

## Access / Navigation
Sidebar: **Patches → Automatic Patch Deployment**. URL: `/patch/automatic-patch-deployment`.

## Page Layout
Config list (no view selector/search/columns). Title **Automatic Patch Deployments** + **Create Automatic Patch Deployment** button; grid; footer pagination.

## Columns
| Column | Notes |
|--------|-------|
| ID | APD-N |
| Name | policy name |
| Last Execution Time | timestamp |
| Next Execution Time | timestamp |
| Enable | on/off toggle (per row) |
| Actions | **Edit** (✎) · **Delete** (🗑) · **View** (👁) |

## Row Actions
Enable toggle · Edit (opens config drawer) · Delete · View.

## Create / Edit Form (drawer)
Titled "Edit Automatic Patch Deployment". Fields:

**Patch selection**
- **Name** *(required)*
- **Select Patch Category** *(required)* — multi-select chips (e.g. Critical Updates)
- **Patch Severity** — multi-select chips (e.g. Low +4)
- **Applications** — toggle **All applications** / **Include applications**

**Target computers**
- **Remote Offices** — table (Remote Office · Filter Applied · Action) + **Add Remote Office**
- **Computers** *(required)* — table (Endpoint ID · Host Name · IP Address · Poller · Agent Credential · OS Name · Version · Service Pack · Architecture · Remote Office · Actions) + **Add Computers**

**Configuration settings**
- **Deployment Policy** *(required)* — dropdown (e.g. "24x7 Deployment Policy – Startup Triggered")
- **Notify to** — recipient select
- **Expires After** — number + unit (e.g. 10 Days)
- **Deploy After Approval** — number of Days (e.g. 0)
- **Schedule Type** *(required)* — dropdown (e.g. Daily)
- **Start At** *(required)* — date/time picker
- **Time** — HH : MM
- **Retry Failed Configuration** — toggle

Footer: **Update** / **Cancel**.

## Pagination
Items-per-page dropdown (default 25); "Showing X-Y of N items".

## Relationships
- Patches — [Patches](01-patches-overview.md)
- Automatic Patch Test (validation gate before auto-deploy) — [Automatic Patch Test](04-automatic-patch-test.md)
- Patch Deployment (manual counterpart) — [Patch Deployment](02-patch-deployment.md)
- Patch Endpoints (deployment targets) — [Endpoint (Patch Computers)](03-patch-endpoints.md)
