# Enterprise Security Incident Investigation

**Data Exfiltration Investigation & Response**

![Project Status](https://img.shields.io/badge/Status-In_Progress-yellow)
![Framework](https://img.shields.io/badge/Framework-MITRE_ATT%26CK-red)
![Skills](https://img.shields.io/badge/Skills-SOC_Analysis-blue)

---

## 📋 Project Overview

This project demonstrates SOC investigation skills through analysis of a data exfiltration incident at TechVenture Solutions, a 150-employee software development company.

**Incident Type:** Data Exfiltration  
**Data Compromised:** 4.35GB (customer PII, proprietary source code)  
**Attack Vector:** Spearphishing → Backdoor → Credential Theft → Exfiltration  
**Timeline:** 72-hour investigation window

---

## 🎯 Skills Demonstrated

**SOC Skills:**
- Log analysis (firewall, SIEM, endpoint, proxy)
- IOC identification and tracking
- Attack timeline reconstruction
- Incident response procedures
- Digital forensics

**GRC Skills:**
- NIST CSF alignment (Detect, Respond, Recover)
- Policy gap analysis
- Compliance impact assessment
- Risk quantification

**Frameworks:**
- MITRE ATT&CK
- NIST Cybersecurity Framework
- Incident Response Lifecycle

---

## 🏢 Incident Summary

**Company:** TechVenture Solutions
- 150 employees
- Software development
- Hybrid cloud/on-premise
- Subject to SOC 2

**Incident Timeline:**
- **March 9, 16:45** - Phishing email received
- **March 9, 17:22** - Malicious attachment opened
- **March 10, 05:15-09:30** - Data exfiltration (4.35GB)
- **March 10, 09:47** - SIEM alert triggered
- **March 10, 10:15** - System isolated

**Impact:** $150K-$500K estimated business impact

---

## 📂 Repository Structure
```
├── 01-Incident-Overview/        # Incident summary and timeline
├── 02-Log-Analysis/             # Parsed logs and analysis
├── 03-Investigation-Report/     # Detailed findings
├── 04-MITRE-ATTACK-Mapping/     # Attack technique mapping
├── 05-GRC-Assessment/           # Policy and compliance gaps
└── 06-Executive-Briefing/       # Business impact summary
```

---

## 🔍 Investigation Phases

### Phase 1: Initial Triage
- Alert validation and scoping
- System isolation
- Evidence preservation

### Phase 2: Deep Investigation
- Log analysis and correlation
- IOC identification
- Timeline reconstruction
- Attack vector analysis

### Phase 3: Impact Assessment
- Data loss quantification
- Business impact analysis
- Compliance implications

### Phase 4: GRC Alignment
- NIST CSF gap analysis
- Policy recommendations
- Control improvement roadmap

---

**⭐ If you found this project helpful, please star this repository!**
