# Addressing Plan – Enterprise Secure Hybrid Infrastructure

## Overview
This document defines the IPv4 addressing scheme used across the enterprise
campus and branch sites. The design follows hierarchical summarization,
clear role separation, and supports scalable growth.

The addressing model aligns with:
- Core / Distribution / Access layers
- Identity-aware segmentation
- Future hybrid cloud connectivity

---

## Core & Infrastructure Networks

| Purpose | Subnet | Notes |
|------|------|------|
| Core Routing & P2P Links | 10.0.0.0/8 | Summarized backbone |
| Management VLAN (VLAN 99) | 10.0.0.16/28 | Switch management, SNMP, logging |
| Router Loopbacks | 10.0.0.76/32 | OSPF Router-ID, NTP reference |

---

## Site A – User & Service Networks

| VLAN | Purpose | Subnet | Gateway (HSRP) |
|----|------|------|------|
| VLAN 10 | User Data | 10.1.0.0/24 | 10.1.0.1 |
| VLAN 20 | Voice | 10.2.0.0/24 | 10.2.0.1 |
| VLAN 40 | Wireless | 10.6.0.0/24 | 10.6.0.1 |
| VLAN 99 | Management | 10.0.0.0/28 | 10.0.0.1 |

---

## Site B – User & Service Networks

| VLAN | Purpose | Subnet | Gateway (HSRP) |
|----|------|------|------|
| VLAN 10 | User Data | 10.3.0.0/24 | 10.3.0.1 |
| VLAN 20 | Voice | 10.4.0.0/24 | 10.4.0.1 |
| VLAN 30 | Server | 10.5.0.0/24 | 10.5.0.1 |
| VLAN 99 | Management | 10.0.0.16/28 | 10.0.0.17 |

---

## WAN & Internet Edge

| Interface | Addressing |
|----|----|
| R1 WAN IPv4 | DHCP Assigned |
| R1 WAN IPv6 | 2001:DB8:A::/64 |
| Internal IPv6 | 2001:DB8:A1::/64 |

---

## Design Rationale
- /24 per VLAN simplifies troubleshooting and policy enforcement
- Dedicated management subnets reduce attack surface
- IPv6 dual-stack prepares the network for cloud-native services
- Addressing aligns with Zero Trust segmentation principles
