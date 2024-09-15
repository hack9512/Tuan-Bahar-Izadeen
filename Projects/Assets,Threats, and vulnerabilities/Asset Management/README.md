# Incident Report: Asset Management and Classification in a Home Office Network


### Objective:
The objective of this activity is to develop a comprehensive understanding of asset management by creating an inventory of assets connected to a home office network. You will classify these assets based on their importance and sensitivity to risk, ensuring effective protection against potential security threats. This process will enhance your ability to identify and prioritize critical assets, contributing to the overall security of the network.
## Scenario

One of the most valuable assets in the world today is information. Most information is
accessed over a network. There tend to be a variety of devices connected to a network
and each is a potential entry point to other assets.
An inventory of network devices can be a useful asset management tool. An
inventory can highlight sensitive assets that require extra protection.
You’re operating a small business from your home and must create an inventory of your
network devices. This will help you determine which ones contain sensitive information
that require extra protection.

## Skills Learned

During this investigation, the following skills were developed and applied:

- **Organization Skills:** The ability to maintain an accurate inventory of all assets, including hardware, software, data, and other resources. Keeping track of asset lifecycle management (acquisition, maintenance, and retirement).
- **Risk Management:** Identifying, assessing, and mitigating risks associated with assets. Prioritizing assets based on their importance and vulnerability to ensure that critical assets receive extra protection.
- **Technical Skills:** Understanding of how assets (both physical and digital) operate within a network.
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

This reading explains how to identify the brute force attack using `tcpdump`.
