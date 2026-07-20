---
id: admin-agent-installation
title: "Admin: Agent Installation"
url: /admin/asset-management/agent?tab=agent_installation
area: Admin / Discovery And Agents / Agent
page_type: settings
captured: live (172.16.13.8, PMG ServiceOps)
source_server: 172.16.13.8
---

# Admin — Agent Installation

## Purpose
**Deploy the discovery agent to managed endpoints** — remotely push and install the ServiceOps agent onto target machines so they can be scanned/managed (patch, vulnerability, package).

## Access / Navigation
Admin → **Discovery And Agents → Agent → Agent Installation**. URL: `/admin/asset-management/agent?tab=agent_installation`.

## List
**Create Agent Installation** button. Table columns: **Name · IP Range Type · Created By · Agent Credential Profile · Actions** (view/details icons + kebab). Example rows: **centos** and **bhautik** (IP Range Type = Specific set of IPs, Agent Credential Profile = Default).

## Create Agent Installation Form
Defines Name, **IP Range Type** (Entire Network / Specific IP Range / Specific set of IPs), target IPs, **Agent Credential Profile**, agent build, and poller.

## Relationships
- Uses Agent Credential Profile — [Admin: Agent Credential Profile](07-agent-credential-profile.md)
- Uses Agent Build binaries — [Admin: Agent Build](02-agent-build.md)
- Results tracked in Agent Installation History — [Admin: Agent Installation History](03-agent-installation-history.md)
- Installed agents appear in Agents — [Admin: Agents](04-agents.md)
- Installs onto endpoints — [Endpoint (Patch Computers)](../../../patches/03-patch-endpoints.md)
