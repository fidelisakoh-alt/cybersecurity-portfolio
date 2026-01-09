# Lab: DNS & ICMP Traffic Analysis

## Objective
Analyse network traffic using `tcpdump` to identify the cause of a DNS resolution failure and interpret ICMP error messages.

---

## Scenario
Users were unable to access `www.yummyrecipesforme.com` and received a “destination port unreachable” error. The goal was to determine which protocol and service were affected.

---

## Tools Used
- tcpdump
- TCP/IP model
- DNS and ICMP analysis

---

## Observations
- DNS queries sent using UDP
- Destination port: 53
- DNS server returned ICMP error messages
- Repeated message: `udp port 53 unreachable`

---

## Protocols Identified
- DNS (Application layer)
- UDP (Transport layer)
- ICMP (Internet layer)

---

## Packet Evidence (Summarised)
UDP 192.51.100.15 → 203.0.113.2 domain A?
ICMP 203.0.113.2 → 192.51.100.15 udp port 53 unreachable




---

## Conclusion
The DNS server was reachable but not accepting traffic on UDP port 53. This indicates a DNS service outage or firewall restriction rather than a general network failure.

---

## Related Incident Report
- 📝 Incident Journal: [DNS Resolution Failure](../incident-journal/2026-01-dns-resolution-failure.md)
