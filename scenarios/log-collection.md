# Log Collection

## Objective

Verify that the Wazuh Manager successfully collects authentication and Linux system logs from the monitored endpoint.

---

## Commands Executed

### System Information

```bash
whoami
hostname
hostname -I
pwd
date
```

### Package Management

```bash
sudo apt update
```

### User Activity

```bash
sudo adduser analyst
sudo deluser analyst
```

### Privilege Escalation

```bash
sudo su
exit
```

### SSH Service

```bash
sudo systemctl restart ssh
```

---

## Expected Logs

The following log types were generated:

- Authentication Logs
- User Management Events
- Privilege Escalation
- SSH Service Logs
- System Logs

---

## Detection

Navigate to:

```
Security Events
```

Search:

```
authentication
```

or

```
agent.name:kali
```

---

## Result

The Wazuh Manager successfully collected endpoint logs and displayed them in the Security Events dashboard.
