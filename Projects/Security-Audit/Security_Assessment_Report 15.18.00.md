
# Security Assessment Report

## 1. Overview

This security assessment was conducted for Botium Toys, a small U.S. business that develops and sells toys. As the company's online presence has expanded, the IT department is under increased pressure to maintain security and compliance. This report outlines the findings from the internal security audit conducted, focusing on the controls and compliance requirements.

## 2. Scope and Goals

- **Scope:** The audit covered the entire security program at Botium Toys, including all assets, internal processes, and procedures.
- **Goals:** The primary goal was to assess existing assets, complete the controls and compliance checklist, and identify areas for improvement in Botium Toys' security posture.

## 3. Findings

### 3.1 Controls Assessment

| **Control** | **Status** | **Explanation** |
|-------------|------------|-----------------|
| Least Privilege | Not Implemented | All employees currently have access to customer data; privileges need to be limited. |
| Disaster Recovery Plans | Not Implemented | No disaster recovery plans are in place. |
| Password Policies | Not Implemented | Existing password policies are minimal and inadequate. |
| Separation of Duties | Not Implemented | Not implemented, increasing the risk of fraud. |
| Firewall | Implemented | The firewall blocks traffic based on security rules. |
| Intrusion Detection System (IDS) | Not Implemented | No IDS is in place. |
| Backups | Not Implemented | No backups of critical data exist. |
| Antivirus Software | Implemented | Antivirus software is installed and monitored regularly. |
| Manual Monitoring for Legacy Systems | Not Implemented | Legacy systems are monitored but lack a regular schedule. |
| Encryption | Not Implemented | Encryption is not used to secure sensitive data. |
| Password Management System | Not Implemented | No centralized password management system is in place. |
| Physical Security (Locks, CCTV) | Implemented | Locks and CCTV are in place and functioning. |
| Fire Detection/Prevention | Implemented | Fire detection and prevention systems are operational. |

### 3.2 Compliance Assessment

**Payment Card Industry Data Security Standard (PCI DSS)**

| **Best Practice** | **Status** | **Explanation** |
|-------------------|------------|-----------------|
| Authorized access to credit card data | Not Adhered | All employees can access credit card data. |
| Secure environment for credit card data | Not Adhered | Credit card information is not encrypted. |
| Data encryption | Not Adhered | Encryption procedures are not implemented. |
| Secure password management | Not Adhered | Password policies are inadequate, and no management system exists. |

**General Data Protection Regulation (GDPR)**

| **Best Practice** | **Status** | **Explanation** |
|-------------------|------------|-----------------|
| Data privacy/security for E.U. customers | Not Adhered | Encryption is not used for sensitive information. |
| Breach notification plan | Adhered | A plan is in place to notify E.U. customers within 72 hours. |
| Data classification/inventory | Not Adhered | Data has been inventoried but not classified. |
| Enforced privacy policies | Adhered | Privacy policies and procedures are enforced. |

**System and Organization Controls (SOC type 1, SOC type 2)**

| **Best Practice** | **Status** | **Explanation** |
|-------------------|------------|-----------------|
| User access policies | Not Adhered | Controls for Least Privilege and Separation of Duties are not in place. |
| Confidentiality of sensitive data | Not Adhered | Sensitive data is not encrypted. |
| Data integrity | Adhered | Data integrity measures are in place. |
| Data availability | Not Adhered | Data access is not restricted to authorized personnel. |

## 4. Recommendations

To improve the security posture and compliance of Botium Toys, the following actions are recommended:

- **Implement Least Privilege:** Limit data access to only those employees who need it to perform their duties.
- **Develop Disaster Recovery Plans:** Establish and regularly test disaster recovery plans to ensure business continuity.
- **Strengthen Password Policies:** Update password policies to meet current security standards and enforce them through a centralized management system.
- **Establish Separation of Duties:** Implement separation of duties to reduce the risk of fraud and unauthorized access.
- **Install Intrusion Detection System (IDS):** Deploy an IDS to detect and respond to potential security incidents.
- **Enable Data Encryption:** Encrypt sensitive data, especially credit card information, to protect against data breaches.
- **Schedule Regular Monitoring for Legacy Systems:** Create and adhere to a regular monitoring schedule for legacy systems.
- **Classify and Inventory Data:** Properly classify all data to identify and protect sensitive information more effectively.

## 5. Conclusion

This security assessment has identified several critical areas where Botium Toys needs to improve its security controls and compliance measures. By implementing the recommended actions, the company can significantly enhance its security posture and reduce the risk of non-compliance with relevant regulations.
