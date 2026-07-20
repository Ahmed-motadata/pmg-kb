---
id: admin-discovery-and-agents-overview
title: "Admin: Discovery & Agents — Overview"
url: /admin (IT Operations → Discovery And Agents)
area: Admin / Discovery And Agents
page_type: overview
captured: live (172.16.13.8 + 172.16.12.224, PMG ServiceOps)
source_server: 172.16.13.8 (Discovery data re-validated on 172.16.12.224)
---

# Admin — Discovery & Agents (Overview)

The admin configuration surface for **Discovery And Agents**, under **Admin → IT Operations**. It is how endpoints get onto the platform — discovered on the network, given an agent, and placed in management scope — feeding the Patch / Vulnerability / Package modules.

## Structure

### Discovery (find devices on the network)
- **Discovery Service** — runs & monitors scans — [Admin: Discovery Service](discovery/01-discovery-service.md)
- **Network Scan** — IP-range on-prem scan — [Admin: Network Scan](discovery/02-network-scan.md)
- **Public Cloud Network** — AWS/Azure/GCP — [Admin: Public Cloud Network](discovery/03-public-cloud-network.md)
- **Private Cloud Network** — VMware/etc. — [Admin: Private Cloud Network](discovery/04-private-cloud-network.md)
- **Domain Scan** — AD/LDAP — [Admin: Domain Scan](discovery/05-domain-scan.md)
- **SCCM Scan** — import from SCCM/MECM — [Admin: SCCM Scan](discovery/06-sccm-scan.md)
- **ChromeOS Scan** — ChromeOS devices — [Admin: ChromeOS Scan](discovery/07-chromeos-scan.md)
- **DNS Configuration** — resolver DNS — [Admin: DNS Configuration](discovery/08-dns-configuration.md)
- **Discovery Preference Rule** — merge/create rules *(present on 172.16.12.224 only)* — [Admin: Discovery Preference Rule](discovery/09-discovery-preference-rule.md)

### Agent (deploy & manage the agent)
- **Agent Installation** — deploy agent to endpoints — [Admin: Agent Installation](agent/01-agent-installation.md)
- **Agent Build** — agent binaries per platform — [Admin: Agent Build](agent/02-agent-build.md)
- **Agent Installation History** — install/upgrade history — [Admin: Agent Installation History](agent/03-agent-installation-history.md)
- **Agents** — installed-agent inventory — [Admin: Agents](agent/04-agents.md)
- **Mobile Agents** — mobile-device agents — [Admin: Mobile Agents](agent/05-mobile-agents.md)
- **Discovery Poller** — poller/probe machines — [Admin: Discovery Poller](agent/06-discovery-poller.md)
- **Agent Credential Profile** — agent auth credentials — [Admin: Agent Credential Profile](agent/07-agent-credential-profile.md)
- **Agent Audit** — agent activity log — [Admin: Agent Audit](agent/08-agent-audit.md)

### Endpoint Management
- **Endpoint Scopes** — endpoints in management scope (EP-) — [Admin: Endpoint Scopes](10-endpoint-scopes.md)
- **Scope Policies** — auto-add rules — [Admin: Scope Policies](11-scope-policies.md)
- **Endpoint Audit** — scope change log — [Admin: Endpoint Audit](12-endpoint-audit.md)

### Shared config
- **Credentials** — scan credentials — [Admin: Credentials](13-credentials.md)
- **Discovery Pattern** — device classification (SSH/WMI/Nmap) — [Admin: Discovery Pattern](14-discovery-pattern.md)
- **SNMP Custom Properties** — OID→device-type DB — [Admin: SNMP Custom Properties](15-snmp-custom-properties.md)
- **IP Range Location** — IP→location mapping — [Admin: IP Range Location](16-ip-range-location.md)
- **Relationship Types** — CMDB dependency types — [Admin: Relationship Types](17-relationship-types.md)

## The pipeline (how it feeds the frontend)
1. **Discovery** scans (Network/Domain/Cloud/SCCM) find devices; **Discovery Pattern** + **SNMP Custom Properties** classify them; **Credentials** authenticate; **Discovery Poller** runs the probes; **IP Range Location** tags location; **Discovery Preference Rule** decides create-vs-update; **Relationship Types** wire dependencies.
2. **Agent Installation** (using **Agent Build** binaries + **Agent Credential Profile**) deploys the agent → machines appear in **Agents**.
3. **Scope Policies** auto-add matching machines to **Endpoint Scopes** → those are the managed **endpoints** ([Endpoint (Patch Computers)](../../patches/03-patch-endpoints.md) · [Endpoint (Vulnerability Scope)](../../vulnerabilities/04-vulnerability-endpoints.md) · [Endpoint (Package Scope)](../../packages/03-package-endpoints.md)) the Patch/Vulnerability/Package modules act on.
4. **Agent Audit** / **Endpoint Audit** record the activity.

## Server notes
Captured from **172.16.13.8** (has agent + endpoint-scope data: 12 agents, 23 endpoints, POLLER-1). Discovery submenu re-validated on **172.16.12.224** (has 3 network scans + 2 completed scans, and an extra **Discovery Preference Rule** page — a version difference). Cloud/Domain/SCCM/ChromeOS scans were empty on both.
