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

<br/><br/>
VLAN Setup: <br/>
<img src="https://imgur.com/6R3gjeo.png" height="70%" width="70%" alt="VLAN Config"/>

<br/><br/>
DHCP Setup: <br/>
<img src="https://imgur.com/CTxmyfv.png" height="70%" width="70%" alt="VLAN Config"/>
<img src="https://imgur.com/HWJw2XG.png" height="70%" width="70%" alt="VLAN Config"/>

<br/><br/>
ACL & PAT Implementation: <br/>
<img src="https://imgur.com/IbQNogT.png" height="70%" width="70%" alt="ACLs and PAT"/>

<br/><br/>
DHCP Snooping + DAI: <br/>
<img src="https://imgur.com/CQeQ6p7.png" height="70%" width="70%" alt="DHCP Snooping and DAI"/>
<img src="https://imgur.com/zxTAwJe.png" height="70%" width="70%" alt="DHCP Snooping and DAI"/>
<img src="https://imgur.com/iCxlcJJ.png" height="70%" width="70%" alt="DHCP Snooping and DAI"/>


<br/><br/>
Switchport Security: <br/>
<img src="https://imgur.com/2SKykWX.png" height="70%" width="70%" alt="Switchport Security"/>

<br/><br/>
OSPF route on HQ CORE 1: <br/>
<img src="https://imgur.com/zHLPLxL.png" height="70%" width="70%" alt="Switchport Security"/>

<br/><br/>
IP route on HQ CORE 1: <br/>
<img src="https://imgur.com/F9Nu6RR.png" height="70%" width="70%" alt="Switchport Security"/>


</p>

---

## 🔒 Security Implementation Highlights

- Configured **PAT** to allow private IPs to access the internet via a single public IP.
- Applied **ACLs** to filter traffic entering/exiting specific departments.
- Used **DHCP Snooping** and **DAI** to block rogue DHCP servers and ARP spoofing.
- Enabled **Port Security** to limit the number of devices on switchports in the Server VLAN.

---

## 💡 What I Learned

- How to **design secure, segmented networks** using VLANs and multilayer switches.
- Implementing **routing protocols (RIP v2, OSPF)** across complex networks.
- Strengthened my understanding of **Layer 2 and Layer 3 security features** like DHCP Snooping, Port Security, and ACLs.
- Learned how to **simulate and troubleshoot real-world network breaches and implement countermeasures**.

---

## ⚙️ Tools

- **Cisco Packet Tracer**
- **Windows CLI for testing**
- **Subnetting calculator**
- **Notepad++ for config documentation**

---

> 📝 *This repo contains only documentation and screenshots. The actual `.pkt` file and config scripts are intentionally excluded for privacy and academic integrity.*

