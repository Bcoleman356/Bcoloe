# 🔵 Defensive Security Intro — TryHackMe

![TryHackMe](https://img.shields.io/badge/TryHackMe-212C42?style=for-the-badge&logo=tryhackme&logoColor=white)
![Defensive Security](https://img.shields.io/badge/Defensive_Security-0078D4?style=for-the-badge)
![SOC](https://img.shields.io/badge/SOC-Operations-0078D4?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

---

## 📋 Overview

This room introduced the core disciplines of defensive security — the practices, tools, and frameworks that security teams use to protect organizations from cyber threats. Covering Threat Intelligence, Security Operations Centers (SOC), Digital Forensics and Incident Response (DFIR), Malware Analysis, and SIEM — this room maps directly to the daily work of SOC Analysts, Information Security Analysts, and Cybersecurity Operations professionals.

While offensive security thinks like an attacker, defensive security thinks like a guardian. Both perspectives together form a complete cybersecurity skillset.

---

## 🎯 What I Learned

- How Security Operations Centers (SOC) are structured and how analysts monitor, detect, and respond to threats
- The role of Threat Intelligence in proactively identifying and preparing for emerging attack vectors
- The Digital Forensics and Incident Response (DFIR) process — how security teams investigate breaches and recover from attacks
- How Malware Analysis works — static vs dynamic analysis, behavioral indicators, and sandboxing techniques
- How SIEM platforms (like Splunk) aggregate and correlate logs to surface security events and alerts
- The relationship between all defensive security disciplines in a mature security operations environment

---

## 🔑 Key Concepts Covered

| Concept | Description |
|---|---|
| **SOC (Security Operations Center)** | Team of analysts who monitor, detect, investigate, and respond to cybersecurity threats 24/7 |
| **Threat Intelligence** | Collecting and analyzing data about current and emerging threats to proactively defend against them |
| **DFIR** | Digital Forensics & Incident Response — investigating security incidents, preserving evidence, and restoring operations |
| **Digital Forensics** | Collecting and analyzing digital evidence from compromised systems to understand what happened |
| **Incident Response** | Structured process for containing, eradicating, and recovering from a security incident |
| **Malware Analysis** | Examining malicious software to understand its behavior, origin, and impact |
| **Static Analysis** | Analyzing malware without executing it — examining code, strings, and file structure |
| **Dynamic Analysis** | Running malware in a controlled sandbox environment to observe its behavior |
| **SIEM** | Security Information and Event Management — aggregates logs from across an environment to detect threats |
| **IoC (Indicator of Compromise)** | Evidence that a system has been breached — suspicious IPs, file hashes, registry changes |
| **Threat Hunting** | Proactively searching for threats that evade automated detection |

---

## 🏗️ SOC Operations Flow

```
Log Sources (Firewall, AD, Endpoints, Cloud)
              │
              ▼
        SIEM Platform
     (Splunk / Sentinel)
              │
         Correlation
          & Alerting
              │
              ▼
    ┌─────────────────────┐
    │    SOC Analyst       │
    │  Tier 1 — Triage    │
    └──────────┬──────────┘
               │ Escalate
               ▼
    ┌─────────────────────┐
    │  Tier 2 — Investigate│
    │  DFIR / Malware      │
    └──────────┬──────────┘
               │ Major Incident
               ▼
    ┌─────────────────────┐
    │  Tier 3 — Response  │
    │  Contain / Eradicate │
    └─────────────────────┘
```

---

## 🔐 How This Connects to Your Experience

| What You Do at AAFES | Defensive Security Equivalent |
|---|---|
| ServiceNow ticket triage & escalation | SOC Tier 1 alert triage & escalation |
| Identifying and routing issues to correct teams | Incident classification and handoff |
| Access management & role approvals | Identity-based threat detection |
| Generating performance reports for leadership | SOC metrics and security posture reporting |
| Process documentation & compliance | Security policy documentation & audit support |

You have been performing defensive security functions daily without the title. This room formalizes that knowledge.

---

## 🛠️ Tools & Platforms Referenced

| Tool | Purpose |
|---|---|
| **Splunk** | SIEM — log aggregation, correlation, and alerting *(actively learning)* |
| **Wireshark** | Network traffic analysis and packet capture |
| **Autopsy** | Digital forensics — disk image analysis |
| **MITRE ATT&CK** | Framework mapping attacker tactics and techniques |
| **VirusTotal** | Online malware scanning and IoC lookup |

---

## 🎓 Certifications This Supports

| Certification | Relevant Concepts |
|---|---|
| **CompTIA Security+** *(In Progress)* | Security Operations domain (28% of exam) — SOC, SIEM, incident response, threat intelligence |
| **Microsoft AZ-104** *(In Progress)* | Azure Monitor, Log Analytics, cloud security monitoring |

---

## 🗂️ TryHackMe Learning Path Progress

| Room | Status | Category |
|---|---|---|
| Offensive Security Intro | ✅ Completed | Offensive Security |
| **Defensive Security Intro** | ✅ Completed | Defensive Security |
| SOC Level 1 Path | 🔄 In Progress | SOC Operations |
| Splunk Rooms | 🔄 In Progress | SIEM / Log Analysis |
| Security+ Prep Path | 🔄 In Progress | Certification Prep |

---

## 👤 Author

**Brandon Coleman**
IT Systems Analyst | Cybersecurity · Azure Cloud · Data Analytics

[![TryHackMe](https://img.shields.io/badge/TryHackMe-212C42?style=flat&logo=tryhackme&logoColor=white)](https://tryhackme.com/p/YourUsername)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/Bcoleman356)

📍 Mansfield, TX
