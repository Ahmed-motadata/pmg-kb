---
id: vulnerabilities
title: Vulnerabilities (Detected CVEs)
url: /vulnerability
area: Vulnerabilities
page_type: list
detail_route: /vulnerability/{id}
captured: live (172.16.15.185, PMG ServiceOps)
---

# Vulnerabilities — Detected CVEs

## Purpose
Central register of every CVE detected across endpoints by vulnerability scanning. Each row is a CVE with its severity, CWE mapping, CVSS score, exploit status, patch availability, and how many endpoints it impacts. This is the landing page for the **Vulnerabilities** sidebar area (page title is "Detected CVEs").

## Access / Navigation
Sidebar: **Vulnerabilities → Vulnerabilities** (and **Detected CVEs**). URL: `/vulnerability`. (In this build both items resolve to this Detected CVEs list.)

## View Selector (saved views)
7 views (each pinnable): **Detected Vulnerabilities** (default) · **Critical Vulnerabilities** · **Active Vulnerabilities** · **Resolved Vulnerabilities** · **Fixable Vulnerabilities** · **Exploited Vulnerabilities** · **Declined Vulnerability**.

## Toolbar & Header Actions
Export (page↗) · Download (↓) · Refresh (↻) · Column Selection (▥) · ⋮ menu.

## Search / Filterable Fields
"Select field to search…" exposes **18** fields: ID · Severity · Title · Description · Vulnerability Type · Status · Impacted Endpoints · CVSS 2.0 Score · CVSS 2.0 Vector · CVSS 3.0 Score · CVSS 3.0 Vector · CVSS 3.1 Score · CVSS 3.1 Vector · CVSS 4.0 Score · CVSS 4.0 Vector · Patch Availability · Exploit Status · Published Date.

## Columns
**Pinned:** CVE ID.
**Default visible (9):** Description · Severity · CWE ID · Impacted Endpoints · Patch Availability · CVSS 3.1 Score · Exploit Status · Published Date · Status.
**Available (off by default):** Title · Tags · CVSS 3.1 Vector · Last Updated Date · Reboot Required · Vulnerability Type · (plus other CVSS score/vector variants).
**Default: 10.** Panel: drag-reorder, checkboxes, search, **Apply**.

## Data / Pagination
Example dataset: **300 Detected CVEs** across **12 pages**. Items-per-page dropdown (default 25). Severity rendered as colored chips (High/Medium/…).

## Row / Bulk Actions
Row → CVE detail. Checkboxes support multi-select (bulk approve/decline). Hover shows open-in-new-tab (↗).

## Detail Page — `/vulnerability/{id}`
**Header:** back · CVE code + title · previous/next arrows · **Decline** button · refresh. Sub-header: published/detected date.

**Summary fields:** CWE ID · Status (e.g. Analyzed) · Severity · Approval Status (e.g. Approved) · Exploit Status · Patch Availability. Plus editable **Tags**.

**Vulnerability Details:** description text.

**Tabs (5):**
1. **Metrics** — **CVSS** block(s): Exploitability Score · Impact Score · Severity · Access Vector (full CVSS vector string) · Source (e.g. secure@microsoft.com) · Type (e.g. Primary). Supports CVSS 2.0/3.0/3.1/4.0.
2. **Endpoint** — impacted endpoints.
3. **Patches** — patches that remediate this CVE.
4. **References** — external advisory links.
5. **Audit Trail** — change history.

**Other Info side panel:** Published Date · Last Updated Date.

## Relationships
- Detected CVEs (same list) — [Detected CVEs](03-detected-cves.md)
- Patch View — [Patch View](02-patch-view.md)
- Endpoint (vulnerability scope) — [Endpoint (Vulnerability Scope)](04-vulnerability-endpoints.md)
- Patches (remediation) — [Patches](../patches/01-patches-overview.md)
- Patch Endpoints (Vulnerabilities tab lists these CVEs) — [Endpoint (Patch Computers)](../patches/03-patch-endpoints.md)
