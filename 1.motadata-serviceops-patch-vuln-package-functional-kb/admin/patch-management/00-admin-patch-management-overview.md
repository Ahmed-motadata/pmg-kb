---
id: admin-patch-management-overview
title: "Admin: Patch Management — Overview"
url: /admin (IT Operations → Patch Management)
area: Admin / Patch Management
page_type: overview
captured: live (172.16.15.185, PMG ServiceOps)
---

# Admin — Patch Management (Overview)

The admin configuration surface for Patch Management, under **Admin → IT Operations → Patch Management**. It groups the settings that power the frontend Patches / Packages modules. Fourteen config pages across three groups plus three standalone items.

## Structure

### Patch Administration
- **Patch Repository** — sync local patch DB with Motadata Central Patch Repository — [Admin: Patch Repository](01-patch-repository.md)
- **Application Updates** — enable third-party app patching — [Admin: Application Updates](02-application-updates.md)
- **File Server** — patch distribution servers, cleanup, credentials, builds — [Admin: File Server](03-file-server.md)
- **Network Distribution** — bandwidth limits + relay server — [Admin: Network Distribution](04-network-distribution.md)
- **Patch Control** — approval policy + decline policies — [Admin: Patch Control](05-patch-control.md)
- **OS Vendor Patches** — RedHat + SUSE patch sources — [Admin: OS Vendor Patches](06-os-vendor-patches.md)
- **Deployment Notification** — deployment-status alert frequency — [Admin: Deployment Notification](07-deployment-notification.md)
- **Patch Audit** — audit log of patch changes — [Admin: Patch Audit](08-patch-audit.md)

### Deployment Management
- **Deployment Policies** — reboot/scheduling/rollout rules — [Admin: Deployment Policies](09-deployment-policies.md)
- **Remote Offices** — branch-office patch distribution — [Admin: Remote Offices](10-remote-offices.md)
- **Computer Group** — endpoint groups for targeting — [Admin: Computer Group](11-computer-group.md)

### Standalone
- **System Health Settings** — thresholds for Highly Vulnerable / Vulnerable tags — [Admin: System Health Settings](12-system-health-settings.md)
- **Packages** — custom software package builder (PKG-) — [Admin: Packages (Builder)](13-packages.md)
- **Registry Templates** — reusable registry configs — [Admin: Registry Templates](14-registry-templates.md)

## How admin config powers the frontend
- **Patch Repository + OS Vendor Patches + Application Updates** feed the patch database scanned by [Patches](../../patches/01-patches-overview.md) and [Endpoint (Patch Computers)](../../patches/03-patch-endpoints.md).
- **Patch Control** sets the Approval Status seen on [Patches](../../patches/01-patches-overview.md); **Test and Approve** ties to [Automatic Patch Test](../../patches/04-automatic-patch-test.md).
- **Deployment Policies** are the "Deployment Policy" dropdown in [Patch Deployment](../../patches/02-patch-deployment.md) / [Package Deployments](../../packages/01-package-deployments.md) / [Registry Deployments](../../packages/02-registry-deployments.md) / [Automatic Patch Deployment](../../patches/05-automatic-patch-deployment.md).
- **Remote Offices** + **Computer Group** provide the targeting used by deployments and the Remote Office column on endpoints.
- **File Server** + **Network Distribution** handle physical patch delivery/relay.
- **System Health Settings** defines the Healthy / Vulnerable / Highly Vulnerable classification and the matching saved views on the endpoint lists.
- **Packages** and **Registry Templates** are the payload catalogs for [Package Deployments](../../packages/01-package-deployments.md) and [Registry Deployments](../../packages/02-registry-deployments.md).

## Route patterns
- Patch Administration: `/admin/patch-management/patch-settings?tab=<name>`
- Deployment Management: `/admin/patch-management/deployment-management?tab=<name>`
- Standalone: `/admin/patch-management/system-health-settings`, `/admin/packages`, `/admin/registry-template`
