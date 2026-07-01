## Baseline Monitoring

### Objective

Establish a baseline of normal endpoint activity before generating security events.

### Activities

- Verified Wazuh agent connectivity.
- Generated routine Linux user activity.
- Collected authentication and system logs.
- Monitored endpoint health through the Wazuh Dashboard.

### Commands Executed

```bash
whoami
hostname
pwd
date
ls
sudo apt update
sudo systemctl restart ssh
```

### Security Events Observed

- Authentication Logs
- Linux System Logs
- User Activity
- Service Activity

### Outcome

A normal operating baseline was established, allowing future security events to be compared against expected system behavior.
