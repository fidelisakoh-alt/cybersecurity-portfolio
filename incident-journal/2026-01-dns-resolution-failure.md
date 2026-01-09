### Related Lab Work
This incident analysis is based on hands-on packet analysis conducted using `tcpdump`.

- 📂 Lab: [DNS & ICMP Traffic Analysis](../labs/dns-icmp-traffic-analysis.md)

# Incident Journal: DNS Resolution Failure

**Date:** 2026-01  
**Incident Type:** Service Availability – DNS Resolution Failure  
**Severity:** Medium  
**Status:** Escalated to engineering

---

## Summary
Multiple users reported being unable to access the website `www.yummyrecipesforme.com`. When attempting to load the site, users received a “destination port unreachable” error. Initial analysis indicated a failure in DNS resolution rather than a general network outage.

---

## Detection
The issue was first reported by client customers after repeated failed attempts to access the website. The problem was reproduced internally by attempting to load the website and observing the same error message.

---

## Investigation
Network traffic was captured using `tcpdump` while attempting to access the affected domain.

Key observations:
- DNS queries sent via UDP
- Destination port **53**
- ICMP error responses returned
- Repeated message: `udp port 53 unreachable`

---

## Analysis
ICMP “port unreachable” messages indicate that the DNS server was reachable but not accepting traffic on UDP port 53. Because DNS resolution failed, the browser could not obtain an IP address and therefore could not initiate an HTTPS request.

Protocols involved:
- **DNS** (Application layer)
- **UDP** (Transport layer)
- **ICMP** (Internet layer)

This confirms a DNS service-level failure rather than a web server outage.

---

## Impact
- Website unavailable to users
- Services dependent on DNS resolution disrupted
- No evidence of data compromise observed

---

## Current Status
The incident was escalated to network and security engineering teams. Remediation was ongoing at the time of reporting.

---

## Suspected Root Cause
- DNS service outage or misconfiguration  
**or**  
- Firewall rule blocking UDP port 53

---

## Recommended Next Steps
- Verify DNS service status
- Review firewall rules for UDP port 53
- Restore DNS availability
- Monitor traffic post-remediation
