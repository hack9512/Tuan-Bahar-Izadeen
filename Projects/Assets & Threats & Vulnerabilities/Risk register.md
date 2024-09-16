# Risk Register

### Operational Environment
The bank is located in a coastal area with low crime rates. Many people and systems handle the bank's data—100 on-premise employees and 20 remote employees. The customer base includes 2,000 individual accounts and 200 commercial accounts. The bank's services are marketed by a professional sports team and ten local businesses in the community. Strict financial regulations require the bank to secure its data and funds, ensuring they have enough cash available each day to meet Federal Reserve requirements.

---

## Asset Risk Table

| Asset                  | Risk(s)                      | Description                                                       | Likelihood | Severity | Priority |
|------------------------|------------------------------|-------------------------------------------------------------------|------------|----------|----------|
| **Funds**               | Business email compromise    | An employee is tricked into sharing confidential information.      | 1          | 3        | 3        |
| **User Database**       | Compromised database         | Customer data is poorly encrypted.                                | 2          | 6        | 12       |
| **Financial Records**   | Data leak                    | A database server of backed-up data is publicly accessible.        | 2          | 6        | 12       |
| **Cash**                | Theft                        | The bank's safe is left unlocked.                                  | 1          | 3        | 3        |
| **Supply Chain**        | Supply chain disruption      | Delivery delays due to natural disasters.                          | 1          | 3        | 3        |

---

### Notes
How are security events possible considering the risks the asset faces in its operating environment?

- Doing business with third-party companies might increase the risks to data since other entities might have access to it.
- Theft and supply chain disruption due to natural disasters can be ruled out since it is a low-crime area and natural disasters are unlikely to occur.

---

## Definitions

- **Asset**: The asset at risk of being harmed, damaged, or stolen.
- **Risk(s)**: A potential risk to the organization's information systems and data.
- **Description**: A vulnerability that might lead to a security incident.
- **Likelihood**: A score from 1-3 based on the chances of a vulnerability being exploited. A 1 means low likelihood, a 2 means moderate likelihood, and a 3 means high likelihood.
- **Severity**: A score from 1-3 based on the potential damage the threat could cause to the business. A 1 means low severity impact, a 2 is a moderate severity impact, and a 3 is a high severity impact.
- **Priority**: How quickly a risk should be addressed to avoid the potential incident. Use the formula:  
  **Likelihood x Severity = Risk Score**.

---

## Risk Matrix

| Likelihood ↓ / Severity → | 1 (Low Impact) | 2 (Moderate Impact) | 3 (Catastrophic Impact) |
|---------------------------|----------------|---------------------|-------------------------|
| **3 (Certain)**            | 3              | 6                   | 9                       |
| **2 (Likely)**             | 2              | 4                   | 6                       |
| **1 (Rare)**               | 1              | 2                   | 3                       |

---

*Created by: T B Izadeen - Cybersecurity Portfolio*
