# USB Baiting Risk Assessment

## Project Description

In this exercise, I assessed the security risks of an unfamiliar USB drive found in a workplace parking lot. The objective was to analyse the contents of the drive, consider how an attacker might exploit the information, and recommend controls to reduce the risk of USB baiting attacks.

This activity demonstrates an understanding of attack vectors, social engineering, removable media risks, and safe investigation practices.

---

## Scenario Summary

A USB drive with the hospital’s logo was found in the parking lot of Rhetorical Hospital. The device appeared to belong to an employee named Jorge and contained a mixture of personal and work-related files.

The USB drive was investigated in a virtual environment rather than being opened on a normal workstation, reducing the risk of malware spreading to other systems.

---

## Contents Identified

The USB drive contained a mixture of personal and work-related files, including family photos, dog pictures, a wedding list, a resume, a new hire letter, employee budget information, and shift schedules.

Some of these files may contain personally identifiable information (PII) or sensitive business information. Storing personal and work files together increases the risk of accidental exposure.

---

## Attacker Mindset

An attacker could use the personal files to learn about Jorge’s family, pets, relationships, or interests, making phishing or social engineering attempts more convincing.

Work files such as shift schedules, new hire letters, and employee documents could reveal internal processes and staff information. The USB may also have been planted to encourage someone to plug it in and trigger malware.

---

## Risk Analysis

A USB drive could contain malware such as spyware, ransomware, keyloggers, or a backdoor that gives an attacker access to hospital systems. If another employee plugged it into a normal workstation, it could infect the device or spread across the network.

Even if the USB contained no malware, the information stored on it could still create risk. Personal and work-related files could be used for social engineering, phishing, identity theft, or targeted attacks against employees.

---

## Recommended Controls

### Technical Controls

- Disable USB auto-run on company devices
- Use endpoint protection to scan removable media
- Restrict USB access on sensitive systems
- Investigate unknown USB devices only in isolated virtual environments

### Operational Controls

- Create a clear process for reporting found devices
- Require staff to hand unknown USBs to IT or security teams
- Separate personal and business storage devices

### Managerial Controls

- Provide regular security awareness training
- Establish a removable media policy
- Communicate the risks of USB baiting and social engineering

---

## Key Skills Demonstrated

- Attack vector analysis
- USB baiting risk assessment
- Social engineering awareness
- Identification of personally identifiable information (PII)
- Recommendation of technical, operational, and managerial controls
- Safe investigation practices using virtual environments

---

## Summary

This assessment shows how a simple USB drive can become a serious security risk. Unknown removable media can expose sensitive information, support social engineering attacks, or deliver malware into an organisation.

By using technical controls, clear procedures, and staff awareness training, organisations can reduce the likelihood of USB baiting attacks and improve their overall security posture.