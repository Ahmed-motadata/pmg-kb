---
id: admin-snmp-custom-properties
title: "Admin: SNMP Custom Properties"
url: /admin/asset-management/snmp-custom-properties
area: Admin / Discovery And Agents
page_type: list
captured: live (172.16.13.8, PMG ServiceOps)
source_server: 172.16.13.8
---

# Admin — SNMP Custom Properties

## Purpose
**Configure SNMP properties to capture device data** — the database mapping SNMP **System OIDs** to device types (Switch, Router, Wireless Controller, etc.) so SNMP-discovered network devices are classified and their custom properties captured.

## Access / Navigation
Admin → **Discovery And Agents → SNMP Custom Properties**. URL: `/admin/asset-management/snmp-custom-properties`.

## List
Search + **Import Snmp property** + **Import Snmp device** + **Add Snmp device** buttons. Table columns: **Name · Asset Type · System OID · Actions** (Add Snmp property, edit).

Captured (172.16.13.8): a large **out-of-box database of ~24,433 entries** (978 pages) — vendor device definitions like "Switch- (OOB)", "Router- (OOB)", "Wireless Controller- (OOB)" each keyed to an SNMP System OID (e.g. `.1.3.6.1.4.1.25506.11.2.29`), mapped to Asset Types Switch / Router / SNMP Devices.

## Relationships
- Classifies SNMP devices found by network discovery — [Admin: Network Scan](discovery/02-network-scan.md) · [Admin: Discovery Service](discovery/01-discovery-service.md)
- Complements Discovery Pattern (protocol classification) — [Admin: Discovery Pattern](14-discovery-pattern.md)
