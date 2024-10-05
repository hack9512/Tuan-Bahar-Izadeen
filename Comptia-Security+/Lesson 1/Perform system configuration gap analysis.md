<h1>Perform system configuration gap analysis</h1>

***What is gap analysis***
> <p>Gap analysis is the act of comparing the current configuration of a system with a template, configuration file, baseline, security framework, or settings documentation. This is an essential operation to discover the differences between the intended or expected configuration of a system and its actual operating configuration. In this exercise, you will perform a gap analysis.</p>

<h3>Scenario</h3>

<p>As a security team member of Structureality Inc, you are working to improve your organization's security stance. Often the best path to a secure IT infrastructure starts with thorough planning and analysis. You will perform a gap analysis of the current configuration of a system against a security template.

In this lab, you will use security templates to manage a Windows Server configuration, which will entail using the Microsoft Policy Analyzer to perform a security baseline template review and gap analysis.</p>

<h2>Objectives</h2>

> - 1.2 Summarize fundamental security concepts.
> - 3.2 Given a scenario, apply security principles to secure enterprise infrastructure
> - 4.1 Given a scenario, apply common security techniques to computing resources.
> - 4.4 Explain security alerting and monitoring concepts and tools.
> - 5.1 Summarize elements of effective security governance.

<h2>Steps</h2>

Determine the build for the Windows Server 2019 running in the PC. **Type here to search** from taskbar, type **winver**.
![Screenshot 2024-10-05 at 12 25 10](https://github.com/user-attachments/assets/2602fd55-96ae-4bb3-8a48-c8279d826641)
> - Version Number = 1809
> - OS Build Number = 17763.4377

If you perform these operations against other systems, you will need to match the version and build numbers to the baseline template files.

Select **Type here to search** from the taskbar, type **powershell**, right-click **Windows PowerShell** from the results, then select **Run as administrator**.
![Screenshot 2024-10-05 at 12 31 43](https://github.com/user-attachments/assets/f4de7244-6923-4cb9-82e0-f063f4761158)

Type in Command copy D:\* c:\LABFILES
> - This command copies PolicyAnalyzer.zip and Windows 10 Version 1809 and Windows Server 2019 Security Baseline.zip from the read-only removable media virtual optical disc (i.e., D:) to C:\LABFILES.
> - These two files are from the Microsoft Security Compliance Toolkit. The baseline file was selected based on the OS version and build number.
> - The Microsoft Security Compliance Toolkit includes the Policy Analyzer tool as well as numerous security configuration template files. Searching for "Microsoft Security Compliance Toolkit" will help you locate the download area on the Microsoft website where these items are hosted. They have been provided for you the Student-Resources-L01.ISO media.

Type in command **cd c:\LABFILES** to change into the directory.
Enter **ls** to view the contents of the directory.
> - You should see PolicyAnalyzer.zip and Windows 10 Version 1809 and Windows Server 2019 Security Baseline.zip in the list of files.
![Screenshot 2024-10-05 at 12 46 02](https://github.com/user-attachments/assets/24a24987-50e7-4771-a922-bf41f5799d40)

Enter the following commands to extract the contents of the zip files into their own sub-directories:
> - Expand-Archive -Path PolicyAnalyzer.zip
> - Expand-Archive -Path "Windows 10 Version 1809 and Windows Server 2019 Security Baseline.zip"

Enter the following command to open the Policy Analyzer application:
> - C:\LABFILES\PolicyAnalyzer\PolicyAnalyzer_40\PolicyAnalyzer.exe

![Screenshot 2024-10-05 at 12 53 24](https://github.com/user-attachments/assets/a9735c94-d9fa-47ab-aa05-deb9e96989a0)

<p>The Policy Analyzer window should now be displayed. If needed, minimize the PowerShell window.<p/>
<p>Maximize the Policy Analyzer window</p>
<p>At the bottom of the Policy Analyzer window, select the **Policy Rule sets in** field.</p>
<p>On the Pick the folder containing the Policy Analyzer Policy Rules files window</p>
<p>Perform a View/Compare of **MSFT-Win10-v1809-RS5-WS2019-FINAL** using Policy Analyzer by marking the **MSFT-Win10-v1809-RS5-WS2019-FINAL** checkbox, then selecting View / Compare.</p>

![Screenshot 2024-10-05 at 13 02 38](https://github.com/user-attachments/assets/e7d928bf-fde5-41b8-9518-a8ed6394fe37)

Scroll to the bottom of the list and locate the **LockoutBadCount** and **MinimumPasswordLength**.
![Screenshot 2024-10-05 at 13 08 54](https://github.com/user-attachments/assets/4fb631ba-99e7-4934-bcab-363daa3bdac3)
> - Notice the baseline value from the security templates for the policy settings of LockoutBadCount is 10

![Screenshot 2024-10-05 at 13 13 21](https://github.com/user-attachments/assets/343e9621-ee64-4d2c-86c4-131675a10ae4)
> - Notice the baseline value from the security templates for the policy settings of MinimumPasswordLength is 14

Close the Policy Viewer window

Now lets **Click Button** **Compare to Effective State**

When using a tool like Policy Viewer, the “Compare the Effective State” feature enables you to:
> - Compare Actual Policy vs. Baseline: You can compare the currently applied (effective) policy settings on a system with a predefined security baseline (e.g., Windows security baseline or CIS benchmark). This helps in identifying misconfigurations or deviations from best practices.
> - Detect Policy Gaps: Any differences between the current effective policy and the desired configuration will be highlighted. For example, you may find that a specific security setting is weaker than recommended (e.g., password length is shorter than recommended).
> - Audit and Compliance: The comparison helps in auditing the system to ensure that security policies meet compliance standards and organizational policies.

<p>Perform a Compare to Effective State of **MSFT-Win10-v1809-RS5-WS2019-FINAL** using Policy Analyzer by marking the **MSFT-Win10-v1809-RS5-WS2019-FINAL** checkbox, then selecting **Compare to Effective State**.</p>

![Screen Recording 2024-10-05 at 20 01 08](https://github.com/user-attachments/assets/e1b03cd3-a0b9-4aa0-bf80-e9bb38a920df)

This information appears to be a detailed explanation of the **Account Lockout Policy**, particularly focusing on the **Account Lockout Threshold** setting in Group Policy, which is a part of the **Security Settings** under **Account Policies**.

### Breakdown:

#### 1. **Policy Path:**
The policy path points to where this specific setting can be found within the **Group Policy Editor**:
- **Security Settings**: This is a section within Group Policy settings where various security configurations are managed.
- **Account Policies**: This subsection deals with policies that affect user accounts, such as password and lockout settings.
- **Account Lockout Policy**: This policy handles the rules for locking out accounts after multiple failed login attempts.
- **Account Lockout Threshold**: The specific setting that determines how many failed login attempts will trigger an account lockout.

#### 2. **Account Lockout Threshold:**
This section explains what this setting does:

- **Purpose**:  
  The **Account Lockout Threshold** specifies the number of failed login attempts that will cause a user account to be locked out. If a user exceeds this number, the account is locked, either requiring intervention from an administrator or waiting for the lockout duration to expire before the account is unlocked.

- **Value Range**:  
  You can set a value between **0 and 999**. A value of **0** means that the account will **never be locked out** regardless of how many failed login attempts occur.

- **Use Case**:  
  This is important in environments where brute-force attacks could be attempted. The threshold helps in preventing attackers from continuously trying to guess a user's password.

- **Special Cases**:  
  Failed login attempts against workstations or member servers that have been locked (e.g., with `CTRL + ALT + DELETE` or password-protected screensavers) **still count** as failed logon attempts, and can contribute to locking out the account.

- **Default Value**:  
  The default value for this setting is **0**, meaning accounts will never be locked out by default unless an administrator changes the setting.

#### 3. **Baseline(s):**
- **Option**: **10**  
  The security baseline suggests setting the account lockout threshold to **10** failed attempts before the account is locked out.
- **GPO (Group Policy Object)**:  
  The specific baseline or security recommendation is part of **MSFT Windows 10 1809 and Server 2019 - Domain Security**. This means the baseline is applicable to **Windows 10 Version 1809** and **Windows Server 2019** and reflects Microsoft’s security recommendations for domain environments.

#### 4. **Effective State:**
This section compares the actual settings applied on the machine (effective state) to the baseline:

- **Option**: **10**  
  This indicates that the **effective setting** on the system is set to 10 failed attempts before locking the account, which is in line with the baseline recommendation.
- **GPO**: **PC10 - secedit**  
  This indicates that the setting is being applied from a specific Group Policy Object named **PC10**, and the tool used to configure or audit this setting is likely **secedit** (a command-line tool used for security configuration).

### Summary:
- The **Account Lockout Threshold** is set to **10** failed login attempts before an account is locked out, which matches the recommended baseline for Windows 10 (Version 1809) and Windows Server 2019.
- This policy ensures that after 10 incorrect password attempts, a user’s account is temporarily locked, enhancing security against brute-force attacks.
- The configuration is enforced via a **GPO** on the domain, and this is validated by tools like **secedit**. The baseline being followed is from Microsoft's security recommendations for domain environments.


<h3>Tools</h3>

> - <p>Microsoft Policy Analyzer</p>
> - <p>Powershell</p>
> - <p>ChatGPT</p>

<h3>Skills enriched</h3>
During a **gap analysis**, you typically develop and enhance the following skills:

### 1. **Analytical Thinking**:
   - The ability to assess the current state versus the desired state.
   - Identifying gaps between existing processes and the required outcomes.

### 2. **Problem-Solving**:
   - Determining the root causes of gaps and creating solutions to address them.
   - Prioritizing issues based on their impact and feasibility of resolution.

### 3. **Attention to Detail**:
   - Carefully examining policies, processes, and configurations to find deviations from baselines.
   - Ensuring no crucial settings or practices are overlooked.

### 4. **Research and Benchmarking**:
   - Familiarizing yourself with industry standards, frameworks, and baselines (e.g., CIS benchmarks, Microsoft security baselines).
   - Comparing current policies and procedures with best practices.

### 5. **Technical Knowledge**:
   - Understanding system configurations, such as Group Policy settings, security policies, and system baselines (for example, in Windows environments).
   - Gaining familiarity with tools used in gap analysis, like Policy Analyzer, Microsoft Compliance Toolkit, and PowerShell.

### 6. **Documentation and Reporting**:
   - Documenting the findings from the gap analysis in a clear, structured format.
   - Reporting gaps to stakeholders and explaining the risks and impact.

### 7. **Communication**:
   - Explaining technical gaps to non-technical stakeholders and suggesting solutions in an understandable way.
   - Coordinating with different teams (security, compliance, IT) to implement improvements.

### 8. **Project Management**:
   - Developing action plans to close identified gaps.
   - Monitoring the progress and ensuring that remediation efforts are completed within set timelines.

