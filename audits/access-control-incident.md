# Access Control Assessment – Unauthorised Payment Incident

## Project Description

In this exercise, I investigated an unauthorised financial transaction within a business environment. The objective was to analyse access logs, identify weaknesses in access control mechanisms, and recommend improvements to prevent similar incidents.

This activity demonstrates an understanding of authentication, authorisation, and the importance of enforcing proper access control policies.

---

## Incident Summary

An unauthorised payment was initiated to an unknown bank account. Although the transaction was stopped, the incident required investigation to determine how access controls were bypassed.

Event log analysis revealed that the activity was performed using an account belonging to a former employee with administrative privileges.

---

## Findings

### User Activity

- User: Robert Taylor Jr.  
- Date: 10/03/2023  
- Time: 08:29 AM  
- Device: Up2-NoGud  
- Access Level: Administrative  

The account used in the incident belonged to a user who should no longer have had access to the system.

---

## Identified Issues

- Excessive privileges were granted to the user, allowing administrative actions beyond what was necessary  
- The account remained active after the employee left the organisation  
- Lack of proper access revocation and account lifecycle management  

---

## Recommendations

1. **Implement least privilege access control**  
   Ensure users only have the minimum level of access required for their role, removing unnecessary administrative permissions.

2. **Introduce a formal offboarding process**  
   Immediately deactivate or remove access for employees who leave the organisation to prevent unauthorised system access.

---

## Key Skills Demonstrated

- Log analysis and incident investigation  
- Access control evaluation  
- Identification of privilege misuse  
- Risk mitigation planning  
- Security best practices (least privilege)

---

## Summary

This assessment highlights how weak access control practices can lead to security incidents. By enforcing least privilege and implementing proper account management processes, organisations can significantly reduce the risk of unauthorised access and financial fraud.