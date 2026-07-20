---
id: patches
title: Patches
url: /patch
area: Patches
page_type: list
detail_route: /patch/{id}
captured: live (172.16.15.185, PMG ServiceOps)
---

# Patches

## Purpose
Master list of every patch ServiceOps knows about (from patch scanning and manual creation). Shows each patch's category, severity, approval/test status, and how many endpoints are missing vs. have it installed. Technicians approve, decline, download, and deploy patches from here.

## Access / Navigation
Sidebar: **Patches → Patches**. URL: `/patch`.

## Page Layout
Header shows title **Patches** with a **view selector** ("Missing Patches ▾"). Below is a filter row (saved-search star + active view chip + search box), then the data grid, then a footer with pagination and total count ("Showing 1-5 of 5 Patches").

## View Selector (saved views)
Dropdown with a search box and 5 predefined views (each pinnable):
1. **Missing Patches** (default)
2. **Installed Patches**
3. **Applicable Patches**
4. **Declined Patches**
5. **Manually Created Patches**

## Toolbar & Header Actions
Left → right:
| # | Control | Tooltip | Action |
|---|---------|---------|--------|
| 1 | page↗ icon | **Export** | Opens "Export Patches" drawer (see Export) |
| 2 | ↓ icon | **Download** | Download list |
| 3 | ↻ icon | **Refresh** | Reload grid |
| 4 | box↓ icon | **Download Patch** | Download the patch binary/content |
| 5 | ▥ grid icon | **Column Selection** | Opens column show/hide + reorder panel |
| 6 | dark button | **Create Patch** | Create a manually-defined patch |

Filter row also has a **Save Search** (★) button to save the current filter as a view.

## Filters / Searchable Fields
The "Select field to search…" box exposes **18** fields:
Patch ID · Name · UUID · Patch Type · Platform · Created By · Last Updated By · Patch Category · Severity · Approval Status · Test Status · Release Date · KB Number · Superseded Status · Download Status · Patch Source · Patch Status · Patch Upload Status

## Columns
**Pinned (always shown):** Patch ID, Name.
**Default visible (10, toggleable/reorderable):** Patch Category, Severity, Release Date, Missing Endpoint, Installed Endpoint, Patch Type, Download Size, Created By, Last Updated Date, Last Updated By.
**Available (off by default, 12):** Approval Status, Download Status, Approved On, Reboot Required, Support Uninstallation, Description, Test Status, Tags, Patch Status, Patch Source, Upload Status, UUID.

**Default columns: 12 · Total available: 24.** Column panel has drag-handles (reorder), checkboxes, a search box, and an **Apply** button.

## Row Actions
- Patch ID / Name link → detail page `/patch/{id}`
- On row hover, an **open-in-new-tab** (↗) icon appears next to the Patch ID.

## Bulk Actions (Take Action)
Selecting one or more rows shows a **"Take Action ▾"** bar ("Total N records selected · Unselect All"). Menu:
- **Download to File Server**
- **Approve** (✓)
- **Decline** (✗)

## Pagination
Items-per-page options: **10 / 25 / 50 / 100** (default 25). First/prev/next/last controls; count shown as "Showing X-Y of N Patches".

## Export
**Export Patches** drawer:
- **Format toggle:** CSV / Excel
- **Select All Fields** checkbox + per-field search
- Selectable fields include: Patch ID, Created Date, Last Updated Date, Last Updated By, Approval Status, Description, Tags, Created By, Approval Date, Name, Category, Severity, KB Number, Test Status, Download Status, Download Size(MB), Reference URL (list continues).

## Detail Page — `/patch/{id}`
**Header:** back arrow · patch code + full title · previous/next record arrows · refresh · **⋮ menu → Download to File Server**.

**Summary fields (top):** Patch Category · Severity · Approval Status · Test Status · Release Date · KB Number · Superseded Status · Reference Url (external link).

**Tags:** editable tag chips (add via +, remove via ✕).

**Patch Details:** description text block (expandable).

**Tabs (7)** — all captured live from PCH-116:
1. **Endpoint** — sub-tabs **Missing / Installed / Ignored**; endpoint table columns: Endpoint ID, Host Name, IP Address, Poller, Agent Credential, OS Name, Version, Service Pack, Architecture, Used By, System Health, Remote Office. Own search + pagination.
2. **Affected Products** — header "Supported Languages: <value>" (e.g. all); table columns **Name · Type** (e.g. "Microsoft Defender Antivirus" / "Application"). Paginated.
3. **File Details** — the actual patch binaries; table columns **Sr.No · File Name · Size · Language · Actions**. Per-row Actions: copy (URL) + download. (e.g. mpas-fe_amd64.exe · 148.22 MB · all.)
4. **Vulnerabilities** — sub-tabs **Approved / Declined**; search + CVE table columns **CVE ID · Title · Description · Exploit Status · Severity · Status · Vulnerability Type · Patch Availability** (empty for a definition/AV update with no CVEs).
5. **Installation** — deployment/installation records; search + table columns **Endpoint ID · Host Name · IP Address · Configuration Type · Deployment Date · Installation Status · Retry Status · Download Status · Task Type · Actions** (empty until deployed).
6. **Audit Trail** — chronological event timeline (actor avatar · action text · timestamp) with a **date-range filter** and **export** control; e.g. "yash has added Tags: no.", "System has found PCH-116 missing on computer EP-1.", "System has created Patch PCH-116." Paginated.
7. **Superseded** — sub-tabs **Superseded / Superseded By** (lists patches this one supersedes / that supersede it; empty when neither applies).

**Other Info side panel:** UUID · Architecture · Source (e.g. Patch Scanning) · Status (e.g. Published) · Download Status · Download On · Download Size · Reboot Required · Support Uninstallation · Approved By · Approved On · Patch Type · Created Date.

## Create Manual Patch Form — `/patch/create`
Opened by the **Create Patch** toolbar button (full-page form; captured live). Header actions: **Create** · **Cancel**. Fields:
- **Title** *(required)*
- **Description** (textarea)
- **Patch Category** *(required)* — dropdown
- **Severity** *(required)* — dropdown
- **KB Number** — text
- **Release Date** *(required)* — date/time picker
- **Reboot Required** *(required)* — dropdown
- **Support Uninstallation** — toggle
- **Architecture** *(required)* — dropdown
- **Reference URL** — text
- **Applications** — table (Name · Type · Actions) + **Add Applications**

## Relationships
- Patch Deployment — [Patch Deployment](02-patch-deployment.md)
- Patch Endpoints — [Endpoint (Patch Computers)](03-patch-endpoints.md)
- Automatic Patch Test — [Automatic Patch Test](04-automatic-patch-test.md)
- Automatic Patch Deployment — [Automatic Patch Deployment](05-automatic-patch-deployment.md)
- Patch View (Vulnerabilities) — [Patch View](../vulnerabilities/02-patch-view.md)
- Detail "Vulnerabilities" tab links patches to CVEs — [Detected CVEs](../vulnerabilities/03-detected-cves.md)
