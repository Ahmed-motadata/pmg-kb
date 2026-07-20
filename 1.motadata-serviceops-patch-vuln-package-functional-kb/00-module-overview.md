---
id: patch-vuln-package-module
title: Patch, Vulnerability & Package Management
sidebar_position: 0
sidebar_label: Module Overview
module: ServiceOps Endpoint Management
captured: live (172.16.15.185, PMG ServiceOps)
---

# Patch, Vulnerability & Package Management — Module Overview

Three related endpoint-management areas in Motadata ServiceOps, reached from the left sidebar: **Vulnerabilities**, **Patches**, and **Packages**. All three operate over the same shared **Endpoint** inventory (the EP-* machines), viewed through different lenses.

## Sidebar Map (confirmed routes)

### Vulnerabilities
- **Vulnerabilities / Detected CVEs** — `/vulnerability` (page title "Detected CVEs") — [Vulnerabilities (Detected CVEs)](vulnerabilities/01-vulnerabilities-overview.md) · [Detected CVEs](vulnerabilities/03-detected-cves.md)
- **Endpoint** (vulnerability scope) — `/computer/endpoint_scope` — [Endpoint (Vulnerability Scope)](vulnerabilities/04-vulnerability-endpoints.md)
- **Patch View** (related route) — `/vulnerability/patch-view` — [Patch View](vulnerabilities/02-patch-view.md)

### Patches
- **Patches** — `/patch` — [Patches](patches/01-patches-overview.md)
- **Patch Deployment** — `/remote-deployment/patch_remote_deployment` — [Patch Deployment](patches/02-patch-deployment.md)
- **Endpoint** (patch scope) — `/computer/patch_computers` — [Endpoint (Patch Computers)](patches/03-patch-endpoints.md)
- **Automatic Patch Test** — `/patch/auto-patch-test` — [Automatic Patch Test](patches/04-automatic-patch-test.md)
- **Automatic Patch Deployment** — `/patch/automatic-patch-deployment` — [Automatic Patch Deployment](patches/05-automatic-patch-deployment.md)

### Packages
- **Package Deployments** — `/remote-deployment/packages_remote_deployment` — [Package Deployments](packages/01-package-deployments.md)
- **Registry Deployments** — `/remote-deployment/registry_remote_deployment` — [Registry Deployments](packages/02-registry-deployments.md)
- **Endpoint** (package scope) — `/computer/packages_computers` — [Endpoint (Package Scope)](packages/03-package-endpoints.md)

## How the areas relate

1. **Vulnerabilities** scans endpoints and produces **Detected CVEs**, each mapped to CWE, CVSS, and the patches that remediate it.
2. **Patch View** bridges the two: it lists patches (PCH-) with the Exploited / Non-Exploited CVEs they close, so teams prioritize by risk.
3. **Patches** is the master patch catalog; patches are approved, then pushed via **Patch Deployment** (manual, PDR-) or automated via **Automatic Patch Test** (APT-, validation) → **Automatic Patch Deployment** (APD-, scheduled rollout).
4. **Packages** deploys software (**Package Deployments**) and Windows registry changes (**Registry Deployments**, CDR-) through the same remote-deployment engine as patch deployment.
5. Every area has an **Endpoint** list backed by the same machines; the three scopes (`patch_computers`, `endpoint_scope`, `packages_computers`) differ only in default columns and which detail tab opens first.

## Shared Endpoint Inventory
All Endpoint lists share the base fields (ID, Host Name, IP Address, OS Name/Version, Service Pack, Architecture, Remote Office) and the same detail page (tabs: Vulnerabilities, Patches, Installation, Notes, Audit Trail; Scan Now action; Other Info + Scan Info panels). Default columns differ per scope: Patch scope → Installed Patches; Vulnerability scope → Total Vulnerabilities + Reboot Required; Package scope → Language + Agent Version.

## Cross-cutting patterns
- **List pages** share a view selector (saved views), a "Select field to search…" filter builder, a Column Selection panel (pinned + default + available columns), Export (CSV/Excel) / Download / Refresh toolbar, bulk **Take Action**, and 10/25/50/100 pagination.
- **Deployment pages** (patch/package/registry) share the 6 views (Pending/Draft/Canceled/Expired/All/Archived), the 7 status values, and the Analytics/Endpoint/Installation/Audit detail tabs.
