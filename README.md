# Wazuh SOC Lab – End-to-End Security Operations Center Simulation

A complete **Security Operations Center (SOC)** laboratory built using **Wazuh SIEM** to simulate real-world security monitoring, log analysis, threat detection, incident investigation, and threat hunting.

This project demonstrates the responsibilities of a **Tier 1 SOC Analyst**, including collecting endpoint logs, monitoring security events, investigating alerts, correlating incidents, and documenting findings.

---

# Project Overview

Organizations continuously generate thousands of security events every day. Security Operations Centers (SOCs) rely on Security Information and Event Management (SIEM) platforms to centralize logs, detect suspicious activity, and investigate incidents.

This project implements a small SOC environment using Wazuh where a monitored Linux endpoint generates security events that are collected, analyzed, and investigated through the Wazuh Dashboard.

The lab demonstrates several common SOC workflows including:

- Centralized Log Collection
- Security Monitoring
- Alert Generation
- Authentication Monitoring
- Threat Detection
- Threat Hunting
- Incident Investigation
- Security Reporting

---

# Objectives

- Deploy a functioning Wazuh SOC environment
- Configure endpoint monitoring
- Collect Linux authentication and system logs
- Detect suspicious activities
- Investigate security alerts
- Perform threat hunting
- Analyze Linux security events
- Document findings through incident reports

---

# Lab Environment

| Component | Technology |
|-----------|------------|
| Host Machine | macOS |
| Hypervisor | VMware Fusion |
| SIEM Platform | Wazuh |
| Wazuh Manager | Ubuntu Server |
| Dashboard | Wazuh Dashboard |
| Endpoint | Kali Linux |
| Endpoint Agent | Wazuh Agent |

---

# Architecture

```
                     macOS Host
                  VMware Fusion
                         │
        ┌────────────────┴────────────────┐
        │                                 │
        ▼                                 ▼
+----------------------+       +----------------------+
| Ubuntu Server        |       | Kali Linux           |
|----------------------|       |----------------------|
| Wazuh Manager        |<----->| Wazuh Agent          |
| Wazuh Dashboard      | Logs  | Security Events      |
| Wazuh Indexer        |       | Attack Simulation    |
+----------------------+       +----------------------+
```

---

# SOC Workflow

```
  User Activity

        │
        ▼

Endpoint Logs Generated

        │
        ▼

  Wazuh Agent

        │
        ▼

  Wazuh Manager

        │
        ▼

     Indexer

        │
        ▼

    Dashboard

        │
        ▼

Alert Investigation

        │
        ▼

 Threat Hunting

        │
        ▼

 Incident Report
```

---

# Technologies Used

- Wazuh SIEM
- Ubuntu Server
- Kali Linux
- VMware Fusion
- Linux
- SSH
- Hydra
- AppArmor
- OpenSearch Dashboard
- Linux PAM
- Syslog
- MITRE ATT&CK Framework

---

# Security Scenarios Performed

| Scenario | Description | Status |
|----------|-------------|--------|
| Agent Registration | Connected Kali endpoint to Wazuh Manager | ✅ |
| Log Collection | Monitored Linux authentication and system logs | ✅ |
| SSH Monitoring | Generated SSH login events | ✅ |
| Brute Force Simulation | Simulated repeated SSH login attempts using Hydra | ✅ |
| Privilege Escalation | Generated sudo activity | ✅ |
| PAM Monitoring | Monitored login sessions | ✅ |
| AppArmor Investigation | Investigated AppArmor DENIED alerts | ✅ |
| Threat Hunting | Investigated security events using Wazuh queries | ✅ |
| Incident Investigation | Correlated collected events | ✅ |

---

# Security Events Observed

- SSH Authentication
- PAM Login Sessions
- Successful sudo to ROOT
- Authentication Logs
- Linux System Logs
- AppArmor DENIED Events
- Security Event Correlation
- Linux Audit Events

---

# Threat Hunting

Threat hunting activities performed during this lab included:

- Authentication event analysis
- Login session monitoring
- Privilege escalation investigation
- AppArmor alert investigation
- Event timeline analysis
- Endpoint activity review
- Rule severity analysis
- Alert correlation

---

# Project Structure

```
wazuh-soc-lab/

│
├── README.md
├── LICENSE
│
├── architecture/
│   ├── architecture.png
│   └── network-diagram.drawio
│
├── screenshots/
│
├── configs/
│
├── scenarios/
│
├── reports/
│
└── docs/
```

---

# MITRE ATT&CK Mapping

| Technique | Description |
|------------|-------------|
| T1078 | Valid Accounts |
| T1548 | Abuse Elevation Control Mechanism |
| T1059 | Command and Scripting Interpreter |
| T1021 | Remote Services |
| T1110 | Brute Force |

---

# Skills Demonstrated

- SIEM Administration
- Security Monitoring
- Threat Detection
- Threat Hunting
- Incident Response
- Log Analysis
- Linux Security
- Authentication Monitoring
- Privilege Escalation Investigation
- Security Event Correlation
- Wazuh Administration
- MITRE ATT&CK Mapping

---

# Incident Investigation Summary

During the lab, multiple security events were intentionally generated and investigated to simulate a SOC environment.

The investigation included:

- Authentication monitoring
- Login session tracking
- Privilege escalation analysis
- AppArmor policy violations
- Event correlation
- Threat hunting

All alerts were analyzed through the Wazuh Dashboard to understand the sequence of events and validate the effectiveness of endpoint monitoring.

---

# Key Learning Outcomes

- Built an end-to-end SOC environment using Wazuh.
- Configured and monitored Linux endpoints.
- Generated and analyzed authentication events.
- Investigated Linux security alerts.
- Performed threat hunting using SIEM dashboards.
- Documented security findings in a structured manner.
- Gained practical experience with SOC workflows and security monitoring.

---

# Future Improvements

- Malware Detection using EICAR
- File Integrity Monitoring (FIM)
- VirusTotal Integration
- YARA Rule Integration
- Active Response Automation
- Email Alerting
- Windows Endpoint Monitoring
- Sysmon Integration
- Sigma Rule Detection

---

# Author

**Aisha**

Aspiring SOC Analyst | Security Analyst | Cybersecurity Enthusiast

GitHub: https://github.com/aishabanuu
