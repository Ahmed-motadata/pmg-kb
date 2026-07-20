---
id: admin-system-health-settings
title: "Admin: System Health Settings"
url: /admin/patch-management/system-health-settings
area: Admin / Patch Management
page_type: settings
captured: live (172.16.15.185, PMG ServiceOps)
---

# Admin — System Health Settings

## Purpose
Define the **criteria used to assess and tag endpoint health** — i.e. the missing-patch thresholds that classify a machine as **Highly Vulnerable**, **Vulnerable**, or (by exclusion) Healthy. These thresholds drive the System Health column and the "Highly Vulnerable Computers / Vulnerable Endpoints / Healthy Endpoints" saved views on the endpoint lists.

## Access / Navigation
Admin → **Patch Management → System Health Settings**. URL: `/admin/patch-management/system-health-settings`. Editable via the pencil (✎) icon.

## Criteria — "Highly Vulnerable"
Number of missing patches per severity that tags a system Highly Vulnerable (captured values):
- **Missing Critical Severity Patches:** 3
- **Missing Important Severity Patches:** 3
- **Missing Moderate Severity Patches:** 0
- **Missing Low Severity Patches:** 0

## Criteria — "Vulnerable"
- **Missing Critical Severity Patches:** 0
- **Missing Important Severity Patches:** 0
- **Missing Moderate Severity Patches:** 3
- **Missing Low Severity Patches:** 3
- **Consider Only Approved Patch** — toggle

## Relationships
- Drives System Health tag + saved views on endpoints — [Endpoint (Patch Computers)](../../patches/03-patch-endpoints.md) · [Endpoint (Vulnerability Scope)](../../vulnerabilities/04-vulnerability-endpoints.md)
- Severity comes from Patches — [Patches](../../patches/01-patches-overview.md)
