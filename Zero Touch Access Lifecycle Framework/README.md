# Zero Trust Access Lifecycle Framework
![Cloud Honeynet / SOC](https://i.imgur.com/EpDGiZG.png)

# Introduction
In this project, I implemented a centralized identity governance framework in Okta focused on secure onboarding, suspension management, and contractor access control. The goal was to standardize access assignment at the point of user creation while introducing tighter controls for temporary access restrictions and third-party users.
Using attribute-based group rules, new users are automatically assigned to appropriate groups during onboarding. When a user is suspended, their status change places them into a dedicated Suspended Users group and sends an automated email notification to the Security team. Contractor accounts are dynamically identified using profile attributes and governed by adaptive policies that enforce stricter authentication and session controls.
# Project Title
Automated Office 365 User Onboarding with Okta Workflows
# Overview
Built an automated identity onboarding solution using Okta Workflows to provision Office 365 access for newly created users. The workflow assigns users to the appropriate Office 365 access group and sends real-time email notifications to IT for visibility and audit tracking.
# Tools & Technologies
- Okta Identity Cloud
- Okta Workflows
- Microsoft Office 365
- Office 365 Mail Connector
- Group-based access provisioning
# Workflow Logic
- Triggered when a user is created in Okta
- Retrieves user profile attributes
- Validates user status to ensure the account is active
- Automatically assigns the user to the Office 365 access group
- Provisions Office 365 applications via group assignment
- Sends an automated email notification confirming access provisioning
![Architecture Diagram](https://i.imgur.com/9lXXVGS.png)
![Architecture Diagram](https://i.imgur.com/Q5xOUz5.png)
![Architecture Diagram](https://i.imgur.com/Z1KjUW3.png)
# Business Impact
- Eliminated manual Office 365 license assignment
- Improved onboarding speed and consistency
- Increased visibility through automated notifications
- Reduced risk of missed or incorrect access assignments
- Strengthened IAM governance and audit readiness
# Key Skills Demonstrated
- Identity lifecycle automation
- Okta Workflows orchestration
- SaaS application provisioning
- Notification and audit workflows
- Secure onboarding design
# Project Title
# Automated User Suspension Handling and Notification with Okta Workflows
![Architecture Diagram](https://i.imgur.com/VUiyeiv.png)
# Overview
Designed and implemented an automated identity governance workflow using Okta Workflows to handle user suspension events. The workflow adds suspended users to a dedicated security group right away and sends an automated email notification, improving visibility, audit readiness, and response time during account lifecycle events.
 # Workflow Logic
- Triggered automatically when a user account is suspended in Okta
- Retrieves the suspended user’s profile details for context and logging
- Adds the user to a predefined Suspended Users group for centralized tracking
- Sends an automated email notification to IT/Security via Office 365
- Logs the workflow execution for audit and troubleshooting purposes
![Architecture Diagram](https://i.imgur.com/1GPgrxV.png)
![Architecture Diagram](https://i.imgur.com/tHC8kaH.png)
![Architecture Diagram](https://i.imgur.com/6aMI1yg.png)
# Business Impact
- Ensured immediate and consistent handling of suspended accounts
- Eliminated manual tracking of suspended users
- Improved security visibility through real-time notifications
- Supported audit and compliance requirements by maintaining group-based records
- Reduced risk of delayed response during security or HR-driven suspensions
# Key Skills Demonstrated
- Identity lifecycle automation
- Security-focused workflow design
- Okta event-based triggers
- Group-based access control
- Automated notification and audit workflows
# Project Title
Contractor Access Control Using Attribute-Based Grouping and Adaptive Policies in Okta
# Overview
Designed and implemented a secure contractor access model in Okta using attribute-based group rules and targeted authentication policies. The solution automatically classifies contractor accounts, enforces stronger password requirements, and applies multi-factor authentication to reduce risk associated with non-employee access.
# Tools & Technologies
- Okta Identity Cloud
- Okta Universal Directory
- Okta Group Rules
- Okta Password Policies
- Okta Enrollment and Authentication Policies
![Architecture Diagram](https://i.imgur.com/ZdRJthd.png)
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

Through structured onboarding automation, suspended user handling, and contractor-specific access controls, this project establishes a clear governance model within Okta. Group-based automation ensures accurate access provisioning, while suspension workflows introduce accountability and immediate restriction when needed.
The use of attribute-based grouping combined with adaptive authentication policies provides stronger protection for contractor accounts, which typically present a higher risk. Overall, the solution reflects a mature approach to identity security that balances automation, oversight, and risk-based access control.
