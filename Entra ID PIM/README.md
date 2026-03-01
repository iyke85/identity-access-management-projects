# Privileged Identity Management (PIM) Role Activation – SharePoint Administrator
![ENTRA PIM](https://i.imgur.com/YXc70I5.png)
# Project Overview
In this implementation, I configured Privileged Identity Management (PIM) within Microsoft Entra ID to securely manage administrative access for a SharePoint Administrator role. The objective was to enforce governance controls, reduce standing privileges, and introduce approval-based access for elevated permissions.

# Objective
To ensure privileged access to SharePoint Online is controlled, auditable, and approved through a structured workflow — minimizing security risks associated with permanent administrative assignments.
The showcased metrics offer a holistic perspective on the security stance of the environment, both pre- and post-implementation of security controls. These insights serve as a valuable resource for understanding threat detection, optimizing incident response strategies, and enhancing overall resilience.
# Implementation Details
# 1️⃣ PIM Activation Configuration
- Enabled Privileged Identity Management (PIM) in the Enterprise tenant.
- Selected the SharePoint Administrator Azure AD role.
- Configured the role type as Active assignment.
![Architecture Diagram](https://i.imgur.com/hZhH9S5.png)
![Architecture Diagram](https://i.imgur.com/9vmto5P.png)
# 2️⃣ Approval Workflow Setup
- Configured approval settings requiring manager authorization.
-When the role was activated:
- An automatic email notification was sent to the user’s manager.
- The manager approved the request.
- The role was successfully assigned to the user.
![Architecture Diagram](https://i.imgur.com/E9Xr7qC.png)
![Architecture Diagram](https://i.imgur.com/jXAUc4q.png)
# 3️⃣ Governance & Control Measures
- Enforced approval-based activation.
- Ensured role assignment was auditable via Entra logs.
- Reduced risk of unauthorized privilege escalation.
![Architecture Diagram](https://i.imgur.com/HOjq6jA.png)
# Security & Compliance Impact
- Eliminates uncontrolled administrative access.
- Introduces accountability through manager approval.
- Improves audit readiness and compliance posture.
- Aligns with Zero Trust and least privilege principles.
# Outcome
The successful activation of the SharePoint Administrator role through PIM demonstrates controlled privileged access management within Microsoft Entra ID. By integrating approval workflows and audit logging, the environment now enforces stronger governance and reduces exposure to security risks associated with permanently elevated roles.

  




