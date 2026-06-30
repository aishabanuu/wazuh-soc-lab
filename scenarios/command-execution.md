# Suspicious Command Execution

## Objective

Generate command execution activity that can be investigated through Wazuh.

---

## Commands Executed

```bash
sudo su

wget http://example.com

curl http://example.com

find / -name passwd 2>/dev/null

sudo cat /etc/shadow

ss -tulpn

history
```

---

## Security Events

Expected observations include:

- Successful sudo to ROOT executed
- PAM Login Session Opened
- PAM Login Session Closed
- Authentication Logs

---

## Investigation

Search for:

```
sudo
```

```
PAM
```

```
agent.name:kali
```

---

## Result

Privilege escalation and authentication events were successfully monitored.
