# Case Study 01: Potential Account Compromise Investigation

## Overview

This case study documents the investigation of a suspicious authentication and execution sequence identified during SOC analysis.

## Alert Information

**Alert Name:** Multiple Failed Login Attempts

**Affected Account:** Administrator

**Source IP:** 203.0.113.50

**Initial Severity:** Medium

---

## Timeline of Events

| Time | Event |
|--------|--------|
| 13:55 | Event ID 4625 – Failed Login |
| 13:56 | Event ID 4625 – Failed Login |
| 13:57 | Event ID 4625 – Failed Login |
| 13:58 | Event ID 4624 – Successful Login |
| 13:59 | Event ID 4688 – PowerShell Execution |
| 14:00 | DNS Query – update-security-check.xyz |
| 14:01 | HTTPS Connection – update-security-check.xyz |

---

## Investigation Findings

### Authentication Activity

Multiple failed login attempts were observed against the Administrator account, followed by a successful login from the same source IP.

### Process Execution

PowerShell was executed immediately after successful authentication.

### Network Activity

The host queried and connected to an external domain shortly after PowerShell execution.

---

## MITRE ATT&CK Mapping

| Activity | Tactic |
|-----------|----------|
| Failed Login Attempts | Credential Access |
| Successful Login | Initial Access |
| PowerShell Execution | Execution |
| DNS Query | Command and Control |
| HTTPS Connection | Command and Control |

---

## Risk Assessment

The activity was classified as a Potential Security Incident due to the combination of suspicious authentication activity, command execution, and outbound communication.

---

## Incident Narrative

Multiple failed login attempts were observed against the Administrator account. A successful login occurred shortly afterward, followed by PowerShell execution. The host then queried and communicated with an external domain. This sequence suggests possible credential compromise, command execution, and external communication consistent with attacker behavior.

---

## Recommended Actions

1. Escalate to Tier 2 / Incident Response.
2. Review PowerShell command history.
3. Investigate domain reputation.
4. Search for similar activity on other hosts.
5. Assess the need for host isolation.

---

## Lessons Learned

- Authentication logs should never be analyzed in isolation.
- Log correlation is critical for identifying attack chains.
- MITRE ATT&CK provides a structured way to describe attacker behavior.
- PowerShell activity following suspicious authentication events should be investigated promptly.
