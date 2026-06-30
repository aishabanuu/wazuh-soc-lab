# SSH Authentication Monitoring

## Objective

Generate SSH authentication events and verify their detection in Wazuh.

---

## Commands Executed

From Kali:

```bash
ssh ash@172.16.61.130
```

Exit the SSH session:

```bash
exit
```

---

## Expected Logs

- Successful SSH Login
- PAM Login Session Opened
- PAM Login Session Closed
- Authentication Success

---

## Dashboard Investigation

Navigate to:

```
Security Events
```

Search:

```
ssh
```

or

```
authentication
```

---

## Result

SSH authentication events were successfully collected and visualized in the Wazuh Dashboard.
