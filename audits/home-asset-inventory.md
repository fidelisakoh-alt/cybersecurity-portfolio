# Home Asset Inventory

## Project Description

In this exercise, I created an asset inventory for a home office network to identify connected devices and assess their security risk. The objective was to evaluate each asset based on its usage, exposure to the network, and the potential impact if compromised.

This activity demonstrates an understanding of asset management, risk evaluation, and sensitivity classification.

---

## Asset Inventory

| Asset | Network Access | Owner | Location | Notes | Sensitivity |
|------|--------------|------|----------|------|------------|
| Network Router | Continuous | ISP | On-premises | Central network device managing all traffic. If compromised, attacker could control or monitor all network activity. | Confidential |
| Desktop | Occasional | Homeowner | On-premises | Stores personal and potentially sensitive data such as files and photos. Risk of data exposure if accessed. | Restricted |
| Guest Smartphone | Occasional | Friend | On and off-premises | External device connecting to network. Potential risk if device is compromised or insecure. | Internal-only |
| Consoles | Occasional | Homeowner | On-premises | Connected to network but limited sensitive data. Could still be used as an entry point if vulnerable. | Internal-only |
| Apple TV | Occasional | Homeowner | On-premises | Streaming device connected to network. Low data sensitivity but potential lateral movement risk. | Internal-only |
| Smart Home Devices | Continuous | Homeowner | On-premises | Controls appliances such as heating and lighting. Always connected, increasing exposure to network-based attacks. | Restricted |

---

## Risk Considerations

Each asset was evaluated based on:

- The type of data it stores or accesses  
- Its level of network exposure  
- The potential impact if compromised  

Devices with high control over the network or sensitive data were classified as **Confidential** or **Restricted**, while lower-risk devices were classified as **Internal-only**.

---

## Key Skills Demonstrated

- Asset identification and inventory management  
- Risk-based thinking  
- Sensitivity classification  
- Understanding of network exposure and attack surfaces  

---

## Summary

This activity demonstrates how asset inventory supports security by identifying devices that require stronger protection. By classifying assets based on their sensitivity and exposure, security efforts can be prioritised to reduce the risk of unauthorised access or data breaches.