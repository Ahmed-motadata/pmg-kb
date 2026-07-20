---
id: patch-endpoints
title: Endpoint (Patch Computers)
url: /computer/patch_computers
area: Patches
page_type: list
detail_route: /computer/patch_computers/{id}
captured: live (172.16.15.185, PMG ServiceOps)
---

# Endpoint — Patch Computers

## Purpose
Inventory of all managed endpoints (computers) from the Patches perspective. Shows each machine's OS, architecture, remote office, and how many patches are installed, and is the launch point for scanning, patch status, and vulnerabilities on that machine. Endpoint IDs use the **EP-** prefix.

## Access / Navigation
Sidebar: **Patches → Endpoint**. URL: `/computer/patch_computers`.

## View Selector (saved views)
5 views (each pinnable): **All Endpoints** (default) · **Highly Vulnerable Computers** · **Vulnerable Endpoints** · **Healthy Endpoints** · **Reboot Required Endpoints**.

## Toolbar & Header Actions
Left → right: **Export** (page↗) · **Download** (↓) · **Refresh** (↻) · **Column Selection** (▥) · **⋮ menu → Auto Refresh Interval**.

## Search / Filterable Fields
"Select field to search…" exposes **14** fields: ID · Activation Status · Host Name · IP Address · Poller · Credential Profile · OS Name · Version · Architecture · System Health · Remote Office · Last Logged In User · Tags · Reboot Required.

## Columns
**Pinned:** ID, Host Name.
**Default visible (7):** IP Address · OS Name · OS Version · Service Pack · Architecture · Remote Office · Installed Patches.
**Available (off by default):** Asset ID · CI ID · Poller · Agent Version · Agent Credential Profile · System Health · Total Vulnerabilities · Software Vulnerabilities (list continues).
Panel: drag-reorder, checkboxes, search, **Apply**.

## Row / Status
Each row has an online/offline status dot. Hover shows an **open-in-new-tab** (↗) icon. Row opens the endpoint detail page.

## Pagination
Items-per-page dropdown (default 25); "Showing X-Y of N Endpoints".

## Detail Page — `/computer/patch_computers/{id}`
**Header:** back · status dot · endpoint code (EP-N) + host name · previous/next arrows · refresh · **Scan Now** button · ⋮ menu. Sub-header: last-scan timestamp.

**Summary fields:** System Health · Used By · Service Pack · IP Address · Host Name · Architecture · OS Name · OS Version. Plus editable **Tags**.

**Tabs (5):**
1. **Vulnerabilities** — sub-tabs **Approved / Declined**; CVE table columns: CVE ID, Description, Exploit Status, Severity, Status (e.g. Analyzed), Vulnerability Type (e.g. OS), Patch Availability, Reboot Required. Own search.
2. **Patches** — patches applicable/installed on this endpoint.
3. **Installation** — installation history.
4. **Notes** — technician notes.
5. **Audit Trail** — change history.

**Other Info side panel:** Asset ID (→ asset) · CI ID (→ CMDB) · Agent ID · Reboot Required · Agent Version · Poller · MAC Address · Domain Name · Remote Office · Last Logged In User · Language.

**Scan Info panel:** Patch Scan Date (+ status badge, e.g. Completed) · Vulnerability Scan Date (+ status) · Last Reboot Time.

## Relationships
- Patches — [Patches](01-patches-overview.md)
- Patch Deployment — [Patch Deployment](02-patch-deployment.md)
- Vulnerability Endpoints (same machines, vuln scope) — [Endpoint (Vulnerability Scope)](../vulnerabilities/04-vulnerability-endpoints.md)
- Package Endpoints — [Endpoint (Package Scope)](../packages/03-package-endpoints.md)
- Detail links to Asset & CMDB CI records
- Vulnerabilities tab links to CVEs — [Detected CVEs](../vulnerabilities/03-detected-cves.md)
