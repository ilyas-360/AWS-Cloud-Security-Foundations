# VLAN & Inter-VLAN Routing Lab (SVI on Multilayer Switch)

Lab based on Jeremy IT Lab #34 (Multilayer switch with SVIs).  
This repository shows VLAN creation, trunk configuration, SVIs (last usable as gateways), and verification.

## Topology
![Topology](./topology.png)

## Addressing plan (subnets are /26)
- VLAN10: 10.0.0.0/26 — SVI gateway (last usable): **10.0.0.62**  
- VLAN20: 10.0.0.64/26 — SVI gateway (last usable): **10.0.0.126**  
- VLAN30: 10.0.0.128/26 — SVI gateway (last usable): **10.0.0.190**  
- SW2 ↔ R1 link: 10.0.0.192/30 — SW2: **10.0.0.193** / R1: **10.0.0.194**

## Files
- `vlan-config.txt` — VLAN creation & access ports (SW1)
- `trunk-config.txt` — trunk configuration (SW2)
- `svi-config.txt` — SVIs + routed uplink (SW2)
- `router-config.txt` — router to SW2 link
- `verification.txt` — commands and screenshot list

## How to apply
1. Apply `vlan-config.txt` on SW1.  
2. Apply `trunk-config.txt` on SW2 (and SW1 trunk already included).  
3. Apply `svi-config.txt` on SW2 (enables `ip routing`).  
4. Apply `router-config.txt` on router R1.  
5. Set PCs IPs according to addressing plan and default gateways to the SVI IPs.  
6. Run verification commands and add screenshots to `screenshots/`.

## Screenshots (stored in `screenshots/`)
- `vlan-show-sw1.png` — `show vlan brief` on SW1  
- `trunk-show-sw1.png` — `show interfaces trunk` on SW1  
- `vlan-show-sw2.png` — `show vlan brief` on SW2  
- `svi-show-sw2.png` — `show ip interface brief` on SW2 (SVIs)  
- `trunk-show-sw2.png` — `show interfaces trunk` on SW2  
- `router-ifbrief.png` — `show ip interface brief` on Router R1  
- `ping-tests.png` — example successful pings between VLANs

