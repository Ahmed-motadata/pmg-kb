# Motadata ServiceOps — Patch, Vulnerability & Package Management: Functional KB

A complete, plain-English functional guide to the **Patch, Vulnerability & Package
Management** areas of Motadata ServiceOps — every page, tab, button, field, and option, in
the product's own words. Captured live from PMG ServiceOps environments (172.16.15.185;
admin Discovery/Agent areas from 172.16.13.8, re-validated on 172.16.12.224). It describes
what the product is and does — it contains no opinions, comparisons, or improvement ideas.

Start with the [Module Overview](00-module-overview.md), then use the index below.

## Module Overview

| File | What it covers |
|---|---|
| [00-module-overview.md](00-module-overview.md) | How the three areas (Vulnerabilities, Patches, Packages) relate, the confirmed sidebar routes, the shared Endpoint inventory, and cross-cutting list/deployment patterns. |

## Vulnerabilities

| File | What it covers |
|---|---|
| [01-vulnerabilities-overview.md](vulnerabilities/01-vulnerabilities-overview.md) | Central register of every CVE detected across endpoints, with severity, CWE, CVSS, and exploit status. |
| [02-patch-view.md](vulnerabilities/02-patch-view.md) | Patches (PCH-) seen from the vulnerability angle — each patch with the Exploited / Non-Exploited CVEs it closes. |
| [03-detected-cves.md](vulnerabilities/03-detected-cves.md) | The "Detected CVEs" list page — columns, filters, views, and the CVE detail page. |
| [04-vulnerability-endpoints.md](vulnerabilities/04-vulnerability-endpoints.md) | The endpoint inventory in vulnerability scope — default columns surface Total Vulnerabilities and Reboot Required. |

## Patches

| File | What it covers |
|---|---|
| [01-patches-overview.md](patches/01-patches-overview.md) | Master catalog of every patch ServiceOps knows about — category, severity, approval/test status. |
| [02-patch-deployment.md](patches/02-patch-deployment.md) | Manual remote deployment jobs (PDR-) that push approved patches to endpoints — list, create form, and detail page. |
| [03-patch-endpoints.md](patches/03-patch-endpoints.md) | The endpoint inventory in patch scope — OS, architecture, remote office, and installed-patch counts. |
| [04-automatic-patch-test.md](patches/04-automatic-patch-test.md) | Automated test policies (APT-) that deploy patches to a pilot set of endpoints and track approval after an observation period. |
| [05-automatic-patch-deployment.md](patches/05-automatic-patch-deployment.md) | Policy-driven scheduled automatic deployment of patches (APD-) selected by category, severity, or application. |

## Packages

| File | What it covers |
|---|---|
| [01-package-deployments.md](packages/01-package-deployments.md) | Remote deployment jobs that install or uninstall software packages on endpoints. |
| [02-registry-deployments.md](packages/02-registry-deployments.md) | Remote deployment jobs (CDR-) that apply Windows registry changes to endpoints using Registry Templates. |
| [03-package-endpoints.md](packages/03-package-endpoints.md) | The endpoint inventory in package scope — default columns surface Language and Agent Version. |

## Admin — Vulnerability Management

| File | What it covers |
|---|---|
| [00-admin-vulnerability-management-overview.md](admin/vulnerability-management/00-admin-vulnerability-management-overview.md) | Map of the Vulnerability Management admin section and its tabs. |
| [01-vulnerability-database.md](admin/vulnerability-management/01-vulnerability-database.md) | Vulnerability database sync — updates, schedules, proxy, and notifications. |
| [02-vulnerability-audit.md](admin/vulnerability-management/02-vulnerability-audit.md) | Audit log of vulnerability database update activities and setting changes. |

## Admin — Patch Management

| File | What it covers |
|---|---|
| [00-admin-patch-management-overview.md](admin/patch-management/00-admin-patch-management-overview.md) | Map of the Patch Management admin section and its tabs. |
| [01-patch-repository.md](admin/patch-management/01-patch-repository.md) | Local patch repository sync with the Motadata Central Patch Repository. |
| [02-application-updates.md](admin/patch-management/02-application-updates.md) | Enabling and configuring patching of third-party (non-OS) applications. |
| [03-file-server.md](admin/patch-management/03-file-server.md) | File servers that distribute patches to endpoints — cleanup, storage alerts, and credential profiles. |
| [04-network-distribution.md](admin/patch-management/04-network-distribution.md) | Patch distribution across remote networks — bandwidth throttling and relay-server settings. |
| [05-patch-control.md](admin/patch-management/05-patch-control.md) | Rules for approving, blocking, or deferring patches — the global patch-approval mode. |
| [06-os-vendor-patches.md](admin/patch-management/06-os-vendor-patches.md) | Vendor-specific patch sources for Windows, macOS, and Linux (RedHat / SUSE subscriptions). |
| [07-deployment-notification.md](admin/patch-management/07-deployment-notification.md) | Recurring alerts to users and technicians about patch deployment status. |
| [08-patch-audit.md](admin/patch-management/08-patch-audit.md) | Audit log of patch downloads, approvals, and configuration changes. |
| [09-deployment-policies.md](admin/patch-management/09-deployment-policies.md) | Deployment policies — reboot, scheduling, and rollout rules picked in deployment forms. |
| [10-remote-offices.md](admin/patch-management/10-remote-offices.md) | Remote/branch offices grouping computers behind a File Server for localized patch distribution. |
| [11-computer-group.md](admin/patch-management/11-computer-group.md) | Named endpoint groups for targeted deployment and decline-policy scoping. |
| [12-system-health-settings.md](admin/patch-management/12-system-health-settings.md) | Missing-patch thresholds that classify endpoints as Highly Vulnerable / Vulnerable / Healthy. |
| [13-packages.md](admin/patch-management/13-packages.md) | The package builder and catalog (PKG-) that feeds Package Deployments. |
| [14-registry-templates.md](admin/patch-management/14-registry-templates.md) | Reusable registry configurations used as the payload of Registry Deployments. |

## Admin — Discovery And Agents

| File | What it covers |
|---|---|
| [00-admin-discovery-and-agents-overview.md](admin/discovery-and-agents/00-admin-discovery-and-agents-overview.md) | Map of the Discovery And Agents admin section and its tabs. |
| [10-endpoint-scopes.md](admin/discovery-and-agents/10-endpoint-scopes.md) | The master list of endpoints included in management scope (up to the licensed limit). |
| [11-scope-policies.md](admin/discovery-and-agents/11-scope-policies.md) | Rules that automatically include discovered endpoints into scope. |
| [12-endpoint-audit.md](admin/discovery-and-agents/12-endpoint-audit.md) | Audit log of endpoint-scope additions, removals, and policy changes. |
| [13-credentials.md](admin/discovery-and-agents/13-credentials.md) | Reusable credential records (SSH, SNMP, WMI, …) used by network scanning. |
| [14-discovery-pattern.md](admin/discovery-and-agents/14-discovery-pattern.md) | Patterns that identify and classify network devices during discovery. |
| [15-snmp-custom-properties.md](admin/discovery-and-agents/15-snmp-custom-properties.md) | SNMP System OID → device type mappings used to classify discovered devices. |
| [16-ip-range-location.md](admin/discovery-and-agents/16-ip-range-location.md) | IP-range → physical location mappings that auto-assign a Location to discovered devices. |
| [17-relationship-types.md](admin/discovery-and-agents/17-relationship-types.md) | The dictionary of asset/CI relationship types (direct + inverse name pairs). |

### Discovery

| File | What it covers |
|---|---|
| [01-discovery-service.md](admin/discovery-and-agents/discovery/01-discovery-service.md) | The service that runs discovery scans — central control point for all scan jobs. |
| [02-network-scan.md](admin/discovery-and-agents/discovery/02-network-scan.md) | Agentless on-prem network scans over an IP range. |
| [03-public-cloud-network.md](admin/discovery-and-agents/discovery/03-public-cloud-network.md) | Asset discovery on public cloud networks via cloud-provider credentials. |
| [04-private-cloud-network.md](admin/discovery-and-agents/discovery/04-private-cloud-network.md) | Asset discovery on private cloud environments via hypervisor/API credentials. |
| [05-domain-scan.md](admin/discovery-and-agents/discovery/05-domain-scan.md) | Active Directory / LDAP domain scans for users and devices. |
| [06-sccm-scan.md](admin/discovery-and-agents/discovery/06-sccm-scan.md) | Importing assets from Microsoft SCCM / MECM instead of scanning directly. |
| [07-chromeos-scan.md](admin/discovery-and-agents/discovery/07-chromeos-scan.md) | Discovering and inventorying ChromeOS devices. |
| [08-dns-configuration.md](admin/discovery-and-agents/discovery/08-dns-configuration.md) | DNS servers used to resolve discovered hosts during scans. |
| [09-discovery-preference-rule.md](admin/discovery-and-agents/discovery/09-discovery-preference-rule.md) | Merge/dedup rules deciding whether a discovered device creates a new Asset/CI or updates one. |

### Agent

| File | What it covers |
|---|---|
| [01-agent-installation.md](admin/discovery-and-agents/agent/01-agent-installation.md) | Remotely pushing and installing the ServiceOps agent onto target machines. |
| [02-agent-build.md](admin/discovery-and-agents/agent/02-agent-build.md) | Agent installer builds per platform/architecture that Agent Installation deploys. |
| [03-agent-installation-history.md](admin/discovery-and-agents/agent/03-agent-installation-history.md) | History of running and completed agent-installation jobs. |
| [04-agents.md](admin/discovery-and-agents/agent/04-agents.md) | Inventory of all installed agents with health, version, and upgrade status. |
| [05-mobile-agents.md](admin/discovery-and-agents/agent/05-mobile-agents.md) | Inventory of ServiceOps mobile agent installs. |
| [06-discovery-poller.md](admin/discovery-and-agents/agent/06-discovery-poller.md) | Poller/probe machines that execute discovery scans against a network segment. |
| [07-agent-credential-profile.md](admin/discovery-and-agents/agent/07-agent-credential-profile.md) | Credential profiles agents use to access and manage target machines. |
| [08-agent-audit.md](admin/discovery-and-agents/agent/08-agent-audit.md) | Audit log of agent installs, upgrades, and agent policy changes. |
