# 🔹 Basic VLAN Configuration Lab

---

## 📌 Objective

To configure a basic VLAN and assign devices to it, ensuring communication within the same broadcast domain.

---

## 🧠 Concepts Covered

* VLAN Creation
* Access Port Configuration
* Basic Layer 2 Communication

---

## 🖼️ Topology Description:

* 1 Switch
* 2 PCs
* Both PCs are connected to the same VLAN

---

## ⚙️ Configuration

* Create VLAN 10
* Assign both PC ports to VLAN 10

---

## ✅ Verification

✔ PC1 can ping PC2 successfully
✔ Both devices are in the same VLAN

---

## 📊 Expected Results

| Test Case | Result    |
| --------- | --------- |
| PC1 → PC2 | ✅ Success |

---

## 🧩 Key Takeaways

* Devices in the same VLAN can communicate directly
* VLANs define broadcast domains
* Proper port assignment is essential

---

## 🚀 Next Step

Expand this lab to:

* Multiple VLANs (VLAN 10, VLAN 20)
* Add trunk links between switches
