# Microsoft 365 Business Premium Homelab

## Overview
Complete hands-on Microsoft 365 Business Premium 
homelab built on a trial tenant covering all major 
M365 administration areas from user management to 
Conditional Access, Intune, Defender and Purview.

## Tenant Details
- Plan: Microsoft 365 Business Premium
- Tenant: praveenlab2026.onmicrosoft.com
- Users: 10+ test users across IT, Finance, HR, 
  Sales, Marketing departments

## What I Built and Configured

### Identity and Access Management
- Created and managed users, security groups, 
  M365 groups, distribution lists and dynamic groups
- Configured Dynamic Groups with auto-membership 
  rules using Entra ID P1
- Assigned admin roles following principle of 
  least privilege
- Configured Multi-Factor Authentication using 
  Microsoft Authenticator app
- Enabled and tested Self-Service Password Reset

### Conditional Access - Zero Trust
- Disabled Security Defaults and implemented 
  Conditional Access policies
- CA001: Require MFA for all users
- CA002: Block sign-ins from outside Italy
- CA003: Require MFA for all admin roles
- CA004: Block legacy authentication protocols
- Created emergency admin account to prevent lockout

### Exchange Online
- Managed user mailboxes and permissions
- Created shared mailbox with Full Access and 
  Send As permissions
- Configured mail flow rules including legal 
  disclaimer on all outbound email
- Set up room mailbox with auto-accept booking
- Configured anti-spam and anti-phishing policies

### Microsoft Teams
- Created Teams with standard and private channels
- Configured meeting policies and messaging policies
- Configured external access and guest access

### SharePoint Online and OneDrive
- Created team sites with custom permissions
- Configured document libraries and external 
  sharing settings
- Managed OneDrive admin access

### Security - Microsoft Defender for Business
- Configured Safe Attachments with sandbox analysis
- Configured Safe Links with time-of-click protection
- Hardened anti-phishing with impersonation protection
- Onboarded Windows device to Defender for Business

### Compliance - Microsoft Purview
- Created 7-year email retention policy
- Created DLP policy to protect EU financial data
- Created and published Confidential sensitivity label
- Investigated audit logs and sign-in logs

### Microsoft Intune
- Created Windows compliance policy requiring 
  BitLocker, PIN, antivirus and firewall
- Created Windows configuration profile for 
  Defender and update settings
- Created iOS app protection policy for Outlook

### PowerShell Automation
- Connected to Microsoft Graph, Exchange Online, 
  Teams and SharePoint via PowerShell
- Created users, assigned licenses and managed 
  groups via Microsoft Graph
- Managed Exchange Online mailboxes and permissions
- Bulk created 3 users from CSV with automatic 
  license assignment

### Monitoring and Reporting
- Reviewed M365 usage reports across all services
- Investigated audit logs and sign-in logs
- Configured security alert policies
- Improved Microsoft Secure Score by implementing 
  security best practices

## Skills Demonstrated
Microsoft 365 Administration - Exchange Online 
Microsoft Teams - SharePoint Online - OneDrive 
Microsoft Intune - Microsoft Entra ID - MFA - SSPR 
Conditional Access - Microsoft Defender for Business 
Microsoft Purview - DLP - Sensitivity Labels 
PowerShell - Microsoft Graph API - Zero Trust Security

## Certifications
- Microsoft Certified: Azure Fundamentals (AZ-900)
- Microsoft Certified: Security, Compliance and 
  Identity Fundamentals (SC-900)
- AWS Certified Cloud Practitioner

## Related Projects
- Active Directory Enterprise Homelab: 
  github.com/Orange3456/active-directory-homelab

## Author
Praveenkumar Saminathan
MSc Graduate - Geoinformatics Engineering
Politecnico di Milano - July 2026
Milan, Italy
praveennathan10@gmail.com
linkedin.com/in/praveenkumar-saminathan-993902228
