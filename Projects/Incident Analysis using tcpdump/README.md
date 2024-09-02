# Incident Report: Website Compromise and Malware Distribution

## Objective

The objective of this analysis is to investigate and document the security breach on yummyrecipesforme.com, identify the network protocols involved in the attack, and recommend measures to prevent future incidents, particularly focusing on preventing brute force attacks.

## Scenario

You are a cybersecurity analyst for yummyrecipesforme.com, a website that sells recipes and cookbooks. A former employee has decided to lure users to a fake website with malware.

The baker executed a brute force attack to gain access to the web host. They repeatedly entered several known default passwords for the administrative account until they correctly guessed the right one. After they obtained the login credentials, they were able to access the admin panel and change the website’s source code. They embedded a JavaScript function in the source code that prompted visitors to download and run a file upon visiting the website. After embedding the malware, the baker changed the password to the administrative account. When customers download the file, they are redirected to a fake version of the website that contains the malware.

Several hours after the attack, multiple customers emailed yummyrecipesforme’s helpdesk. They complained that the company’s website had prompted them to download a file to access free recipes. The customers claimed that, after running the file, the address of the website changed and their personal computers began running more slowly.

In response to this incident, the website owner tried to log in to the admin panel but was unable to, so they reached out to the website hosting provider. You and other cybersecurity analysts are tasked with investigating this security event.

## Skills Learned

During this investigation, the following skills were developed and applied:

- **Network Traffic Analysis:** Gained expertise in analyzing network traffic logs to detect malicious activities, such as unauthorized access and data exfiltration.
- **Brute Force Attack Detection:** Learned to identify signs of brute force attacks and understand how weak passwords can be exploited.
- **Malware Analysis:** Developed skills in analyzing and understanding how malware is delivered and executed through compromised websites.
- **Incident Documentation:** Improved the ability to document security incidents comprehensively, detailing each step of the attack and the investigation.

## Tools Used

The following tools were used during the investigation:

- **`tcpdump`:** A powerful command-line packet analyzer tool used to capture and analyze network traffic.
- **Sandbox Environment:** An isolated environment created to safely observe and interact with the suspicious website without risking the integrity of the primary network.

## Steps Taken in the TCP Investigation

### Step 1: Setup and Preparation
- **Create a Sandbox Environment:** Set up a secure, isolated environment to safely analyze the suspicious website behavior without exposing the main network to potential risks.
  
### Step 2: Capture Network Traffic
- **Run `tcpdump`:** Launched `tcpdump` to capture all incoming and outgoing network traffic while interacting with the suspicious website.

### Step 3: Simulate User Interaction
- **Visit the Website:** Accessed `yummyrecipesforme.com` in the sandbox environment to replicate the user experience and observe any malicious activity.
- **Download the File:** Allowed the website to prompt for a file download, as reported by the users, to capture the associated network traffic.

### Step 4: Analyze Captured Traffic
- **Inspect DNS Requests:** Analyzed the DNS requests and responses to verify the legitimacy of the IP addresses and detect any redirections.
- **Examine HTTP Requests:** Scrutinized HTTP requests to understand the nature of the communication between the browser and the server, including the delivery of the malware.
- **Identify Redirection:** Observed the redirection from `yummyrecipesforme.com` to `greatrecipesforme.com`, confirming the compromise.

### Step 5: Document Findings
- **Record the Process:** Documented each step of the investigation, including the tools used, the traffic captured, and the anomalies detected.
- **Generate a Report:** Compiled a comprehensive report detailing the incident, the investigation process, and the recommended preventive measures.

## Recommendations

### Strengthening Security Against Brute Force Attacks

1. **Implement Strong Password Policies:** Enforce complex password requirements and mandatory password changes from default settings.
2. **Enable Account Lockout Mechanisms:** Introduce account lockout features after a set number of failed login attempts to prevent brute force attacks.
3. **Use Multi-Factor Authentication (MFA):** Require MFA for administrative accounts to add an additional layer of security.
4. **Regularly Monitor and Audit Access Logs:** Continuously monitor access logs for unusual login attempts and implement alerting systems for suspicious activity.

---

## How to Read the `tcpdump` Traffic Log
<a href="https://opensource.com/article/18/10/introduction-tcpdump">This reading explains how to identify the brute force attack using `tcpdump`.</a>
