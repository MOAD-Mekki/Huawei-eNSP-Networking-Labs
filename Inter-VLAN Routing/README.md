# 🔀 Inter-VLAN Routing Lab (Router-on-a-Stick)

---

## 📌 Objective

Enable communication between different VLANs using a router by implementing **Inter-VLAN Routing (Router-on-a-Stick)**.

---

## 🧠 Concepts Covered

* VLAN Segmentation
* Trunking (802.1Q)
* Sub-interfaces
* Default Gateway Configuration
* Inter-VLAN Routing

---

## 🖼️ Topology Description:

* 1 Router
* 1 Switch
* 2 VLANs (VLAN 10 and VLAN 20)
* 2 PCs (each in different VLAN)

---

## ⚙️ Configuration Overview

### 🔹 Switch

* Create VLANs (10, 20)
* Assign access ports to VLANs
* Configure trunk link to router

### 🔹 Router

* Create sub-interfaces
* Assign IP addresses for each VLAN
* Enable 802.1Q encapsulation

---

## 🧾 Configuration Files

Located in `configs/`:

* switch.txt
* router.txt

---

## 🌐 IP Addressing Plan

| Device | Interface | IP Address   | VLAN |
| ------ | --------- | ------------ | ---- |
| PC1    | -         | 192.168.10.2 | 10   |
| PC2    | -         | 192.168.20.2 | 20   |
| Router | G0/0/0.10 | 192.168.10.1 | 10   |
| Router | G0/0/0.20 | 192.168.20.1 | 20   |

---

## ✅ Verification

✔ PC1 can ping PC2 (different VLANs)
✔ Router routes traffic between VLANs
✔ Sub-interfaces are operational

---

## 📊 Expected Results

| Test Case                   | Result    |
| --------------------------- | --------- |
| PC1 → PC2 (different VLANs) | ✅ Success |
| PC1 → Gateway               | ✅ Success |
| PC2 → Gateway               | ✅ Success |

---

## 🧩 Key Takeaways

* VLANs isolate traffic at Layer 2
* Routing is required for inter-VLAN communication
* Router-on-a-Stick uses sub-interfaces with 802.1Q tagging

---

## 🚀 Next Step

Implement **dynamic routing (RIP or OSPF)** between multiple routers.
