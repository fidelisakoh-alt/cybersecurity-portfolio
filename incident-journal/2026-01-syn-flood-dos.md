# Incident Journal: SYN Flood Denial of Service

**Date:** 2026-01  
**Incident Type:** Denial of Service (DoS)  
**Attack Vector:** TCP SYN flood  
**Severity:** High  
**Status:** Mitigated / Under investigation

---

## Summary

Employees and customers experienced slow load times and connection failures when accessing the company website. In some cases, the website failed to load entirely and returned timeout errors.

Initial analysis indicated that the web server was overwhelmed by an unusually high number of incoming connection requests, preventing it from responding to legitimate users.

---

## Detection

The issue was detected after an automated monitoring alert reported abnormal traffic levels on the web server. Employees also reported being unable to access internal web resources, confirming a service disruption.

---

## Investigation

Network traffic was reviewed using a packet capture and log analysis tool to identify abnormal patterns. The captured data showed a high volume of incoming TCP connection requests originating from multiple external IP addresses.

Many of the requests initiated TCP connections but did not complete the full three-way handshake, leaving connections in a half-open state on the server.

---

## Analysis

The traffic pattern is consistent with a TCP SYN flood attack. In this type of attack, an attacker sends a large number of SYN packets to a server without completing the connection handshake.

As a result, the server allocates resources for each incomplete connection until it can no longer handle legitimate requests. This causes slow response times, connection timeouts, and service unavailability for real users.

No evidence was found to suggest data exfiltration or unauthorized access. The impact was limited to service availability.

---

## Impact

- Website availability was degraded or unavailable
- Employees were unable to access internal web resources
- Customer-facing services experienced disruption
- No data loss or system compromise was identified


---

## Current Status

Traffic filtering and rate-limiting controls were applied to reduce the impact of the attack. The incident was escalated to network and security engineering teams for further mitigation and monitoring.

----

## Suspected Root Cause

The most likely cause was an external SYN flood denial-of-service attack targeting the web server’s TCP connection handling.


---

## Recommended Next Steps

- Enable SYN flood protection and TCP connection rate limiting
- Implement or tune firewall and load balancer protections
- Monitor traffic patterns for recurring attack behavior
- Review incident response procedures for denial-of-service events

---

### Related Lab Work

This incident analysis is based on hands-on network traffic inspection and log analysis.

- 📂 Lab: [SYN Flood Traffic Analysis](../labs/syn-flood-traffic-analysis.md)


