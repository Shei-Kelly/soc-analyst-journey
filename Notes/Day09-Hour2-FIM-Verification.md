# Day 9 – Hour 2: File Integrity Monitoring Verification

## Objective
Verify that Wazuh File Integrity Monitoring (FIM) is enabled and properly configured.

## FIM Status
- Status: Enabled
- Configuration: `<disabled>no</disabled>`

## Scan Frequency
- Frequency: 43200 seconds
- Equivalent: Every 12 hours

## Monitored Directories
- /etc
- /usr/bin
- /usr/sbin
- /bin
- /sbin
- /boot

## Ignored Files
- /etc/mtab
- /etc/random-seed
- /etc/adjtime
- /etc/hosts.deny
- Others specified in the configuration

## Analyst Observations
The Wazuh agent is configured to monitor critical Linux system directories while excluding files that change frequently during normal operation. This reduces false positives and helps focus investigations on meaningful file changes.
