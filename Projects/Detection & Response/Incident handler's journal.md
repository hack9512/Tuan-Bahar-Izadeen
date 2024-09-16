# Incident Handler's Journal

## Scenario 1

### Overview
A small U.S. healthcare clinic specializing in primary-care services experienced a **security incident** on Tuesday morning at approximately 9:00 a.m. Several employees reported being unable to access their computers or essential files like medical records. As a result, business operations were halted.

A **ransom note** appeared on employees’ computers, stating that the company's files had been encrypted by an organized group of unethical hackers known for targeting healthcare and transportation industries. The note demanded a large sum of money in exchange for the decryption key.

The attackers gained access to the network through **phishing emails**, which contained malicious attachments. Once opened, the ransomware was deployed, encrypting critical files and disrupting business operations. The company contacted various organizations for assistance and shut down their computer systems.

---

**Date**: January 16th, 2024  
**Entry**: #1

### Incident Details:
- **Who caused the incident?**: Organized group of hackers.
- **What happened?**: Ransomware attack. Employees were unable to access medical records, and business operations were shut down.
- **When did the incident occur?**: Tuesday Morning, January 16th, 2024.
- **Where did the incident happen?**: A healthcare company.
- **Why did the incident happen?**: The attackers gained access via phishing emails that installed ransomware when downloaded.

### Additional Notes:
1. **Prevention**: The healthcare company could implement more training and awareness programs to prevent phishing emails from being downloaded.
2. **Ransom Payment**: The company should avoid paying the ransom, as it may not guarantee data recovery and could encourage further criminal activities.

---

## Scenario 2

### Overview
On January 22, 2024, at 7:20 p.m. PT, an individual gained unauthorized access to **personal identifiable information (PII)** and **financial information** of approximately 50,000 customers. The estimated financial impact was $100,000 in direct costs and potential loss of revenue.

The incident was first detected on January 20, 2024, when an employee received an email claiming the sender had stolen customer data. The sender demanded $25,000 in cryptocurrency, but the employee ignored it. On January 22, the employee received another email, this time with a sample of the stolen data and an increased demand of $50,000. The security team was then notified.

---

**Date**: January 22nd, 2024  
**Entry**: #1

### Incident Details:
- **Who caused the incident?**: Cybercriminal (malicious actor).
- **What happened?**: An external email threatened to release stolen customer data unless a cryptocurrency payment was made.
- **When did the incident occur?**: January 22, 2024, 7:20 p.m. PT.
- **Where did the incident happen?**: At the organization.
- **Why did the incident happen?**: The attackers gained unauthorized access to customer information and attempted blackmail.

### Recommendations:
- Increase training to raise awareness of potential cyber attacks.
- Conduct investigations using a playbook and ensure security team members report such incidents immediately.

---

**Date**: January 23rd, 2024  
**Entry**: #2

### Incident Details:
- **Who caused the incident?**: Cybercriminal (malicious actor).
- **What happened?**: Attackers used a forced browsing attack by modifying the order number in the URL string to gain access to customer transaction data.
- **When did the incident occur?**: January 23, 2024.
- **Where did the incident happen?**: At the organization.
- **Why did the incident happen?**: The attackers exploited a vulnerability in the e-commerce web application through forced browsing.

### Recommendations:
- Perform routine scans and penetration testing to identify vulnerabilities.
- Implement allowlisting to block unauthorized URLs.
- Increase employee awareness through training and communicate these threats to relevant stakeholders.

---

## Scenario 3

### Overview
As a Level 1 SOC analyst at a financial services company, you received an alert about a suspicious file downloaded on an employee's computer. The employee received an email with a password-protected spreadsheet. After opening the file, a malicious payload was executed.

Using the file's **SHA256 hash**, you investigate the incident using VirusTotal to uncover additional indicators of compromise (IoCs).

---

**Date**: January 17th, 2024  
**Entry**: #1

### Incident Details:
- **Who caused the incident?**: Cybercriminal (malicious actor).
- **What happened?**: The employee opened a malicious file attached to an email, which led to malware execution.
- **When did the incident occur?**: January 17th, 2024, 1:20 p.m.
- **Where did the incident happen?**: Financial Service Company.
- **Why did the incident happen?**: The employee downloaded and executed the malicious file after receiving the email.

### Additional Notes:
- To prevent similar incidents, employees should be educated to avoid downloading suspicious files.
- Should be reported to a Level 2 SOC analyst for further investigation.

---

**Date**: January 18th, 2024  
**Entry**: #2

### Incident Details:
- **Who caused the incident?**: Cybercriminal (malicious actor).
- **What happened?**: The phishing attempt was escalated. The employee opened a malicious email and attachments.
- **When did the incident occur?**: January 17th, 2024, 1:20 p.m.
- **Where did the incident happen?**: Financial Service Company.
- **Why did the incident happen?**: The employee clicked a link from an unknown sender and opened a password-protected file.

### Ticketing Information:
- **Ticket ID**: A-AD3CO
- **Alert Message**: SERVER-MAIL Phishing attempt.
- **Severity**: Medium.
- **Ticket Status**: Escalated.

### Comments:
The alert detected that an employee downloaded and opened a malicious file from a phishing email. The sender's name, “Security IT team”, and the email address raised suspicion due to grammatical errors and a password-protected attachment. The incident was escalated to a Level 2 SOC analyst for further action.

---

### Reflections/Notes:
- **Number of Entries**: Two entries for this scenario.
- **Type of Incident**: Phishing attack.
- **Attack Vector**: Email.
- **Prevention**: More training and awareness to avoid downloading malicious files.

---

*Created by: T B Izadeen - Cybersecurity Portfolio*
