# Day 5 – Hour 3: Hunting Suspicious PowerShell Activity

## Indicators

- PowerShell execution
- Encoded commands (-enc)
- Hidden execution (-w hidden)
- Unusual parent-child processes
- Suspicious DNS queries
- External HTTPS communication

## Common Suspicious Pattern

winword.exe
↓
powershell.exe
↓
DNS Query
↓
HTTPS Connection

## MITRE ATT&CK Mapping

- Initial Access
- Execution
- Defense Evasion
- Command and Control

## Key Insight

PowerShell is a legitimate administrative tool that is frequently abused by attackers. Encoded and hidden PowerShell commands should be investigated immediately.
