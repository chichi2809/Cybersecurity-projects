# Firewall Logs Analysis

**Source:** Palo Alto Networks Firewall  
**Time Range:** March 9-10, 2026  
**Total Entries:** 15,247 (filtered to relevant entries below)

---

## Suspicious Outbound Connections

### Connection to C2 Server
```
2026-03-09 17:25:33 | ALLOW | TCP | 10.10.50.45:49182 -> 185.220.101.55:443 | 245 bytes
2026-03-09 17:26:33 | ALLOW | TCP | 10.10.50.45:49182 -> 185.220.101.55:443 | 189 bytes
2026-03-09 17:27:33 | ALLOW | TCP | 10.10.50.45:49182 -> 185.220.101.55:443 | 201 bytes
[Beacon traffic - 60 second intervals]
```

**Analysis:**
- Regular beaconing pattern (every 60 seconds)
- Small packet sizes indicate C2 communication
- Destination IP has poor reputation (threat intel lookup)

---

### Large Data Transfers
```
2026-03-10 05:32:14 | ALLOW | TCP | 10.10.50.45:49201 -> 185.220.101.55:443 | 1,245,678 bytes
2026-03-10 05:45:22 | ALLOW | TCP | 10.10.50.45:49201 -> 185.220.101.55:443 | 854,321 bytes
2026-03-10 06:15:33 | ALLOW | TCP | 10.10.50.45:49201 -> 185.220.101.55:443 | 2,134,987 bytes
[Pattern continues - total 4.35 GB over 4 hours]
```

**Analysis:**
- Unusually large outbound transfers
- Same destination as C2 server
- Outside normal business hours (5 AM - 9 AM)
- User typically works 9 AM - 5 PM

---

## Threat Intelligence Correlation

**IP Reputation Check: 185.220.101.55**
- VirusTotal: 15/89 vendors flagged as malicious
- AbuseIPDB: Confidence score 98% (malicious)
- Categories: Malware C2, Data Exfiltration
- First seen: 45 days ago
- Associated campaigns: APT-style data theft

---
