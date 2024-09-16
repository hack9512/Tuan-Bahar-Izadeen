# Home Asset Inventory

## Project Description
One of the most valuable assets in the world today is **information**. Most information is accessed over a network, and a variety of devices tend to be connected to the network. Each of these devices is a potential entry point to other assets.

Creating an inventory of network devices can be a useful asset management tool. This inventory highlights **sensitive assets** that require extra protection.

This project involves identifying and cataloging devices connected to a home office network, assessing their importance, and determining whether they contain sensitive information requiring additional security measures.

## Categories for Sensitivity Levels
- **Restricted**: Need-to-know access only.
- **Confidential**: Limited to specific users.
- **Internal-only**: Available to users within the premises.
- **Public**: Accessible by anyone.

---

## Asset Inventory Table

| Asset                  | Network Access | Owner                     | Location           | Notes                                                                                   | Sensitivity    |
|------------------------|----------------|----------------------------|--------------------|-----------------------------------------------------------------------------------------|----------------|
| **Network Router**      | Continuous     | Internet service provider (ISP) | On-premises        | Has a 2.4 GHz and 5 GHz connection. All devices on the home network connect to 5 GHz.    | Confidential   |
| **Desktop**             | Occasional     | Homeowner                  | On-premises        | Contains private information, like photos.                                               | Restricted     |
| **Guest Smartphone**    | Occasional     | Friend                     | On and off-premises | Connects to my home network.                                                             | Internal-only  |
| **Smart Home Devices**  | Occasional     | Homeowner                  | On and off-premises | Connects to my home network.                                                             | Internal-only  |
| **Storage Devices/Servers** | Continuous     | Cloud provider             | On-premises        | Contains database for my projects.                                                      | Confidential   |
| **Laptop**              | Occasional     | Homeowner                  | On-premises        | Contains work files.                                                                     | Restricted     |

---

## Risk Assessment

### Asset: 
The assets at risk of being harmed, damaged, or stolen.

### Risk(s): 
Potential risks to the organization's information system and data.

### Description: 
Vulnerabilities that might lead to a security incident.

### Likelihood:
Score from 1-3 based on the likelihood of vulnerabilities being exploited:
- **1**: Low likelihood
- **2**: Moderate likelihood
- **3**: High likelihood

### Severity:
Score from 1-3 based on the potential damage the threat could cause to the business:
- **1**: Low security impact
- **2**: Moderate severity impact
- **3**: High severity impact

### Priority:
How quickly a risk should be addressed to avoid a potential incident. Use the following formula to calculate the overall risk score:  
**Likelihood x Severity = Risk**

---
## Risk Assessment Matrix

| Likelihood ↓ / Severity → | 1 (Low Impact)       | 2 (Moderate Impact)  | 3 (High Impact)      |
|---------------------------|----------------------|----------------------|----------------------|
| **1 (Low Likelihood)**     | Low Risk             | Low-Moderate Risk     | Moderate Risk         |
| **2 (Moderate Likelihood)**| Low-Moderate Risk    | Moderate Risk         | High Risk             |
| **3 (High Likelihood)**    | Moderate Risk        | High Risk             | Critical Risk         |
---

## Conclusion
By compiling an asset inventory, homeowners can effectively classify devices based on their sensitivity and importance. This enables better **risk management** and **protection** of valuable information and assets connected to the network.

---

*Created by: T B Izadeen - Cybersecurity Portfolio*


