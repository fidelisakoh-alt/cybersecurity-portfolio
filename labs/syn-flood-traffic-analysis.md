# Lab: SYN Flood Traffic Analysis

## Objective
Analyse TCP network traffic to identify characteristics of a SYN flood denial-of-service attack and understand how incomplete TCP handshakes impact server availability.

---

## Scenario

Users reported slow performance and failed connections when attempting to access a company website. Monitoring alerts indicated unusually high inbound traffic to the web server.

The goal of this lab was to inspect captured network traffic and determine whether the disruption was caused by a denial-of-service attack.


---

## Tools Used

- Network traffic logs (TCP/HTTP)
- Packet analysis concepts
- TCP/IP model

----

## Background

The Transmission Control Protocol (TCP) establishes connections using a three-way handshake:

1. SYN – Client requests a connection  
2. SYN-ACK – Server acknowledges the request  
3. ACK – Client confirms the connection  

If the final ACK is not received, the connection remains half-open and continues to consume server resources.

----

## Observations

Analysis of the traffic logs revealed the following patterns:

- A high volume of incoming TCP SYN packets
- Multiple source IP addresses targeting the same destination server
- Very few corresponding ACK packets
- Many TCP connections remained in a half-open state

---

## Packet Evidence (Summarised)

- Repeated TCP SYN packets sent to the web server
- Incomplete TCP handshakes observed
- No sustained data transfer following connection attempts

---

## Analysis

The observed traffic pattern matches the behavior of a TCP SYN flood attack. In this attack, an attacker overwhelms a server by sending large numbers of SYN packets without completing the handshake.

Because the server allocates memory and processing resources for each half-open connection, legitimate users are eventually unable to establish connections, resulting in service disruption.


---

## Conclusion

The service outage was caused by a denial-of-service condition resulting from a TCP SYN flood. The issue affected system availability but did not indicate data compromise or unauthorized access.

---

## Skills Demonstrated

- Network traffic analysis
- TCP handshake troubleshooting
- Identification of denial-of-service attacks
- Incident documentation and reporting

---

## Related Incident Report

This lab directly informed the following incident journal entry:

- 📝 Incident Journal: [SYN Flood Denial of Service](../incident-journal/2026-01-syn-flood-dos.md)



