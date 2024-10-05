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
<h3>Tools</h3>

> - <p>Microsoft Policy Analyzer</p>
> - <p>Powershell</p>
