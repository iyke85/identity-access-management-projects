
# Introduction
Effective identity lifecycle management is critical to maintaining both operational efficiency and security. This project demonstrates how Microsoft Entra Lifecycle Workflows can automate onboarding, internal role transitions, and offboarding, reducing manual effort, strengthening access governance, and minimizing risk.
# Automated New Hire Onboarding Using Microsoft Entra Lifecycle Workflows
# Overview
Built an automated new hire onboarding workflow in Microsoft Entra ID using Lifecycle Workflows. The solution provisions user accounts, assigns group-based access, and automatically sends onboarding communications, ensuring consistent and secure Day 1 access for new employees.
# Platform & Technologies
- Microsoft Entra ID
- Identity Governance (Lifecycle Workflows)
- Microsoft 365
- Group-based access control (RBAC)
# Workflow Trigger
The workflow is triggered when a new employee account meets the defined onboarding criteria (for example: account created or hire date reached).
![Architecture Diagram](https://i.imgur.com/dGg3hQE.png)
![Architecture Diagram](https://i.imgur.com/rt90U6X.png)
# Tasks Configured
## 1. Enable User Account
- Automatically activates the user account at the appropriate onboarding stage, ensuring access is granted only when the employee officially begins.
## Impact:
- Prevents premature access while guaranteeing Day 1 readiness.
## 2. Add User to Groups
- Adds the new hire to predefined security and Microsoft 365 groups.
## Impact:
- Grants access to required applications
- Ensures role-based access consistency
- Eliminates manual group assignment errors
## 3. Send Welcome Email
- Automatically sends a welcome message with onboarding instructions and login guidance.
## Impact:
- Improves user experience
- Reduces helpdesk tickets
- Standardizes onboarding communication
![Architecture Diagram](https://i.imgur.com/ezNZ3tb.png)
![Architecture Diagram](https://i.imgur.com/eA9Sctd.png)
![Architecture Diagram](https://i.imgur.com/KnXHIr1.png)
![Architecture Diagram](https://i.imgur.com/NpKiCw7.png)
# Business Value
- Reduced manual onboarding effort
- Accelerated employee productivity
- Improved security through consistent access enforcement
- Increased audit visibility for identity lifecycle events
- Standardized onboarding process across the organization
# Key Skills Demonstrated
- Identity lifecycle automation
- Microsoft Entra Lifecycle Workflows configuration
- Group-based access provisioning
- Access governance principles
- Secure onboarding process design
# Project Title
## Automated Role Change (Mover) Workflow Using Microsoft Entra Lifecycle Workflows
![Architecture Diagram](https://i.imgur.com/6Pmq2Qr.png)
# Overview
Configured an automated role change (Mover) workflow in Microsoft Entra Lifecycle Workflows to manage access transitions when employees change departments or roles. The workflow removes outdated access, assigns new role-based group memberships, and notifies the user’s manager to maintain visibility and governance during access changes.
# Tasks Configured
## 1. Remove User from Selected Groups
- Automatically removes the user from previous role-based or department-specific groups.
## Impact:
- Prevents privilege accumulation
- Reduces risk of excessive access
- Supports the least-privilege security model
## 2. Add User to New Groups
- Assigns the user to new groups aligned with their updated role or department.
## Impact:
- Ensures correct application and resource access
- Maintains consistency across identity governance policies
- Eliminates manual reassignment errors
## 3. Send Email Notification to Manager
- Automatically sends a notification to the user’s manager informing them of the access changes.
## Impact:
- Provides transparency
- Supports accountability and oversight
- Improves communication between IT and leadership
![Architecture Diagram](https://i.imgur.com/UHljufl.png)
![Architecture Diagram](https://i.imgur.com/RYJm2oR.png)
![Architecture Diagram](https://i.imgur.com/29GYRep.png)
![Architecture Diagram](https://i.imgur.com/ggbcW0u.png)
![Architecture Diagram](https://i.imgur.com/4mGNkHF.png)
# Business Value
- Reduced manual access modification workload
- Strengthened governance during internal role transitions
- Prevented access sprawl and privilege creep
-  Improved audit visibility of role-based access changes
- Enhanced security posture through automated enforcement
# Key Skills Demonstrated
- Identity lifecycle automation
- Access recertification principles
- Role-based access management
- Microsoft Entra Identity Governance
- Secure workflow configuration
# Project Title
## Automated Offboarding (Leaver) Workflow Using Microsoft Entra Lifecycle Workflows
# Overview
Built an automated offboarding workflow in Microsoft Entra Lifecycle Workflows to securely manage user departures. The solution removes group memberships, revokes Microsoft Teams access, and notifies managers before the employee’s final working day to ensure a controlled and auditable exit process.
![Architecture Diagram](https://i.imgur.com/mygpmJ3.png)
# Workflow Trigger
The workflow is triggered based on the user’s termination date or last working day attribute, ensuring offboarding actions occur at the correct time without manual intervention.
![Architecture Diagram](https://i.imgur.com/6Pmq2Qr.png)
# Implementation Details
- Attribute-Based Group Assignment
- Created a Contractor group in Okta
- Implemented a group rule that automatically adds users to the Contractor group when the department attribute equals contractor
- Ensured dynamic, scalable group membership without manual intervention
# Contractor Password Policy
- Created a dedicated password policy for contractors
- Enforced a minimum 12-character password length
- Applied stricter password standards to contractor accounts to reduce credential-based risk
# Authentication and Enrollment Policy
- Configured a contractor-specific enrollment and authentication policy
- Required authentication using:
- Password
- Okta Verify as an additional factor
- Restricted authentication methods to prevent weaker or unsupported MFA options
![Architecture Diagram](https://i.imgur.com/vjlLu7k.png)
![Architecture Diagram](https://i.imgur.com/nQ5AQGJ.png)
![Architecture Diagram](https://i.imgur.com/OZ5x3up.png)
![Architecture Diagram](https://i.imgur.com/bFFgxzi.png)
![Architecture Diagram](https://i.imgur.com/ysOeVNx.png)
![Architecture Diagram](https://i.imgur.com/l4HN8oB.png)
![Architecture Diagram](https://i.imgur.com/VVlqyo0.png)
# Workflow Logic Summary
- User account is created or updated
- Okta evaluates the user’s department attribute
- Users with a department set to contractor are automatically added to the Contractor group
- Contractor-specific password and authentication policies are applied
- Access and authentication behavior are enforced consistently across contractor accounts
# Business Impact
- Automated contractor classification and policy enforcement
- Reduced manual effort in managing non-employee access
- Improved security posture for third-party and temporary users
- Ensured consistent application of stronger authentication controls
- Supported least-privilege and zero-trust identity principles
# Key Skills Demonstrated
- Attribute-based access control (ABAC)
- Identity lifecycle management
- Secure authentication policy design
- MFA enforcement and factor restrictions
- Okta group rule configuration

## Conclusion
This project demonstrates a structured and automated approach to identity lifecycle management using Microsoft Entra Lifecycle Workflows. By enforcing consistent onboarding, role transitions, and offboarding controls, the solution strengthens security, reduces manual errors, and ensures timely access governance across the organization.
