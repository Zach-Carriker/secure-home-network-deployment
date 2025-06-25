# 🔐 Secure Home Network Deployment

## 🔍 TL;DR (Key Takeaways)

- Conducted real-world vulnerability scans on my personal home network using **Nessus Essentials**
- Identified and remediated critical SSL/TLS issues, SMB signing weaknesses, and router misconfigurations
- Replaced ISP-provided gateway with a hardened **TP-Link AX55**, deployed custom Wi-Fi security settings
- Applied **host-level security hardening** on a Windows laptop using registry edits and Policy Plus
- Isolated IoT devices like a Smart TV based on post-remediation scan findings
- Documented before-and-after results with screenshots and a full technical report

> This project demonstrates practical experience in network hardening, endpoint security, vulnerability assessment, and real-world remediation — not just theory.

---

This project documents the deployment and hardening of a secure home network using **Nessus Essentials** for vulnerability assessment. It includes replacing an ISP-provided router with a TP-Link Archer AX55, scanning multiple devices, and implementing layered security enhancements across the network.

---

## 📄 Project Overview

To enhance the security posture of a residential network, I followed a structured methodology aligned with the **NIST Cybersecurity Framework**. Key actions included:

- Performing a baseline vulnerability scan
- Replacing the ISP modem/router with a TP-Link Archer AX55
- Hardening host-level security on Windows and IoT devices
- Conducting a post-remediation scan to validate fixes

---

## 🧪 Devices Scanned

- **Arris DG9450** – Original ISP-provided gateway (baseline scan only)
- **TP-Link Archer AX55** – Replaced router, hardened and scanned
- **Visio Smart TV (65" V Series)** – Isolated due to cryptographic issues
- **Acer Aspire 5 Laptop** – Windows 11 Home, registry-level SMB fixes
- **HP Chromebook** – Scanned for visibility and surface reduction

---

## 🔍 Key Findings & Remediation

| Component        | Summary                                                                                  |
|------------------|-------------------------------------------------------------------------------------------|
| **Router**        | High-risk SSL/TLS flaws in ISP device resolved by replacing with hardened TP-Link AX55  |
| **Laptop**        | Medium-risk SMB signing issue remediated via registry edits and RDC policy lockdown     |
| **Smart TV**      | SWEET32 cipher suite flagged; segmented into IoT VLAN to mitigate potential exposure    |
| **All Devices**   | ICMP timestamp disclosures noted but deprioritized due to LAN-only scope and low risk   |

---

## 📂 Documentation

- [`Secure_Home_Network_Deployment_Project.pdf`](./Secure_Home_Network_Deployment_Project.pdf)  
  *Detailed walkthrough of scan configuration, discovery, and remediation strategy.*

- [`Secure_Home_Network_Deployment_Report.pdf`](./Secure_Home_Network_Deployment_Report.pdf)  
  *Hardening checklist, router configuration notes, and summary of implemented controls.*

---

## ✅ Final Status

- High and medium vulnerabilities addressed
- LAN interfaces secured and router HTTPS access enforced
- IoT devices isolated from sensitive systems
- Post-remediation scans confirmed risk reduction

---

## 📌 Notes

> *This report is the result of a real vulnerability scan and remediation effort performed on my personal home network, intended for cybersecurity portfolio use.*

---

## 🔗 Related Topics

- Network segmentation
- SMB signing enforcement
- SSL/TLS certificate validation
- Nessus Essentials configuration
- Policy Plus for Windows Home
