# 🌐 Static Routing Lab

---

## 📌 Objective

Configure **static routing** between two networks using routers to enable communication across different subnets.

---

## 🧠 Concepts Covered

* Static Routing
* Network Addressing
* Default Gateway
* Inter-network Communication
* Routing Tables

---

## 🖼️ Topology Description

* 2 Routers (Router1, Router2)
* 2 Switches
* 2 LANs:

  * Network 1 → 192.168.1.0/24
  * Network 2 → 192.168.2.0/24
* 1 link between routers

---

## 🌐 IP Addressing Plan

| Device  | Interface | IP Address  |
| ------- | --------- | ----------- |
| PC1     | -         | 192.168.1.2 |
| Router1 | G0/0/0    | 192.168.1.1 |
| Router1 | G0/0/1    | 10.0.0.1    |
| Router2 | G0/0/1    | 10.0.0.2    |
| Router2 | G0/0/0    | 192.168.2.1 |
| PC2     | -         | 192.168.2.2 |

---

## ⚙️ Configuration Overview

### 🔹 Router1

* Configure LAN interface
* Configure WAN link to Router2
* Add static route to Network 2

### 🔹 Router2

* Configure LAN interface
* Configure WAN link to Router1
* Add static route to Network 1

### 🔹 Switches

* Basic access configuration

---

## ✅ Verification

✔ PC1 can ping PC2
✔ Routers can reach each other
✔ Routing tables contain static routes

---

## 📊 Expected Results

| Test Case         | Result    |
| ----------------- | --------- |
| PC1 → PC2         | ✅ Success |
| Router1 → Router2 | ✅ Success |
| Route visibility  | ✅ Present |

---

## 🧩 Key Takeaways

* Static routes define fixed paths between networks
* Routers must know all destination networks
* Bidirectional routing is required for communication

---

## 🚀 Next Step

Move to **dynamic routing (RIP or OSPF)** for automatic route learning.
