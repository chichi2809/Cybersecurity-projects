# Incident Scenario: Data Exfiltration at TechVenture Solutions

## Company Background

**TechVenture Solutions**
- **Industry:** Software Development (B2B SaaS)
- **Employees:** 150
- **Revenue:** $25M annually
- **Infrastructure:** Hybrid (on-premise + AWS)
- **Compliance:** SOC 2 Type I (pursuing Type II)

---

## Initial Alert

**SIEM Alert Details**
```
Alert ID: ALT-2026-03-10-0947
Severity: HIGH
Type: Suspicious Outbound Traffic
Time: Monday, March 10, 2026 09:47 AM EST

Source IP: 10.10.50.45 (DESKTOP-DEV-042)
Destination IP: 185.220.101.55 (External - Unknown)
Protocol: HTTPS (Port 443)
Data Volume: 2.5 GB over 4 hours
User: jsmith (Developer - Software Engineering)

Alert Rule: "Large Outbound Data Transfer to Unknown External IP"
Confidence: 95%
```

---

## Investigation Timeline

### Day -1: March 9, 2026 (Attack Preparation)

**16:45** - Phishing email received
```
From: external@malicious.com
To: jsmith@techventure.com
Subject: "Re: Your Resume - Job Opportunity"
Attachment: job_details.docx [Malicious Macro]
```

**17:22** - User opens attachment
- Macro executes
- Downloads payload: malicious_payload.exe
- Hash: 098f6bcd4621d373cade4e832627b4f6

**17:23** - Payload execution
- Establishes persistence (Registry Run Key)
- Creates backdoor connection to C2: 185.220.101.55

**17:25** - C2 communication established
- Beacon interval: Every 60 seconds
- Encrypted communication over HTTPS

---

### Day 0: March 10, 2026 (Data Exfiltration)

**05:15** - Attacker authenticates
- Stolen credentials used (credential dumping)
- Access to file shares and databases

**05:16 - 05:30** - Reconnaissance
- Directory enumeration
- File enumeration
- Database query

**05:30 - 09:30** - Data exfiltration
- Total exfiltrated: 4.35 GB
- Duration: 4 hours
- Files accessed: 237

**09:47** - SIEM alert triggered
- Alert generated based on volume threshold
- Assigned to SOC analyst (you!)

**10:15** - Initial response
- Workstation isolated from network
- User account disabled
- Investigation begins

---

## Data Compromised

### Files Exfiltrated

**1. Customer Database**
- File: Customer_Database.xlsx
- Size: 2.1 MB
- Records: 15,000 customers
- Data: Names, emails, phone, purchase history
- Classification: SENSITIVE (PII)

**2. Proprietary Source Code**
- File: proprietary_algo.py
- Size: 450 KB
- Description: Core recommendation algorithm
- Classification: CONFIDENTIAL (IP)

**3. Client Contracts**
- Folder: client_contracts/
- Size: 1.8 MB
- Files: 23 PDF contracts
- Classification: CONFIDENTIAL

**4. Additional Files**
- Various internal documents
- Total: 4.35 GB

---

## Indicators of Compromise (IOCs)

### File Hashes (SHA256)
```
job_details.docx: 5d41402abc4b2a76b9719d911017c592
malicious_payload.exe: 098f6bcd4621d373cade4e832627b4f6
compress_and_upload.ps1: 7c211433f02071597741e6ff5a8ea34f
```

### IP Addresses
```
C2 Server: 185.220.101.55
Exfiltration Server: 192.168.100.23 (internal pivot)
```

### Domains
```
file-share.onion
malicious-cdn.com
```

### Registry Keys
```
HKCU\Software\Microsoft\Windows\CurrentVersion\Run\SystemUpdate
Value: C:\Users\jsmith\AppData\Local\Temp\malicious_payload.exe
```

### Suspicious Processes
```
svchost.exe (PID 4582) - Unusual parent process
powershell.exe -encodedCommand [Base64]
```

---
