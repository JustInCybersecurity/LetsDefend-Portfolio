
# 🛡️ SOC Fundamentals

This section documents key concepts, workflows, and tools that form the foundation of a Security Operations Center (SOC).  
It’s a mix of reference notes and lessons learned during hands-on labs (LetsDefend.io, TryHackMe, Azure Sentinel, etc.).

---

## 📍 What is a SOC?
A **Security Operations Center (SOC)** is a centralized function where people, processes, and technology work together to:
- Monitor enterprise networks and systems
- Detect, analyze, and respond to cybersecurity incidents
- Improve overall security posture via continuous threat hunting and remediation

---

## 🔄 SOC Workflow (NIST 800-61 Inspired)
1. **Preparation** → Configure SIEM, detection rules, baselines, playbooks.  
2. **Detection & Analysis** → Monitor SIEM alerts, triage false positives, analyze IOCs.  
3. **Containment, Eradication, Recovery** → Quarantine assets, remove malware, restore services.  
4. **Post-Incident Activity** → Lessons learned, update detection rules, report metrics.

---

## 🧰 Common SOC Tools
- **SIEM**: Splunk, Microsoft Sentinel, ELK, QRadar  
- **EDR**: CrowdStrike, SentinelOne, Microsoft Defender ATP  
- **Threat Intelligence**: VirusTotal, AbuseIPDB, AlienVault OTX  
- **Packet Analysis**: Wireshark, Zeek, Suricata  
- **Automation**: SOAR platforms (Cortex XSOAR, Shuffle, Phantom)  

---

## 🚨 Key SOC Analyst Skills
- Log analysis (Windows Event Logs, Sysmon, Linux syslog)  
- Packet capture review (Wireshark basics: filters, TCP streams, DNS lookups)  
- Understanding of **MITRE ATT&CK tactics and techniques**  
- Incident escalation and documentation in ticketing systems (Jira, ServiceNow, Autotask)  
- Basic scripting for automation (Python, PowerShell, Bash)  

---

## 📝 Example Investigation Workflow (Email Alert)
1. Alert in SIEM: Suspicious login from foreign IP  
2. Gather Evidence: Log into Sentinel → review user’s activity  
3. Correlate IOCs: Run IP through VirusTotal / AbuseIPDB  
4. Containment: Disable account in IAM, block IP on firewall  
5. Escalate if persistent or part of campaign  

---

## 📚 Resources
- [NIST SP 800-61 Rev.2: Computer Security Incident Handling Guide](https://csrc.nist.gov/publications/detail/sp/800-61/rev-2/final)  
- [MITRE ATT&CK Framework](https://attack.mitre.org/)  
- [SANS SOC Primer](https://www.sans.org/posters/soc/)  

---

⭐ *This document evolves as I continue SOC training, labs, and real-world experience.*
