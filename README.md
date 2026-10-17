# Internal Network Reconnaissance & Enumeration Assessment
**Target Environment:** Simulated Healthcare Staging Infrastructure (Metasploitable 2)  
**Author:** Junior Penetration Tester, Flatiron Cyber Defense  

---

## 📋 Project Overview
As part of pre-audit preparations for a healthcare provider client, this engagement focused on identifying network misconfigurations, exposed services, and potential vulnerabilities across an isolated staging environment. Using Kali Linux, the assessment combined active network reconnaissance, rigorous port scanning, manual service enumeration (specifically targeting SMB), and strategic risk analysis to map out the target's attack surface prior to the exploitation phase.

---

## 🛠️ Tools & Technologies Used
* **Operating Systems:** Kali Linux (Attacker VM), Metasploitable 2 (Target VM)
* **Reconnaissance & Scanning:** Nmap (Host discovery, TCP/UDP port scanning, service version detection, and script scanning)
* **Service Enumeration:** `enum4linux`, `smbclient`, `rpcclient`
* **Documentation & Reporting:** Structured Pentest Reporting Framework

---

## 🚀 Key Assessment Tasks & Methodology

### Task 1: Environment Setup & Strategy
* Configured an isolated, host-only virtual networking environment between Kali Linux and Metasploitable 2 to ensure safe, controlled testing.
* Designed a balanced scanning strategy, weighing **stealth/evasion** against **tactical speed and thoroughness** within a permitted internal audit scope.

### Task 2: Host Discovery & Network Reconnaissance
* Executed initial host discovery scans to confirm live systems on the subnet.
* Performed comprehensive TCP port scans using Nmap to identify open ports, running service versions, and operating system fingerprints.

### Task 3: Service Enumeration (Deep Dive on SMB)
* Investigated high-risk and legacy protocols discovered during port scanning.
* Utilized `enum4linux` and SMB-specific utilities to query shares, map user accounts, and identify weak access controls on the target's Server Message Block (SMB) implementation.

### Task 4: Vulnerability & Attack Surface Analysis
* Mapped identified service versions (e.g., vsftpd 2.3.4, Samba 3.0.20, Apache/Tomcat legacy versions) to known CVEs and exploit vectors.
* Categorized findings by risk level to prioritize remediation and lay the groundwork for upcoming exploitation phases.

---

## 📁 Repository Structure
```text
├── reports/
│   └── Penetration_Testing_Report.pdf  # Final professional assessment report
├── scans/
│   ├── nmap_initial_discovery.txt      # Raw Nmap scan outputs
│   └── enum4linux_results.txt          # SMB enumeration logs
└── README.md
