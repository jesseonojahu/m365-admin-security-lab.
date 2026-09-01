# Microsoft 365 Administration & Security Lab

Microsoft 365 administration lab covering Entra ID, Intune, Exchange Online, SharePoint, and Teams governance.

**Stack:** Microsoft 365 · Entra ID · Intune · Exchange Online · SharePoint · Teams

## Project Overview

This project involved building and administering a Microsoft 365 tenant to simulate a real-world enterprise IT environment. The lab focused on identity and access management, endpoint security, mail flow governance, collaboration platform administration, and security policy enforcement across the Microsoft 365 ecosystem. All configurations were documented using structured runbook-style documentation to reflect common helpdesk and IT administration procedures.

## Objectives

- Microsoft 365 tenant administration and user lifecycle management
- Multi-Factor Authentication (MFA) configuration and enforcement
- Conditional Access policy creation and testing
- Exchange Online mail flow rule management
- Shared mailbox and group administration
- Microsoft Intune device enrolment and compliance management
- SharePoint permission and site administration
- Microsoft Teams governance and meeting policies

## Environment & Tools Used

| Category | Technologies |
|---|---|
| Administration | Microsoft 365 Admin Centre, User Lifecycle Management |
| Identity & Access | Microsoft Entra ID, Azure AD, MFA, Conditional Access |
| Device Management | Microsoft Intune, Windows Autopilot, Compliance Policies |
| Communication | Exchange Online, Shared Mailboxes, Mail Flow Rules |
| Collaboration | SharePoint Online, Microsoft Teams Admin Centre |
| Security | Legacy Authentication Blocking, Geo-restriction, Security Policies |

## Documentation

Detailed runbook-style write-ups for each section, with supporting evidence:

| Doc | Covers |
|---|---|
| [01 – Tenant Setup](docs/01-tenant-setup.md) | Tenant provisioning, test users, licensing, groups |
| [02 – Entra ID, MFA & Conditional Access](docs/02-entra-id-mfa-ca.md) | Break-glass account, CA policies, MFA registration |
| [03 – Intune](docs/03-intune.md) | Enrolment, Autopilot, compliance & configuration policies |
| [04 – Exchange Online](docs/04-exchange.md) | Shared mailboxes, delegation, distribution groups, mail flow rules |
| [05 – SharePoint & Teams (partial)](docs/05-sharepoint-teams.md) | Site sharing settings; Teams governance in progress |

## Repository Contents

```
/docs                            Runbook-style documentation for each lab area
/screenshots/01-tenant-setup      Evidence for tenant, users & groups
/screenshots/02-entra-mfa-ca      Evidence for Entra ID, MFA & Conditional Access
/screenshots/03-intune            Evidence for Intune enrolment & compliance
/screenshots/04-exchange          Evidence for Exchange mailboxes & mail flow rules
/screenshots/05-sharepoint-teams  Evidence for SharePoint & Teams
README.md                        This file
```

Screenshots are embedded directly inline within each doc, at the step they support — no separate evidence appendix needed.

## Skills Demonstrated

- Enterprise identity and access administration
- Conditional Access and Zero Trust policy design, including staged rollout (Report-only → On)
- Endpoint compliance and mobile device management, including troubleshooting failed MDM auto-enrolment
- Mail flow and messaging security governance
- Documentation of IT procedures in runbook format suitable for a service desk or NOC environment

---

*This lab was built independently as part of ongoing hands-on practice in Microsoft 365 administration and security operations.*
