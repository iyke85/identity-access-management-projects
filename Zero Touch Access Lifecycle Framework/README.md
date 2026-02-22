# Zero Touch Access Lifecycle Framework
![Cloud Honeynet / SOC](https://i.imgur.com/EpDGiZG.png)

# Introduction

This project demonstrates end-to-end identity lifecycle automation across both Okta and Microsoft Entra environments. By configuring Joiner, Mover, and Leaver workflows in Entra and setting up attribute-based access controls and policy enforcement in Okta, the solution provides a coordinated, secure, and automated way to handle user provisioning, access transitions, and offboarding.
# Project Title
Automated Office 365 User Onboarding with Okta Workflows
# Project Overview
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
# Project Overview
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
# Project Overview
Designed and implemented a secure contractor access model in Okta using attribute-based group rules and targeted authentication policies. The solution automatically classifies contractor accounts, enforces stronger password requirements, and applies multi-factor authentication to reduce risk associated with non-employee access.
![Architecture Diagram](https://i.imgur.com/ZdRJthd.png)


In the "BEFORE" metrics analysis, all resources were initially deployed and left exposed to the internet. The Virtual Machines had both their Network Security Groups and built-in firewalls configured with open access, while all other resources were deployed with public endpoints accessible from the Internet, rendering private endpoints unnecessary.

In the "AFTER" metrics assessment, Network Security Groups underwent fortification by enforcing a stringent policy, blocking ALL traffic except for connections originating from my designated admin workstation. Furthermore, additional protection was afforded to all other resources through the reinforcement of their built-in firewalls, supplemented by the implementation of Private Endpoints.


## Attack Maps Before Hardening / Security Controls
![NSG Allowed Inbound Malicious Flows](https://i.imgur.com/oH4Xej5.png)<br>
![Linux Syslog Auth Failures](https://i.imgur.com/c2KbH2A.png)<br>
![Windows RDP/SMB Auth Failures](https://i.imgur.com/esMgryr.png)<br>

## Metrics Before Hardening / Security Controls

The following table shows the metrics we measured in our insecure environment for 24 hours:
Start Time 2024-01-27T02:37:14.7683908Z
Stop Time 2023-03-11T21:03:08.1360519Z

| Metric                   | Count
| ------------------------ | -----
| SecurityEvent            | 18380
| Syslog                   | 13314
| SecurityAlert            | 6
| SecurityIncident         | 334
| AzureNetworkAnalytics_CL | 58501

## Attack Maps Before Hardening / Security Controls

```All map queries returned no results due to no instances of malicious activity for the 24 hours after hardening.```

## Metrics After Hardening / Security Controls

The following table shows the metrics we measured in our environment for another 24 hours, but after I applied security controls:
Start Time 2024-02-07T02:31:10.4920242Z
Stop Time	2024-02-08T02:31:10.4920242Z

| Metric                   | Count
| ------------------------ | -----
| SecurityEvent            | 9590
| Syslog                   | 0
| SecurityAlert            | 1
| SecurityIncident         | 0
| AzureNetworkAnalytics_CL | 0

## Conclusion

In this Azure-based project, a mini honeynet was meticulously crafted, with log sources seamlessly integrated into a Log Analytics workspace. Leveraging Microsoft Sentinel, the system adeptly triggered alerts and swiftly addressed incidents based on the processed logs.

A pivotal aspect of the project involved meticulously measuring metrics within the insecure environment before the implementation of security controls. After the fortification measures, a follow-up evaluation of metrics was conducted, showcasing a remarkable reduction in security events and incidents. This significant decrease underscores the efficacy of the implemented security measures.

Furthermore, it's pertinent to acknowledge that in environments where resources are extensively utilized by regular users, there could be a higher frequency of security events and alerts in the 24 hours following the implementation of security controls.
