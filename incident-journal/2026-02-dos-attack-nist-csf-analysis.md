# Incident Journal: ICMP Flood Denial of Service (DoS) Attack

**Date:** 2026-02  
**Incident Type:** Denial of Service (DoS)  
**Attack Vector:** ICMP Flood  
**Severity:** High  
**Status:** Resolved and Mitigated  

---

## Summary

The organisation experienced a Denial of Service (DoS) attack that disrupted internal network services for approximately two hours. During the incident, legitimate internal users were unable to access network resources due to an overwhelming volume of incoming ICMP packets.

The attack exploited an unconfigured firewall, allowing excessive ICMP traffic into the network.

---

## Detection

The issue was detected when:

- Internal network services became unresponsive  
- Users reported inability to access shared resources  
- Network monitoring indicated abnormal traffic volume  

Investigation revealed a sudden spike in ICMP traffic originating from external sources.

---

## Investigation

Traffic analysis identified:

- A sustained flood of ICMP echo request (ping) packets  
- High packet volume overwhelming internal network resources  
- No rate limiting configured on the firewall  
- No source IP verification in place  

The firewall allowed unrestricted ICMP traffic into the internal network.

---

## Analysis

### Type of Attack

The incident was classified as an **ICMP Flood Denial of Service (DoS) attack**.

An ICMP flood attack works by sending excessive ICMP echo request packets to a target system. The target attempts to respond to each request, consuming bandwidth and processing power until legitimate traffic can no longer be handled.

### Systems Affected

- Internal network services  
- Network infrastructure  
- User access to shared resources  

No data exfiltration or system compromise was identified. The impact was limited to service availability.

---

## Root Cause

The primary vulnerability identified was:

- Firewall misconfiguration allowing unrestricted ICMP traffic  

Contributing factors:

- No rate limiting rules  
- No source IP address verification  
- Lack of abnormal traffic monitoring  

---

## Containment Actions

The incident response team implemented the following measures:

- Blocked incoming ICMP packets temporarily  
- Took non-critical services offline  
- Restored critical services first  
- Applied firewall configuration changes  

---

## Mitigation Implemented

To prevent recurrence, the following controls were deployed:

- Firewall rule to rate-limit incoming ICMP packets  
- Source IP address verification to detect spoofed packets  
- Network monitoring software for abnormal traffic detection  
- Intrusion Detection / Intrusion Prevention System (IDS/IPS) to filter suspicious traffic  

---

## Impact Assessment

- Duration: Approximately 2 hours  
- Business impact: Temporary service disruption  
- Data compromise: None identified  
- Financial impact: Operational downtime  

---

## Lessons Learned

- Firewall misconfiguration significantly increases attack surface  
- Rate limiting is critical for ICMP traffic  
- Real-time monitoring improves detection speed  
- Layered defense (firewall + IDS/IPS + monitoring) reduces risk  

---

## Recommendations

- Conduct regular firewall configuration audits  
- Implement baseline configuration documentation  
- Perform routine penetration testing  
- Continue monitoring ICMP traffic patterns  
- Review and test incident response procedures quarterly  

---

## Related Lab

This incident analysis is based on simulated DoS investigation and network hardening strategy implementation.

