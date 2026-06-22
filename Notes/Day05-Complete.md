# Day 5 – Threat Hunting Fundamentals

## Topics Covered

### Threat Hunting

* Proactive search for threats
* Hypothesis-driven investigations
* Difference between SOC monitoring and threat hunting

### IOC vs IOA

IOC (Indicator of Compromise):

* Malicious IPs
* Malicious domains
* Malware hashes

IOA (Indicator of Attack):

* Failed logins
* PowerShell execution
* Suspicious process activity

### Hunting Suspicious Logins

* Event ID 4625
* Event ID 4624
* Brute-force indicators
* Password spraying indicators

### Hunting PowerShell Activity

* Event ID 4688
* Encoded commands
* Hidden windows
* No-profile execution

### Hunting Network Activity

* DNS queries
* Newly registered domains
* DGA-like domains
* External HTTPS connections

### MITRE ATT&CK Mapping

* Credential Access
* Initial Access
* Execution
* Defense Evasion
* Command and Control

### AI-Assisted Threat Hunting

* Log analysis
* Investigation guidance
* MITRE ATT&CK mapping
* Incident narrative generation

## Key Lessons Learned

* Threat hunting is proactive.
* Evidence is more important than assumptions.
* Attack chains provide context.
* DNS activity can reveal attacker infrastructure.
* PowerShell is frequently abused by attackers.
* AI can accelerate investigations but must be validated.

## Skills Gained

* Threat hunting methodology
* Log correlation
* IOC identification
* IOA identification
* MITRE ATT&CK mapping
* Threat-hunting reporting
* AI-assisted investigation

## Outcome

I can now:

* Hunt suspicious logins
* Hunt PowerShell abuse
* Investigate DNS activity
* Build attack timelines
* Create threat-hunting reports
* Escalate incidents appropriately
