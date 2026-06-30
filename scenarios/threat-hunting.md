# Threat Hunting

## Objective

Perform manual threat hunting using Wazuh Dashboard queries.

---

## Queries Used

Authentication Events

```
authentication
```

SSH Events

```
ssh
```

Privilege Escalation

```
sudo
```

Agent Events

```
agent.name:kali
```

AppArmor Events

```
AppArmor
```

High Severity Alerts

```
rule.level >= 5
```

---

## Investigation Steps

- Reviewed authentication events.
- Investigated SSH login activity.
- Analyzed privilege escalation events.
- Examined AppArmor DENIED alerts.
- Correlated related events using timestamps.

---

## Findings

Authentication events, privilege escalation, and AppArmor policy violations were successfully identified and investigated.
