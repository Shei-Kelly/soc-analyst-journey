# Day 02 - Most Important Protocols for SOC Analysts

## Overview

Protocols are sets of rules that devices use to communicate over a network. Understanding common protocols is essential for SOC analysts because they appear frequently in alerts, investigations, packet captures, firewall logs, and SIEM dashboards.

---

# DNS (Domain Name System)

## Purpose

Translates domain names into IP addresses.

### Example

Instead of remembering:

```text
142.250.190.78
```

Users type:

```text
www.google.com
```

DNS resolves the domain name to an IP address.

## Port

```text
53
```

## SOC Relevance

SOC analysts investigate DNS traffic because attackers often:

* Contact malicious domains
* Use DNS tunneling
* Communicate with command-and-control (C2) servers

### Example Alert

```text
Host repeatedly querying suspicious-domain.xyz
```

This may indicate malware activity.

---

# HTTP (Hypertext Transfer Protocol)

## Purpose

Transfers web content between browsers and web servers.

### Example

```text
http://example.com
```

## Port

```text
80
```

## Characteristics

* Data is transmitted in clear text
* Not encrypted
* Vulnerable to interception

## SOC Relevance

Analysts investigate:

* Malicious downloads
* Web attacks
* Suspicious web requests

### Example

```text
GET /malware.exe
```

This may indicate a malware download.

---

# HTTPS (Hypertext Transfer Protocol Secure)

## Purpose

Provides secure and encrypted web communication.

### Example

```text
https://example.com
```

## Port

```text
443
```

## Characteristics

* Encrypts traffic
* Protects confidentiality
* Uses TLS/SSL

## SOC Relevance

Analysts monitor:

* Connections to suspicious domains
* Unusual encrypted traffic
* Malware communication over HTTPS

### Example Alert

```text
Workstation communicating with unknown external server over HTTPS
```

Requires investigation.

---

# SSH (Secure Shell)

## Purpose

Remote administration of Linux and Unix systems.

### Port

```text
22
```

## Example

Administrators use SSH to remotely manage servers.

```text
ssh admin@192.168.1.10
```

## SOC Relevance

Analysts investigate:

* Brute-force attacks
* Unauthorized logins
* Remote access attempts

### Example Alert

```text
500 failed SSH login attempts from one IP address
```

Possible brute-force attack.

---

# RDP (Remote Desktop Protocol)

## Purpose

Provides remote graphical access to Windows systems.

### Port

```text
3389
```

## Example

Administrators use RDP to manage Windows servers remotely.

## SOC Relevance

RDP is a common attack target.

Analysts investigate:

* Unauthorized access
* Brute-force attacks
* Lateral movement

### Example Alert

```text
Multiple failed RDP login attempts followed by a successful login
```

Potential compromise.

---

# Common Ports Every SOC Analyst Should Know

| Protocol | Purpose               | Port |
| -------- | --------------------- | ---- |
| DNS      | Name Resolution       | 53   |
| HTTP     | Web Traffic           | 80   |
| HTTPS    | Secure Web Traffic    | 443  |
| SSH      | Remote Administration | 22   |
| RDP      | Remote Desktop Access | 3389 |

---

# SOC Analyst Investigation Questions

When reviewing network activity, ask:

1. Which protocol was used?
2. Which port was used?
3. Is the communication expected?
4. Is the destination trusted?
5. Does the activity match normal behavior?

---

# Key Takeaways

* DNS resolves domain names to IP addresses.
* HTTP transfers web content in plain text.
* HTTPS encrypts web traffic.
* SSH provides secure remote administration.
* RDP allows remote access to Windows systems.
* SSH and RDP are common targets for brute-force attacks.
* DNS and HTTPS frequently appear in malware investigations.

## Day 2 Progress

Completed:

* Networking Fundamentals
* IP Addresses
* MAC Addresses
* Ports
* Protocols
* TCP vs UDP
* DNS
* HTTP
* HTTPS
* SSH
* RDP

Next Topic:
DNS Deep Dive and Wireshark Basics
