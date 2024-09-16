# Data Leak Worksheet

## Scenario
You work for an educational technology company that developed an application to help teachers automatically grade assignments. The application handles a wide range of data collected from academic institutions, instructors, parents, and students. Recently, your team was alerted to a data leak of internal business plans on social media. An investigation revealed that an employee accidentally shared those confidential documents with a customer. An audit is underway to determine how similar incidents can be avoided.

The principle of least privilege was not observed by employees at the company during a sales meeting. You have been asked to analyze the situation and find ways to prevent it from happening again.

### Incident Summary
A sales manager shared access to a folder of internal-only documents with their team during a meeting. The folder contained files associated with a new product that had not been publicly announced. It also included customer analytics and promotional materials. After the meeting, the manager did not revoke access to the internal folder but warned the team to wait for approval before sharing the promotional materials with others.

During a video call with a business partner, a member of the sales team forgot the manager’s warning and accidentally shared a link to the internal folder instead of the promotional materials. The business partner posted the link on their company's social media page, assuming it contained promotional content.

---

## Control: Least Privilege

### Issue(s)
**What factors contributed to the information leak?**

- Access to the internal folder was shared with the entire sales team, violating the principle of least privilege.
- The business partner was not authorized to receive confidential information, and the manager did not revoke access after the meeting.

### Review
**What does NIST SP 800-53: AC-6 address?**

NIST SP 800-53: AC-6 focuses on how organizations can protect their data privacy by implementing least privilege. It offers control enhancements to improve the effectiveness of this principle. According to the least privilege guideline, a user or entity should only have access to the specific data, resources, and applications required to complete a task.

### Recommendation(s)
**How might the principle of least privilege be improved at the company?**

- Restrict access to sensitive resources based on the user role (Role-Based Access Control).
- Regularly audit user privileges to ensure unnecessary access is revoked.

### Justification
**How might these improvements address the issues?**

- Restricting access to internal files exclusively to relevant employees reduces exposure to unauthorized users.
- Requiring managers and security teams to regularly audit access would prevent the prolonged exposure of sensitive information, thus reducing the risk of accidental leaks.

---

## Security Plan Snapshot

### NIST Cybersecurity Framework (CSF)
The NIST Cybersecurity Framework uses a hierarchical, tree-like structure to organize information. It defines security functions, which then branch into categories, subcategories, and individual security controls.

| Function   | Category                | Subcategory                        | Reference(s)                       |
|------------|-------------------------|------------------------------------|------------------------------------|
| **Protect**| PR.DS: Data Security     | PR.DS-5: Protections against data leaks | NIST SP 800-53: AC-6              |

In this example, the implemented controls used to protect against data leaks are defined in NIST SP 800-53, a set of guidelines for securing information privacy systems.

---

## NIST SP 800-53: AC-6 - Least Privilege

### Control
Only the minimal access and authorization required to complete a task or function should be provided to users.

### Discussion
Processes, user accounts, and roles should be enforced as necessary to achieve least privilege. The goal is to prevent users from operating at privilege levels higher than necessary for accomplishing business objectives.

### Control Enhancements
- Restrict access to sensitive resources based on user role.
- Automatically revoke access after a set period.
- Keep activity logs for provisioned user accounts.
- Regularly audit user privileges.

---

*Created by: T B Izadeen - Cybersecurity Portfolio*
