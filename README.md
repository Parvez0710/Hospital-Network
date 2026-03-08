# Hospital Network Design and Implementation

This project demonstrates the design and implementation of a **secure and scalable hospital network infrastructure**.
The network connects a **Headquarters site, Branch site, and Server-Side Site (SSS)** while providing centralized services such as **DHCP, DNS, Email, FTP, and Web servers**.

The infrastructure follows a **hierarchical network model (Core, Distribution, Access)** to ensure scalability, performance, and efficient network management.

---

# Network Architecture

The network consists of three main segments:

### Headquarters Network

Hosts major hospital departments including:

* IT
* Customer Service
* Medical Records
* Administration

### Branch Network

Represents a remote medical facility connected to the headquarters using routers for secure communication and centralized services.

### Server-Side Site (SSS)

Provides centralized services for both sites including:

* DHCP
* DNS
* Email Server
* Web Server
* FTP Server

---

# Network Design

The network uses a **three-tier architecture**:

* **Core Layer** – Routers responsible for inter-site and external communication
* **Distribution Layer** – Multilayer switches handling routing and traffic control
* **Access Layer** – Department switches connecting end devices

Wireless access points are also deployed to support **department-level wireless connectivity**.

---

# VLAN Segmentation

Departments are separated using VLANs to improve security and traffic management.

Example VLAN allocation:

| Network        | Departments                     | VLAN Range |
| -------------- | ------------------------------- | ---------- |
| HQ Network     | MLOCS, MER, MRM, IT, CS, HQ-GWA | 10–60      |
| Branch Network | NSO, HL, HR, MK, FIN, BR-GWA    | 80–130     |
| Server Network | DHCP, DNS, Email, Web           | 70         |

---

# IP Addressing

Subnetting is used to allocate network ranges for departments.

Example:

| Department | Network            | VLAN |
| ---------- | ------------------ | ---- |
| MLOCS      | 192.168.100.0/26   | 10   |
| MER        | 192.168.100.64/26  | 20   |
| IT         | 192.168.100.192/26 | 40   |
| CS         | 192.168.101.0/26   | 50   |

Branch departments use `/27` networks while server infrastructure uses `/28`.

---

# Technologies Implemented

### Routing

* OSPF (Single Area 10)
* Dynamic routing between routers and multilayer switches

### Network Services

* DHCP for automatic IP allocation
* DNS for internal name resolution
* Email, FTP, and Web servers

### Security

* Access Control Lists (ACL)
* SSH for secure remote access
* Port security

### Network Infrastructure

* VLAN segmentation
* Inter-VLAN routing using Layer-3 switches
* NAT/PAT for internet access

### Wireless Networking

* Department-based wireless access points
* SSID configuration mapped to VLANs

---

# Key Learning Outcomes

* Enterprise network architecture design
* VLAN segmentation and inter-VLAN routing
* Dynamic routing using OSPF
* Network security with ACLs and port security
* NAT/PAT configuration for internet connectivity
* Infrastructure monitoring and service deployment

---

# Tools Used

* Cisco Packet Tracer / GNS3
* Networking protocols and services
* Enterprise network design principles

---

# Author

**Parvez**
Computer Science & Engineering Student

