---
id: patch-view
title: Patch View
url: /vulnerability/patch-view
area: Vulnerabilities
page_type: list
detail_route: /vulnerability/patch-view/{id}
captured: live (172.16.15.185, PMG ServiceOps)
---

# Patch View

## Purpose
Patches seen from the **vulnerability angle**: each row is a patch (ID prefix **PCH-**) shown together with the CVEs it addresses — split into **Exploited CVEs** and **Non Exploited CVEs** — plus severity, category, and CVSS score. Lets security teams prioritize which patches to deploy based on the vulnerabilities they close.

## Access / Navigation
Sidebar: **Vulnerabilities → Patch View**. URL: `/vulnerability/patch-view`. (Page header reads "Vulnerabilities".)

## View Selector (saved views)
5 views (each pinnable): **Detected Vulnerability Patches** (default) · **Critical Vulnerability Patches** · **Reboot Required Patches** · **Approved Patches** · **Unapproved Patches**.

## Toolbar & Header Actions
Export (page↗) · Download (↓) · Refresh (↻) · Column Selection (▥) · ⋮ menu.

## Search / Filterable Fields
"Select field to search…" exposes **13** fields: Impacted Endpoints · KB Number · Title · Severity · Patch Category · Support URI · Release Date · Reboot Required · Approval Status · Exploited CVEs · Non Exploited CVEs · CVSS 3.1 Score · CVSS 3.1 Vector.

## Columns
**Default visible:** ID (PCH-) · Name · Severity · **Exploited CVEs** · **Non Exploited CVEs** · Category · CVSS 3.1 Score · Published Date. Additional columns available via the Column Selection panel (drag-reorder, checkboxes, Apply).

Notable: **Exploited CVEs** and **Non Exploited CVEs** cells list the actual CVE IDs (e.g. CVE-2017-11826), linking each patch to the vulnerabilities it resolves.

## Row Actions
Row opens the patch detail page under this area's route (`/vulnerability/patch-view/{id}`). A per-row **Delete** (🗑) action is available in the Actions column.

## Detail Page — `/vulnerability/patch-view/{id}`
Confirmed live (opened PCH-103). It is the **same patch detail page** as the Patches module, just served under the patch-view route:
- **Header:** back · patch code (PCH-N) + full title · previous/next arrows · **Decline** button · refresh · ⋮.
- **Summary fields:** Patch Category · Severity · Approval Status · Test Status · Release Date · KB Number · Superseded Status · Reference Url (external link). Plus editable **Tags**.
- **Patch Details:** description text.
- **Tabs (7):** Endpoint (sub-tabs Missing / Installed / Ignored; endpoint table with per-row Delete action) · Affected Products · File Details · Vulnerabilities · Installation · Audit Trail · Superseded.
- **Other Info side panel:** UUID · Architecture · Source (e.g. Patch Scanning) · Status (e.g. Published) · Download Status (e.g. Success) · Download On · Download Size · Reboot Required (Yes/No/May be) · Support Uninstallation · Approved By · Approved On · Patch Type · Created Date.

(Identical structure to the [Patches](../patches/01-patches-overview.md) detail page.)

## Pagination
Items-per-page dropdown (default 25); "Showing X-Y of N Vulnerabilities".

## Relationships
- Vulnerabilities / Detected CVEs (the CVEs referenced here) — [Detected CVEs](03-detected-cves.md) · [Vulnerabilities (Detected CVEs)](01-vulnerabilities-overview.md)
- Patches (shared PCH- records & detail) — [Patches](../patches/01-patches-overview.md)
- Patch Deployment (act on prioritized patches) — [Patch Deployment](../patches/02-patch-deployment.md)
- Vulnerability Endpoints — [Endpoint (Vulnerability Scope)](04-vulnerability-endpoints.md)
