---
id: package-endpoints
title: Endpoint (Package Scope)
url: /computer/packages_computers
area: Packages
page_type: list
detail_route: /computer/packages_computers/{id}
captured: live (172.16.15.185, PMG ServiceOps)
---

# Endpoint — Package Scope

## Purpose
The same managed-endpoint inventory as [Endpoint (Patch Computers)](../patches/03-patch-endpoints.md) and [Endpoint (Vulnerability Scope)](../vulnerabilities/04-vulnerability-endpoints.md), framed for package/registry deployment: default columns surface deployment-relevant attributes like **Language** and **Agent Version**. These are the machines targeted by Package and Registry deployments.

## Access / Navigation
Sidebar: **Packages → Endpoint**. URL: `/computer/packages_computers`. Page title is "Endpoints".

## View Selector (saved views)
Same 5 endpoint views: **All Endpoints** (default) · Highly Vulnerable Computers · Vulnerable Endpoints · Healthy Endpoints · Reboot Required Endpoints.

## Toolbar & Header Actions
Export · Download · Refresh · Column Selection · ⋮ (Auto Refresh Interval).

## Search / Filterable Fields
Same endpoint field set as [Endpoint (Patch Computers)](../patches/03-patch-endpoints.md) (14): ID · Activation Status · Host Name · IP Address · Poller · Credential Profile · OS Name · Version · Architecture · System Health · Remote Office · Last Logged In User · Tags · Reboot Required.

## Columns
**Pinned:** ID, Host Name.
**Default visible:** IP Address · OS Name · OS Version · Service Pack · Architecture · Remote Office · **Language** · **Agent Version**.
Additional columns via Column Selection (Asset ID, CI ID, Poller, System Health, Total/Software Vulnerabilities, etc.).

## Pagination
Items-per-page dropdown (default 25); "Showing X-Y of N Endpoints".

## Detail Page — `/computer/packages_computers/{id}`
Confirmed live (opened EP-1 at `/computer/packages_computers/1`): **identical** to the endpoint detail in [Endpoint (Patch Computers)](../patches/03-patch-endpoints.md) and [Endpoint (Vulnerability Scope)](../vulnerabilities/04-vulnerability-endpoints.md) — same header (Scan Now + ⋮), same summary fields, same 5 tabs (Vulnerabilities / Patches / Installation / Notes / Audit Trail, opening on Vulnerabilities), same **Other Info** panel (Asset ID, CI ID, Agent ID, Reboot Required, Agent Version, Poller, MAC Address, Domain Name, Remote Office, Last Logged In User, Language) and **Scan Info** panel (Patch Scan Date, Vulnerability Scan Date, Last Reboot Time). The three endpoint scopes share one detail page.

## Relationships
- Package Deployments (deploy to these endpoints) — [Package Deployments](01-package-deployments.md)
- Registry Deployments — [Registry Deployments](02-registry-deployments.md)
- Patch Endpoints (same machines, patch scope) — [Endpoint (Patch Computers)](../patches/03-patch-endpoints.md)
- Vulnerability Endpoints (same machines, vuln scope) — [Endpoint (Vulnerability Scope)](../vulnerabilities/04-vulnerability-endpoints.md)
