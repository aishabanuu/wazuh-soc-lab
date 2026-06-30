# Brute Force Simulation

## Objective

Simulate repeated SSH login attempts to generate authentication events.

---

## Tool

Hydra

---

## Commands Executed

```bash
hydra -V -t 4 -l ash -P /usr/share/wordlists/rockyou.txt ssh://172.16.61.130
```

---

## Expected Events

- Failed Authentication
- SSH Login Attempts
- Authentication Monitoring
- Security Event Generation

---

## Investigation

Navigate to:

```
Security Events
```

Search:

```
sshd
```

or

```
authentication
```

---

## Outcome

Repeated SSH login attempts generated authentication-related events for investigation.
