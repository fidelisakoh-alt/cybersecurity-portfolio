# Network Hardening Risk Assessment  
**Organisation Type:** Social Media Platform  
**Assessment Type:** Preventative Security Risk Assessment  
**Focus:** Network hardening and access control  

---

## Overview

This assessment evaluates network security weaknesses identified after a data breach that exposed customer personal information. The objective is to recommend practical network hardening measures that reduce the risk of future breaches by addressing credential misuse, weak access controls, and insufficient traffic filtering.

---

## Identified Vulnerabilities

The following critical vulnerabilities were identified during the assessment:

- Employees share passwords
- Administrative database credentials remain set to default values
- Firewall rules are not configured to filter inbound and outbound traffic
- Multi-Factor Authentication (MFA) is not implemented

---

## Recommended Network Hardening Measures

### 1. Multi-Factor Authentication (MFA)

MFA requires users to verify their identity using more than one authentication factor, such as a password combined with a one-time code or biometric verification.

### 2. Password Policies and Credential Management

Strong password policies enforce unique credentials, prohibit password sharing, require regular password updates, and mandate the removal of default administrative passwords.

### 3. Firewall Rule Configuration and Port Filtering

Firewall rules control which traffic is allowed into and out of the network by filtering connections based on ports, protocols, and source or destination addresses.

---

## Effectiveness of Recommended Controls

### Multi-Factor Authentication (MFA)

MFA is effective because it protects systems even when passwords are compromised. If an attacker gains access to login credentials through password sharing or reuse, MFA prevents access without the second authentication factor. MFA should be enforced continuously and reviewed regularly to ensure coverage across all critical systems.

### Password Policies and Credential Management

Password policies reduce the likelihood of unauthorized access by enforcing strong, unique credentials and eliminating default administrative passwords. These controls should be applied continuously and reviewed periodically to ensure compliance and effectiveness.

### Firewall Rule Configuration and Port Filtering

Proper firewall configuration limits exposure by allowing only necessary network traffic. Port filtering reduces the attack surface and prevents unauthorized services from being accessible. Firewall rules should be implemented immediately and reviewed regularly, particularly after infrastructure changes.

---

## Conclusion

Implementing MFA, enforcing strong password policies, and configuring firewall rules significantly strengthens the organization’s network security posture. These controls address the root causes of the identified vulnerabilities and reduce the likelihood of future data breaches by limiting unauthorized access and network exposure.
