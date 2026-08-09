# Microsoft 365 Business Premium Homelab

![Microsoft 365](https://img.shields.io/badge/Microsoft%20365-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Entra ID](https://img.shields.io/badge/Microsoft%20Entra%20ID-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Intune](https://img.shields.io/badge/Microsoft%20Intune-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Defender](https://img.shields.io/badge/Microsoft%20Defender-00B294?style=for-the-badge&logo=microsoftazure&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white)
![Purview](https://img.shields.io/badge/Microsoft%20Purview-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)

A comprehensive Microsoft 365 Business Premium homelab built entirely hands-on on a trial tenant. Every user, every policy, every security configuration - done from scratch across 16 chapters covering M365 Administration, Identity and Access Management, Device Management, Email Security, Compliance and PowerShell automation.

---

## Table of Contents

- [Tenant Details](#tenant-details)
- [What Was Built](#what-was-built)
- [Screenshots](#screenshots)
  - [A - Users](#a---users)
  - [B - Groups](#b---groups)
  - [C - Licensing](#c---licensing)
  - [D - Exchange Online](#d---exchange-online)
  - [E - Microsoft Teams](#e---microsoft-teams)
  - [F - SharePoint and OneDrive](#f---sharepoint-and-onedrive)
  - [G - Microsoft Entra ID](#g---microsoft-entra-id)
  - [H - Conditional Access](#h---conditional-access)
  - [I - SSPR](#i---sspr)
  - [J - Microsoft Defender](#j---microsoft-defender)
  - [K - Microsoft Purview](#k---microsoft-purview)
  - [L - Microsoft Intune](#l---microsoft-intune)
  - [M - PowerShell](#m---powershell)
  - [N - Monitoring and Reports](#n---monitoring-and-reports)
- [Skills Demonstrated](#skills-demonstrated)
- [Tools and Technologies](#tools-and-technologies)
- [Repository Structure](#repository-structure)
- [About](#about)

---

## Tenant Details

| Component | Details |
|-----------|---------|
| Plan | Microsoft 365 Business Premium |
| Tenant | praveenlab2026.onmicrosoft.com |
| Users | 10+ test users across IT, Finance, HR, Sales, Marketing |
| Admin Account | PRAVEENKUMARSAMINATHAN@praveenlab2026.onmicrosoft.com |
| Entra ID | P1 - included in Business Premium |
| Intune | Included in Business Premium |
| Defender | Defender for Business + Defender for Office 365 P1 |
| Purview | Basic compliance features included |
| Hardware | Dell Latitude i5, 16GB RAM |

---

## What Was Built

### User and Group Management
- Created and managed 10+ users across multiple departments
- Full Joiner-Mover-Leaver (JML) lifecycle implemented hands-on
- Created Microsoft 365 Groups, Security Groups, Distribution Lists and Dynamic Groups
- Dynamic Groups with auto-membership rules using Entra ID P1
- Assigned admin roles following principle of least privilege
- Bulk user creation from CSV via PowerShell Microsoft Graph
- Guest user invitation and management

### Identity and Access Management
- Configured Multi-Factor Authentication using Microsoft Authenticator app
- Disabled Security Defaults and implemented Conditional Access policies
- CA001: Require MFA for all users
- CA002: Block sign-ins from outside Italy with Named Locations
- CA003: Require MFA for all admin roles
- CA004: Block legacy authentication protocols
- Created emergency admin account to prevent tenant lockout
- Enabled and tested Self-Service Password Reset (SSPR)
- Configured Temporary Access Pass for emergency MFA recovery

### Exchange Online
- Managed user mailboxes and permissions
- Created shared mailbox (IT Help Desk) with Full Access and Send As permissions
- Configured mail flow rule appending legal disclaimer to all outbound email
- Set up room mailbox with auto-accept booking for Milan Conference Room
- Configured anti-spam, anti-malware and anti-phishing policies
- Set email forwarding and out-of-office replies via PowerShell

### Microsoft Teams
- Created Teams with standard and private channels
- Configured custom meeting policy restricting cloud recording and screen sharing
- Configured messaging policy for professional environment
- Configured external access (federation) and guest access settings

### SharePoint Online and OneDrive
- Created team site with custom permission levels (Owner, Member, Visitor)
- Created document libraries and folder structure
- Configured external sharing settings
- Accessed user OneDrive as admin for data governance

### Security - Microsoft Defender for Business
- Configured Safe Attachments with sandbox analysis blocking zero-day malware
- Configured Safe Links with time-of-click URL protection
- Hardened anti-phishing with impersonation protection for admin accounts
- Onboarded Windows device to Defender for Business via local script
- Configured security role assignments (Security Reader, Security Administrator)
- Configured email notifications for incidents and vulnerabilities

### Compliance - Microsoft Purview
- Created 7-year email retention policy for Exchange mailboxes
- Created DLP policy protecting EU financial data across all M365 locations
- Created and published Confidential sensitivity label with encryption
- Investigated audit logs and sign-in logs for security scenarios
- Configured compliance alert policies

### Microsoft Intune - Device Management
- Created Windows compliance policy requiring BitLocker, PIN, antivirus and firewall
- Created Windows configuration profile for Defender and update settings
- Created iOS app protection policy for Outlook (MAM)
- Assigned compliance policies to security groups
- Configured Defender for Business onboarding

### PowerShell Automation
- Connected to Microsoft Graph, Exchange Online, Teams and SharePoint via PowerShell
- Listed and managed users, groups and licenses via Microsoft Graph
- Created, updated, disabled and deleted users via PowerShell
- Assigned and removed Business Premium licenses programmatically
- Listed and managed Exchange Online mailboxes and permissions
- Bulk created 3 users from CSV with automatic license assignment
- Exported results to CSV for verification

### Monitoring and Reporting
- Reviewed M365 usage reports across Exchange, Teams, SharePoint and OneDrive
- Investigated audit logs for security scenarios in Microsoft Purview
- Reviewed sign-in logs in Entra ID for suspicious activity detection
- Configured security alert policies in compliance portal
- Reviewed and acted on Microsoft Secure Score recommendations
- Blocked legacy authentication via Conditional Access to improve Secure Score

---

## Screenshots

### A - Users

| | |
|---|---|
| ![A1](screenshots/A-Users/A01-active-users-list.png) | ![A2](screenshots/A-Users/A02-user-properties.png) |
| A1 - Active users list showing all test users across departments | A2 - User properties showing job title, department and manager |
| ![A3](screenshots/A-Users/A03-licenses-assigned.png) | ![A4](screenshots/A-Users/A04-user-blocked.png) |
| A3 - Licenses and apps tab showing Business Premium assigned | A4 - Blocked user with red icon demonstrating JML leaver process |

---

### B - Groups

| | |
|---|---|
| ![B1](screenshots/B-Groups/B01-active-groups-list.png) | ![B2](screenshots/B-Groups/B02-m365-group-finance-team.png) |
| B1 - Active groups showing M365 Groups, Security Groups and Distribution Lists | B2 - Finance Team M365 Group with members and owners |
| ![B3](screenshots/B-Groups/B05-dynamic-group-rule.png) | ![B4](screenshots/B-Groups/B06-dynamic-group-members.png) |
| B3 - Dynamic Group membership rule: department equals IT | B4 - Dynamic Group members auto-populated from IT department |

---

### C - Licensing

| | |
|---|---|
| ![C1](screenshots/C-Licensing/C01-licenses-overview.png) | ![C2](screenshots/C-Licensing/C02-license-user-assigned.png) |
| C1 - Billing licenses page showing Business Premium assigned vs available | C2 - User Licenses and apps tab showing Business Premium |

---

### D - Exchange Online

| | |
|---|---|
| ![D1](screenshots/D-Exchange/D01-exchange-admin-center.png) | ![D2](screenshots/D-Exchange/D02-mailboxes-list.png) |
| D1 - Exchange Admin Center dashboard | D2 - All user mailboxes listed with email addresses |
| ![D3](screenshots/D-Exchange/D03-shared-mailbox-created.png) | ![D4](screenshots/D-Exchange/D04-shared-mailbox-delegation.png) |
| D3 - IT Help Desk shared mailbox created | D4 - Delegation tab showing Full Access and Send As permissions |
| ![D5](screenshots/D-Exchange/D05-mail-flow-rule-enabled.png) | |
| D5 - Mail flow rule enabled appending legal disclaimer to all outbound email | |

---

### E - Microsoft Teams

| | |
|---|---|
| ![E1](screenshots/E-Teams/E01-teams-admin-center.png) | ![E2](screenshots/E-Teams/E02-teams-list.png) |
| E1 - Teams Admin Center dashboard | E2 - Teams list showing Finance Team and IT Support Team |
| ![E3](screenshots/E-Teams/E04-meeting-policy.png) | ![E4](screenshots/E-Teams/E06-external-access.png) |
| E3 - Custom meeting policy settings | E4 - External access and guest access configuration |

---

### F - SharePoint and OneDrive

| | |
|---|---|
| ![F1](screenshots/F-SharePoint-OneDrive/F01-sharepoint-admin-center.png) | ![F2](screenshots/F-SharePoint-OneDrive/F02-active-sites-list.png) |
| F1 - SharePoint Admin Center dashboard | F2 - Active sites list showing IT Department Hub |
| ![F3](screenshots/F-SharePoint-OneDrive/F04-site-permissions.png) | ![F4](screenshots/F-SharePoint-OneDrive/F07-onedrive-admin-access.png) |
| F3 - Site permissions showing Owner, Member and Visitor levels | F4 - OneDrive admin access via M365 Admin Center |

---

### G - Microsoft Entra ID

| | |
|---|---|
| ![G1](screenshots/G-Entra-ID/G01-entra-admin-center.png) | ![G2](screenshots/G-Entra-ID/G03-authenticator-enabled.png) |
| G1 - Microsoft Entra Admin Center dashboard | G2 - Microsoft Authenticator enabled as MFA method |
| ![G3](screenshots/G-Entra-ID/G04-sms-disabled.png) | ![G4](screenshots/G-Entra-ID/G06-sspr-properties.png) |
| G3 - SMS disabled following security best practice | G4 - SSPR enabled for all users |

---

### H - Conditional Access

| | |
|---|---|
| ![H1](screenshots/H-Conditional-Access/H01-security-defaults-off.png) | ![H2](screenshots/H-Conditional-Access/H02-ca-policies-list.png) |
| H1 - Security Defaults disabled - switching to Conditional Access | H2 - All four CA policies listed with status On |
| ![H3](screenshots/H-Conditional-Access/H03-ca001-settings.png) | ![H4](screenshots/H-Conditional-Access/H04-named-location-italy.png) |
| H3 - CA001 Require MFA for all users with exclusions configured | H4 - Italy Named Location for geo-based access control |

---

### I - SSPR

| | |
|---|---|
| ![I1](screenshots/I-SSPR/I01-sspr-enabled.png) | ![I2](screenshots/I-SSPR/I02-sspr-registration.png) |
| I1 - SSPR enabled for all users | I2 - Registration required on next sign-in |
| ![I3](screenshots/I-SSPR/I03-sspr-not-registered.png) | |
| I3 - SSPR error when user has not registered - demonstrates full flow | |

---

### J - Microsoft Defender

| | |
|---|---|
| ![J1](screenshots/J-Defender/J01-threat-policies.png) | ![J2](screenshots/J-Defender/J02-safe-attachments.png) |
| J1 - Threat policies page showing all security policies | J2 - Safe Attachments policy set to Block with sandbox analysis |
| ![J3](screenshots/J-Defender/J03-safe-links.png) | ![J4](screenshots/J-Defender/J06-device-onboarded.png) |
| J3 - Safe Links policy with time-of-click protection enabled | J4 - Windows device onboarded to Defender for Business |

---

### K - Microsoft Purview

| | |
|---|---|
| ![K1](screenshots/K-Purview/K01-purview-portal.png) | ![K2](screenshots/K-Purview/K02-retention-policy.png) |
| K1 - Microsoft Purview portal | K2 - 7-year email retention policy for Exchange mailboxes |
| ![K3](screenshots/K-Purview/K03-dlp-policy.png) | ![K4](screenshots/K-Purview/K05-sensitivity-label.png) |
| K3 - DLP policy protecting EU financial data | K4 - Confidential sensitivity label with encryption published |

---

### L - Microsoft Intune

| | |
|---|---|
| ![L1](screenshots/L-Intune/L01-intune-dashboard.png) | ![L2](screenshots/L-Intune/L02-compliance-policy.png) |
| L1 - Microsoft Intune dashboard | L2 - Windows compliance policy requiring BitLocker, PIN and antivirus |
| ![L3](screenshots/L-Intune/L04-configuration-profile.png) | ![L4](screenshots/L-Intune/L05-app-protection-policy.png) |
| L3 - Windows configuration profile for Defender and update settings | L4 - iOS app protection policy for Outlook (MAM) |

---

### M - PowerShell

| | |
|---|---|
| ![M1](screenshots/M-PowerShell/M01-connected-mggraph.png) | ![M2](screenshots/M-PowerShell/M02-get-mguser.png) |
| M1 - Connected to Microsoft Graph via PowerShell | M2 - Get-MgUser listing all tenant users |
| ![M3](screenshots/M-PowerShell/M07-exo-mailboxes.png) | ![M4](screenshots/M-PowerShell/M09-bulk-user-creation.png) |
| M3 - Exchange Online mailboxes listed via Get-EXOMailbox | M4 - Bulk user creation script - 3 users created and licensed from CSV |

---

### N - Monitoring and Reports

| | |
|---|---|
| ![N1](screenshots/N-Monitoring/N01-usage-reports.png) | ![N2](screenshots/N-Monitoring/N03-signin-logs.png) |
| N1 - M365 usage reports dashboard | N2 - Entra ID sign-in logs for security monitoring |
| ![N3](screenshots/N-Monitoring/N05-secure-score.png) | ![N4](screenshots/N-Monitoring/N06-secure-score-recommendations.png) |
| N3 - Microsoft Secure Score dashboard | N4 - Secure Score recommended actions list |

---

## Skills Demonstrated

| Role | Skills Covered in This Lab |
|------|---------------------------|
| IAM Engineer | Conditional Access, MFA, SSPR, Dynamic Groups, Entra ID P1, Zero Trust |
| M365 Administrator | Exchange Online, Teams, SharePoint, OneDrive, Licensing, User Lifecycle |
| IT Support Engineer | Help Desk workflows, JML process, shared mailboxes, device support |
| Security Engineer | Safe Attachments, Safe Links, Anti-phishing, Defender for Business, DLP |
| Endpoint Administrator | Intune compliance policies, configuration profiles, iOS MAM, Autopilot basics |
| Compliance Administrator | Retention policies, DLP, Sensitivity Labels, Audit Logs, Purview |
| PowerShell Engineer | Microsoft Graph API, Exchange Online, bulk operations, CSV automation |

---

## Tools and Technologies

| Category | Tools |
|----------|-------|
| Identity | Microsoft Entra ID P1, Conditional Access, MFA, SSPR, TAP |
| Productivity | Exchange Online, Microsoft Teams, SharePoint Online, OneDrive |
| Security | Defender for Business, Defender for Office 365 P1, Safe Attachments, Safe Links |
| Device Management | Microsoft Intune, Compliance Policies, Configuration Profiles, MAM |
| Compliance | Microsoft Purview, DLP, Retention Policies, Sensitivity Labels, Audit Logs |
| Automation | PowerShell, Microsoft Graph SDK, ExchangeOnlineManagement module |
| Admin Portals | admin.microsoft.com, entra.microsoft.com, security.microsoft.com, intune.microsoft.com, purview.microsoft.com |

---

## About

Built by **Praveenkumar Saminathan**

MSc Geoinformatics Engineering - Politecnico di Milano, Milan, Italy (Graduated July 2026)

Almost 4 years IT support experience including Tata Consultancy Services and freelance IT support in Milan.

**Certifications:** AWS Cloud Practitioner | AZ-900 (Microsoft Azure Fundamentals) | SC-900 (Microsoft Security, Compliance and Identity Fundamentals)

**Target Roles:** IAM Engineer | IT Infrastructure | IT Security | Cloud Security | SOC Analyst | IT Support | Cloud Support

- Portfolio: [praveenkumar-saminathan](https://orange3456.github.io/praveenkumar-saminathan.github.io/)
- LinkedIn: [praveenkumar-saminathan-993902228](https://www.linkedin.com/in/praveenkumar-saminathan-993902228)
- GitHub: [Orange3456](https://github.com/Orange3456)

---

> This lab was built entirely hands-on - every policy configured from scratch, every command typed, every error troubleshot and fixed. The process of building it is as valuable as the result.
