# medicare-secure-architecture

<h1>🏥 MediCare Solutions – Secure Enterprise Architecture</h1>

> Simulated secure network infrastructure for a healthcare environment using Cisco Packet Tracer.

---


## 🧠 Project Summary

This project involved designing and securing a complex network for MediCare Solutions, a multi-departmental healthcare provider. The goal was to internalize their network infrastructure and ensure compliance with the **CIA triad** — Confidentiality, Integrity, and Availability.

---

## 🛠 Technologies & Concepts Used

- **Cisco Packet Tracer**
- **OSPF** for routing
- **VLANs & Inter-VLAN Routing**
- **Multilayer Switch Configuration**
- **Access Control Lists (ACLs)**
- **Port Address Translation (PAT)**
- **DHCP Snooping**
- **Dynamic ARP Inspection (DAI)**
- **Switchport Security**

---

## 🧩 Environment Overview

- Simulated hospital network with 6 VLANs (Patient Records Managment (PRM), Medical Operations & Radiology Services (MORS), Emergency Medicine and Reporting (EMR), IT, Client Services (CS) and the Server-side)
- Each department segmented with its own VLAN and IP subnet
- Core routers connected to two separate ISPs with public IPs
- Centralized server room housing DNS, DHCP, Web, and Mail servers

---

## 📸 Network Design Walkthrough

<p align="center">

Network Topology: <br/>
<img src="https://i.imgur.com/bglj4ft.png" height="70%" width="70%" alt="Network Topology"/>

Device name= CLI name  <br/>
HQ-SW= Server switch  <br/>
HQ CORE 1= Internet-1  <br/>
HQ CORE 2= Internet-2  <br/>

<br/><br/>
VLAN Setup: <br/>
<img src="https://imgur.com/6R3gjeo.png" height="70%" width="70%" alt="VLAN Config"/>


Established inter-departmental communication via inter-VLAN routing on Multilayer switch HQ-SW.

<br/><br/>
DHCP Setup: <br/>
<img src="https://imgur.com/CTxmyfv.png" height="70%" width="70%" alt="VLAN Config"/>
<img src="https://imgur.com/HWJw2XG.png" height="70%" width="70%" alt="VLAN Config"/>

 Enabled dynamic IP address assignment for all devices from a dedicated DHCP server, except those in the server room, which uses a static IP allocation. 

<br/><br/>
ACL & PAT Implementation: <br/>
<img src="https://imgur.com/IbQNogT.png" height="70%" width="70%" alt="ACLs and PAT"/>

Implemented PAT to translate private IP addresses to a single public IP for outbound internet access and configure ACLs to control inbound/outbound traffic based on security policies. 

<br/><br/>
DHCP Snooping + DAI: <br/>
<img src="https://imgur.com/CQeQ6p7.png" height="70%" width="70%" alt="DHCP Snooping and DAI"/>
<img src="https://imgur.com/zxTAwJe.png" height="70%" width="70%" alt="DHCP Snooping and DAI"/>
<img src="https://imgur.com/iCxlcJJ.png" height="70%" width="70%" alt="DHCP Snooping and DAI"/>

Enabled DHCP snooping to mitigate rogue DHCP server attacks by monitoring and filtering DHCP messages, allowing only authorized DHCP servers to allocate IP addresses. Implemented Dynamic ARP Inspection to prevent ARP spoofing attacks by validating ARP packets and discarding malicious or unauthorized ARP packets. 


<br/><br/>
Switchport Security on HQ-SW: <br/>
<img src="https://imgur.com/2SKykWX.png" height="70%" width="70%" alt="Switchport Security"/>

Configured switchport security to limit the number of MAC addresses allowed per switchport, preventing unauthorized devices from connecting to the network. 

<br/><br/>
OSPF route on HQ CORE 1: <br/>
<img src="https://imgur.com/zHLPLxL.png" height="70%" width="70%" alt="Switchport Security"/>

Employed OSPF as the routing protocol to advertise routes across routers and multilayer switches. 

<br/><br/>
IP route on HQ CORE 1: <br/>
<img src="https://imgur.com/F9Nu6RR.png" height="70%" width="70%" alt="Switchport Security"/>

Implemented default static routing to facilitate the forwarding of unmatched traffic by routers and multilayer switches, using next-hop IP addresses. 


</p>

---

## 🔒 Security Implementation Highlights

- Configured **PAT** to allow private IPs to access the internet via a single public IP.
- Applied **ACLs** to filter traffic entering/exiting specific departments.
- Used **DHCP Snooping** and **DAI** to block rogue DHCP servers and ARP spoofing.
- Enabled **Port Security** to limit the number of devices on switchports in the Server Switch.

---

## 💡 What I Learned

- How to **design secure, segmented networks** using VLANs and multilayer switches.
- Implementing **routing protocol OSPF** across complex networks.
- Strengthened my understanding of **Layer 2 and Layer 3 security features** like DHCP Snooping, Port Security, and ACLs.


---

## ⚙️ Tools

- **Cisco Packet Tracer**
- **Notepad++ for config documentation**

---

> 📝 *This repo contains only documentation and screenshots. The actual `.pkt` file and config scripts are intentionally excluded for privacy and academic integrity.*

