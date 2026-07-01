## Network Reconnaissance

### Objective

Simulate reconnaissance activity against the monitored server.

### Activities

- Performed TCP SYN scan.
- Performed service and version detection.

### Commands Executed

```bash
nmap -sS <TARGET-IP>

nmap -A <TARGET-IP>
```

### Security Events Expected

- Network Scan Activity
- Reconnaissance Indicators
- Service Enumeration

### Outcome

Network reconnaissance generated traffic that can be analyzed within the Wazuh environment and correlated with other security events.
