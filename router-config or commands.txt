# VLAN + Inter-VLAN Routing (Cisco Packet Tracer)

This repository documents the step-by-step process of configuring VLANs and enabling inter-VLAN routing using Cisco Packet Tracer.

---

## ⚙️ Topology
- Cisco 2960 Switch
- Cisco 2911 Router
- 4 PCs (IT, HR, Finance, Operations)

---

## 🔑 Configuration Steps

### 1. Router (Cisco 2911)
```bash
enable
configure terminal
hostname R-1

interface gigabitEthernet 0/0
 no shutdown

interface gigabitEthernet 0/0.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0
 no shutdown

interface gigabitEthernet 0/0.20
 encapsulation dot1Q 20
 ip address 192.168.20.1 255.255.255.0
 no shutdown

interface gigabitEthernet 0/0.30
 encapsulation dot1Q 30
 ip address 192.168.30.1 255.255.255.0
 no shutdown

interface gigabitEthernet 0/0.40
 encapsulation dot1Q 40
 ip address 192.168.40.1 255.255.255.0
 no shutdown

do write
