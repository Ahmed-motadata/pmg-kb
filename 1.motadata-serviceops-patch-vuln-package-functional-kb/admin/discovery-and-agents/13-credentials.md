---
id: admin-credentials
title: "Admin: Credentials"
url: /admin/asset-management/credentials
area: Admin / Discovery And Agents
page_type: settings
captured: live (172.16.13.8 / 172.16.12.224, PMG ServiceOps)
source_server: 172.16.13.8
---

# Admin — Credentials

## Purpose
**Store and manage credentials used for network scanning** — reusable credential records (SSH, SNMP, WMI, etc.) that discovery scans present to reach and inventory target devices.

## Access / Navigation
Admin → **Discovery And Agents → Credentials**. URL: `/admin/asset-management/credentials`.

## List
**Import Credentials** + **Create Credentials** buttons. Table columns: **Name · Credential Type · Description · Actions** (edit / delete). Example row (172.16.12.224): **cred test** — Credential Type **SSH**.

## Create Credentials Form
Defines Name, **Credential Type** (SSH / SNMP / WMI / …), the type-specific secret fields (username/password/key/community), and description.

## Relationships
- Selected on discovery scans — [Admin: Network Scan](discovery/02-network-scan.md) · [Admin: Domain Scan](discovery/05-domain-scan.md) · [Admin: SCCM Scan](discovery/06-sccm-scan.md) · [Admin: Public Cloud Network](discovery/03-public-cloud-network.md) · [Admin: Private Cloud Network](discovery/04-private-cloud-network.md)
- Distinct from Agent Credential Profile (agent-side) — [Admin: Agent Credential Profile](agent/07-agent-credential-profile.md)
