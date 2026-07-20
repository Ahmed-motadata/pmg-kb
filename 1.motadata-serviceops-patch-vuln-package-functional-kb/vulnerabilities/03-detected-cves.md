---
id: detected-cves
title: Detected CVEs
url: /vulnerability
area: Vulnerabilities
page_type: list
detail_route: /vulnerability/{id}
captured: live (172.16.15.185, PMG ServiceOps)
---

# Detected CVEs

## Purpose
The catalog of all CVEs detected across scanned endpoints. This is the primary list under the **Vulnerabilities** sidebar group — the page title is literally "Detected CVEs" and the URL is `/vulnerability`. It is the **same list** documented in [Vulnerabilities (Detected CVEs)](01-vulnerabilities-overview.md); this note captures the CVE-record perspective and detail.

## Access / Navigation
Sidebar: **Vulnerabilities → Detected CVEs**. URL: `/vulnerability`. (The Vulnerabilities group's list items are **Detected CVEs** and **Endpoint**; Patch View is a related sub-route — [Patch View](02-patch-view.md).)

## List Summary
See [Vulnerabilities (Detected CVEs)](01-vulnerabilities-overview.md) for the full breakdown. In brief:
- **View selector (7):** Detected / Critical / Active / Resolved / Fixable / Exploited / Declined Vulnerabilities.
- **Search fields (18):** ID, Severity, Title, Description, Vulnerability Type, Status, Impacted Endpoints, CVSS 2.0/3.0/3.1/4.0 Score + Vector, Patch Availability, Exploit Status, Published Date.
- **Default columns:** CVE ID (pinned) · Description · Severity · CWE ID · Impacted Endpoints · Patch Availability · CVSS 3.1 Score · Exploit Status · Published Date · Status.
- **Toolbar:** Export · Download · Refresh · Column Selection · ⋮.
- Example dataset: 300 CVEs / 12 pages, 25 per page.

## CVE Detail Page — `/vulnerability/{id}`
**Header:** back · CVE code + title · previous/next · **Decline** · refresh.
**Summary:** CWE ID · Status · Severity · Approval Status · Exploit Status · Patch Availability · Tags.
**Vulnerability Details:** description.
**Tabs (5):**
1. **Metrics** — CVSS block(s) (2.0/3.0/3.1/4.0): Exploitability Score, Impact Score, Severity, Access Vector string, Source (e.g. secure@microsoft.com), Type (e.g. Primary).
2. **Endpoint** — impacted endpoints.
3. **Patches** — remediating patches.
4. **References** — advisory links.
5. **Audit Trail**.
**Other Info:** Published Date · Last Updated Date.

## Relationships
- Vulnerabilities (same list) — [Vulnerabilities (Detected CVEs)](01-vulnerabilities-overview.md)
- Patch View (patches ↔ these CVEs) — [Patch View](02-patch-view.md)
- Endpoint (vulnerability scope) — [Endpoint (Vulnerability Scope)](04-vulnerability-endpoints.md)
- Patches (remediation) — [Patches](../patches/01-patches-overview.md)
- Patch Endpoints (Vulnerabilities tab shows these CVEs per machine) — [Endpoint (Patch Computers)](../patches/03-patch-endpoints.md)
