# 🔐 Firewall Configuration & Testing

## 📌 Objective
Configure and test basic firewall rules to allow or block traffic on a local system.

## 🛠 Tools Used
- **Windows Firewall** (GUI-based configuration tool)  
- **UFW (Uncomplicated Firewall)** on Linux (command-line tool)

## 📂 Deliverables
- Screenshot or configuration file showing firewall rules applied
- Documentation of commands or GUI steps used
- Summary of how firewall filters traffic

---

## 🚀 Steps Followed

### 1. Open Firewall Configuration Tool
- **Windows:** Open *Windows Defender Firewall with Advanced Security*  
- **Linux (Kali/Ubuntu):** Use terminal with `ufw` commands

### 2. List Current Firewall Rules
sudo ufw status verbose

### 3. Block Inbound Traffic on Port 23 (Telnet)
sudo ufw deny 23/tcp

### 4. Test the Rule
- Attempt to connect to port 23 locally or remotely using `telnet localhost 23`  
- Connection should be blocked

### 5. Allow SSH (Port 22) on Linux
sudo ufw allow 22/tcp

### 6. Remove Test Block Rule
sudo ufw delete deny 23/tcp

### 7. Document Commands / GUI Steps
- Commands listed above for Linux  
- On Windows, rules added via GUI: *Inbound Rules → New Rule → Port → Block 23 → Save*

---

## 📊 Example Firewall Rules (Linux UFW)

Status: active

To                         Action      From
--                         ------      ----
22/tcp                     ALLOW       Anywhere
23/tcp                     DENY        Anywhere
22/tcp (v6)                ALLOW       Anywhere (v6)
23/tcp (v6)                DENY        Anywhere (v6)

---

## ✅ Summary: How Firewalls Filter Traffic
- Firewalls act as a **gatekeeper** between your system and the network.  
- Rules are applied based on **IP, port, and protocol**.  
- **Allow rules** permit traffic through specified ports/services.  
- **Deny rules** block unwanted or insecure traffic.  
- This helps prevent unauthorized access and reduces attack surface.

---

## 📜 License
This project is licensed under the MIT License – feel free to use and adapt.

---
