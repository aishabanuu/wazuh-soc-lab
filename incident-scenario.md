# Incident Scenario

## Overview

This scenario simulates the daily workflow of a Security Operations Center (SOC) analyst using Wazuh SIEM. The objective was to monitor a Linux endpoint, generate security events, investigate alerts, perform threat hunting, and document the findings.

---

## Phase 1 – Wazuh Deployment

### Objective

Deploy the Wazuh platform and configure the lab environment.

### Activities

- Installed Wazuh Manager on Ubuntu Server.
- Configured the Wazuh Dashboard and Indexer.
- Verified all Wazuh services were running successfully.

**Outcome:**  
The Wazuh Manager and Dashboard were successfully deployed and operational.

---

## Phase 2 – Agent Registration

### Objective

Connect the Kali Linux endpoint to the Wazuh Manager.

### Activities

- Installed the Wazuh Agent on Kali Linux.
- Registered the agent with the Wazuh Manager.
- Verified successful communication between the manager and the endpoint.

**Outcome:**  
The endpoint appeared as **Active** in the Wazuh Dashboard.

---

## Phase 3 – Log Collection & Authentication Monitoring

### Objective

Generate authentication and Linux system events.

### Activities

- Generated normal user activity.
- Created SSH login sessions.
- Produced authentication logs.
- Monitored PAM login sessions.

**Security Events Observed**

- SSH Authentication
- PAM Login Session Opened
- PAM Login Session Closed
- Successful Authentication

**Outcome:**  
Authentication events were successfully collected and displayed in the Wazuh Dashboard.

---

## Phase 4 – Brute Force Simulation

### Objective

Simulate repeated SSH login attempts.

### Activities

- Performed an SSH brute-force simulation using Hydra.
- Generated repeated authentication attempts.
- Reviewed authentication-related events.

**Security Events Observed**

- Failed Authentication Attempts
- SSH Login Events
- Authentication Logs

**Outcome:**  
The generated authentication activity was successfully captured for investigation.

---

## Phase 5 – File Integrity Monitoring (FIM)

### Objective

Verify that Wazuh detects file system changes.

### Activities

- Created a test file.
- Modified the file.
- Renamed the file.
- Deleted the file.

**Security Events Expected**

- File Created
- File Modified
- File Renamed
- File Deleted

**Outcome:**  
File system monitoring was tested to validate Wazuh's integrity monitoring capabilities.

---

## Phase 6 – Security Monitoring

### Objective

Monitor endpoint activity through the Wazuh Dashboard.

### Activities

- Reviewed Security Events.
- Investigated authentication logs.
- Observed Linux system activity.
- Monitored endpoint status.

**Outcome:**  
The dashboard successfully centralized endpoint security events.

---

## Phase 7 – Suspicious Command Execution

### Objective

Generate privileged and administrative activity.

### Activities

Executed commands such as:

```bash
sudo su
wget http://example.com
curl http://example.com
find / -name passwd
sudo cat /etc/shadow
ss -tulpn
history
```

**Security Events Observed**

- Successful sudo to ROOT executed
- PAM Login Sessions
- Authentication Events

**Outcome:**  
Privilege escalation and administrative activities were successfully monitored.

---

## Phase 8 – Threat Hunting

### Objective

Investigate collected security events using Wazuh.

### Activities

Performed searches for:

- Authentication Events
- SSH Activity
- Privilege Escalation
- AppArmor Alerts
- Agent Activity
- High Severity Events

Investigated:

- Authentication timeline
- Login sessions
- Privilege escalation
- AppArmor DENIED alerts
- Event correlation

**Outcome:**  
Threat hunting successfully identified authentication activity, privilege escalation, and Linux security alerts.

---

## Phase 9 – Incident Investigation

### Objective

Correlate events and document findings.

### Activities

- Reviewed authentication logs.
- Investigated SSH activity.
- Correlated PAM login sessions.
- Analyzed privilege escalation events.
- Examined AppArmor DENIED alerts.

**Findings**

The observed security events were generated intentionally within the controlled laboratory environment to evaluate Wazuh's monitoring and detection capabilities.

No evidence of an actual system compromise was identified.

---

## Conclusion

The Wazuh SOC Lab successfully demonstrated the complete lifecycle of a Security Operations Center workflow, including endpoint monitoring, log collection, authentication monitoring, threat detection, investigation, and threat hunting using Wazuh SIEM.
