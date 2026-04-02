# Data Leak Assessment – Least Privilege Failure

## Project Description

In this exercise, I analysed a data leak incident at an educational technology company where confidential internal documents were unintentionally shared with an external party. The objective was to identify the root cause of the leak, evaluate existing security controls, and recommend improvements based on the principle of least privilege.

This activity demonstrates an understanding of data protection, access control, and applying NIST SP 800-53 security controls to reduce the risk of data exposure.

---

## Incident Summary

A sales manager shared access to a folder containing sensitive internal documents, including product plans, customer analytics, and marketing materials. Access to the folder was not revoked after the meeting.

During a sales call, a representative accidentally shared the entire folder instead of specific materials with an external business partner. The partner then posted the link publicly, resulting in a data leak.

---

## Identified Issues

The data leak occurred because access to sensitive internal documents was not restricted or revoked after the meeting. The sales representative also had excessive access and accidentally shared the entire folder instead of specific files, demonstrating a failure to enforce the principle of least privilege.

---

## Control Review (NIST SP 800-53 AC-6)

NIST SP 800-53 AC-6 focuses on enforcing the principle of least privilege by ensuring users only have access to the minimum resources required to perform their tasks. It also includes controls such as restricting access based on roles, auditing permissions, and limiting unnecessary privileges.

---

## Recommendations

1. **Role-based access control (RBAC)**  
   Restrict access to sensitive folders based on user roles so only authorised employees can view or share specific files.

2. **Automatic access expiration and audits**  
   Implement time-based access controls and regular permission reviews to ensure access to sensitive data is removed when no longer required.

---

## Justification

These improvements reduce the risk of data leaks by limiting access to sensitive information and ensuring permissions are regularly reviewed and revoked. This prevents employees from having unnecessary access and reduces the likelihood of accidental or unauthorised data sharing.

---

## Key Skills Demonstrated

- Data leak analysis  
- Root cause identification  
- Application of least privilege principles  
- Security control evaluation (NIST SP 800-53)  
- Risk reduction and mitigation planning  
- Clear security communication  

---

## Summary

This assessment highlights how failures in access control and oversight can lead to data leaks. By enforcing least privilege and implementing stronger access management practices, organisations can significantly reduce the risk of accidental data exposure and improve overall information security.