# Enterprise Multi-Site Network Design using Cisco Packet Tracer

## Overview

This project demonstrates the design and implementation of a secure enterprise network using Cisco Packet Tracer. The network consists of one Headquarters (HQ) and two branch offices (Batangas and Cebu) connected through WAN serial links. The network provides centralized services while implementing department-based security policies using Access Control Lists (ACLs).

---

## Network Topology

- Headquarters (HQ)
- Batangas Branch
- Cebu Branch

Departments:
- Information Technology (IT)
- Human Resources (HR)
- Finance
- Sales

Centralized Services:
- FTP Server
- DNS Server
- HTTP Server

---

## Objectives

- Design a multi-site enterprise network.
- Implement VLAN segmentation.
- Configure Router-on-a-Stick.
- Configure DHCP for every VLAN.
- Configure NAT/PAT for Internet access.
- Implement static routing between HQ and branches.
- Secure the network using ACLs.
- Centralize enterprise services.
- Allow controlled communication between branches and HQ.

---

## Technologies Used

- Cisco Packet Tracer
- Cisco IOS
- VLAN
- IEEE 802.1Q
- Static Routing
- DHCP
- NAT/PAT
- Extended ACL
- FTP
- DNS
- HTTP
- WAN Serial Connections

---

## Network Structure

### Headquarters

| VLAN | Department | Network |
|------|------------|---------------|
|10|IT|192.168.10.0/24|
|20|HR|192.168.20.0/24|
|30|Finance|192.168.30.0/24|
|40|Sales|192.168.40.0/24|
|100|Server Farm|192.168.100.0/24|

### Batangas Branch

| VLAN | Department | Network |
|------|------------|---------------|
|110|IT|192.168.110.0/24|
|120|HR|192.168.120.0/24|
|130|Finance|192.168.130.0/24|
|140|Sales|192.168.140.0/24|

### Cebu Branch

| VLAN | Department | Network |
|------|------------|---------------|
|210|IT|192.168.210.0/24|
|220|HR|192.168.220.0/24|
|230|Finance|192.168.230.0/24|
|240|Sales|192.168.240.0/24|

---

## Features

✅ VLAN Segmentation

✅ Router-on-a-Stick

✅ DHCP Configuration

✅ Static Routing

✅ NAT/PAT

✅ WAN Connectivity

✅ FTP Server

✅ DNS Server

✅ HTTP Server

✅ Department Isolation using ACLs

✅ Branch-to-HQ Communication

---

## Security Policies

### Headquarters

- IT can communicate with all departments.
- HR cannot access Finance or Sales.
- Finance cannot access HR or Sales.
- Sales cannot access HR or Finance.

### Branch Offices

- Same department isolation policy as HQ.
- Branch users can access centralized servers.
- Branch Heads can communicate with corresponding HQ Heads.
- Branch offices communicate with HQ through WAN.

---

## Testing Performed

- VLAN connectivity
- Inter-VLAN Routing
- DHCP Address Assignment
- NAT Internet Access
- FTP Login
- DNS Resolution
- HTTP Access
- ACL Verification
- HQ ↔ Batangas Communication
- HQ ↔ Cebu Communication

---

## Skills Demonstrated

- Enterprise Network Design
- Cisco IOS Configuration
- Routing
- Switching
- VLAN Design
- ACL Security
- DHCP
- NAT
- WAN Configuration
- Troubleshooting

---

## Lessons Learned

This project improved my understanding of enterprise network architecture, VLAN segmentation, router-on-a-stick implementation, WAN connectivity, ACL-based security, centralized services, and troubleshooting Cisco networks.

---

## Author

John Mark Gualter

Computer Engineering Student

Cisco Packet Tracer Portfolio Project