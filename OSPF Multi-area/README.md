# 🌐 OSPF Multi-Area Routing Lab

---

## 📌 Objective

Implement **multi-area OSPF (Open Shortest Path First)** routing to enable scalable and efficient communication between multiple networks.

---

## 🧠 Concepts Covered

* OSPF Dynamic Routing
* Multi-Area OSPF
* Backbone Area (Area 0)
* LSAs (Link-State Advertisements)

---

## 🖼️ Topology Description

Contains:

* 3 Routers:

  * AR1
  * AR2
  * AR3

* 3 LANs:

  * LAN 1 → Area 1
  * LAN 2 → Area 0 (Backbone)
  * LAN 3 → Area 2

* Router Roles:

  * AR1 → Area 1 Router
  * AR2 → Area Border Router (ABR)
  * AR3 → Area 2 Router

---

## 🌐 IP Addressing Plan

| Device | Interface | IP Address     | Area   |
| ------ | --------- | -------------- | ------ |
| PC1    | -         | 192.168.1.2/24 | Area 1 |
| AR1    | G0/0/0    | 192.168.1.1/24 | Area 1 |
| AR1    | G0/0/1    | 10.0.12.1/24   | Area 0 |
| PC2    | -         | 192.168.2.2/24 | Area 0 |
| AR2    | G0/0/0    | 192.168.2.1/24 | Area 0 |
| AR2    | G0/0/1    | 10.0.12.2/24   | Area 0 |
| AR2    | G0/0/2    | 10.0.23.1/24   | Area 0 |
| PC3    | -         | 192.168.3.2/24 | Area 2 |
| AR3    | G0/0/0    | 192.168.3.1/24 | Area 2 |
| AR3    | G0/0/1    | 10.0.23.2/24   | Area 0 |

---

## ⚙️ Configuration Overview

### 🔹 AR1

* Configure OSPF Area 1
* Advertise LAN 1 network
* Connect to backbone through AR2

### 🔹 AR2

* Configure Backbone Area 0
* Act as Area Border Router (ABR)
* Exchange routes between areas

### 🔹 AR3

* Configure OSPF Area 2
* Advertise LAN 3 network
* Connect to backbone through AR2

---

## ✅ Verification

✔ PC1 can ping PC2
✔ PC1 can ping PC3
✔ OSPF neighbors are established
✔ OSPF routes appear in routing tables

---

## 🧩 Key Takeaways

* Area 0 is the OSPF backbone
* ABRs connect multiple OSPF areas
* OSPF dynamically calculates shortest paths
