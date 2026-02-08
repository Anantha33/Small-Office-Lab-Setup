# Small-Office-Lab-Setup

# Small Office VLAN Network with Inter-VLAN Routing (Router-on-a-Stick)

## Overview
This project simulates a small office network built in Cisco Packet Tracer.  
The goal was to design a segmented VLAN-based LAN and enable communication
between departments using inter-VLAN routing via a router-on-a-stick topology.

---

## Key Objectives
- Create multiple VLANs to separate departmental traffic
- Subnet a /24 network into /26 subnets
- Configure trunking between a switch and router
- Enable inter-VLAN routing using router subinterfaces
- Verify connectivity and troubleshoot common Layer 2/3 issues

---

## Network Topology
- 1× Cisco Router (1941)
- 1× Cisco Switch (2960)
- Multiple PCs across 3 VLANs

---

## VLAN and IP Addressing Plan

| VLAN | Department | Subnet | Default Gateway |
|------|------------|--------|----------------|
| 10   | HR         | 192.168.10.0/26   | 192.168.10.1   |
| 20   | Sales      | 192.168.10.64/26  | 192.168.10.65  |
| 30   | IT         | 192.168.10.128/26 | 192.168.10.129 |

Subnet Mask: `255.255.255.192`

---

## Configuration Summary

### Switch Configuration
- VLAN creation and port assignment
- Trunk configuration on uplink port

### Router Configuration
- Subinterfaces configured with 802.1Q encapsulation
- Default gateways assigned per VLAN

---

## Verification Commands Used
```bash
show vlan brief
show interfaces trunk
show ip interface brief
show ip route
ping <destination>
```
