# 01 — Tenant Setup, Users & Groups

## Objective
Stand up a working Microsoft 365 tenant and populate it with realistic test identities and groups to use as the foundation for the rest of the lab.

## Steps Taken

**1. Tenant provisioning**
Initially attempted to use the Microsoft 365 Developer Program to obtain a free, renewable E5 sandbox. This route was blocked — Microsoft currently restricts the developer sandbox benefit to members who hold an active Visual Studio subscription. As a fallback, a **Microsoft 365 Business Premium trial** was set up instead, giving access to Entra ID P1, Intune, Exchange Online, SharePoint, and Teams — everything required for the lab.

- Tenant domain: `Diasporapay.onmicrosoft.com`

**2. Test user creation**
Created five test identities via **Microsoft 365 Admin Centre > Users > Active users**, each assigned a Microsoft 365 Business Premium licence:

| Display Name | Username |
|---|---|
| Admin | Admin@Diasporapay.onmicrosoft.com |
| Emmanuel Igbonaya | EmmanuelIgbonaya@Diasporapay.onmicrosoft.com |
| Finance | Finance@Diasporapay.onmicrosoft.com |
| Jesse Onojah | JesseOnojah@Diasporapay.onmicrosoft.com |
| Samuel Kennedy | SamuelKennedy@Diasporapay.onmicrosoft.com |

Licence usage confirmed at 5/25 assigned under **Billing > Licenses**.

**3. Group creation**
- **IT-Support-Team** — a Security group, used later to scope Conditional Access and permissions.
- **Project-Alpha** — a Microsoft 365 group, which automatically provisioned a linked Teams team, SharePoint site, and shared mailbox for collaboration scenarios.

## Evidence
See the `/screenshots` folder in this repository for supporting evidence images from this section (tenant/enrolment screens, policy configuration, and confirmation dialogs).

## Notes
Choosing Business Premium over the Developer Program sandbox is a realistic constraint many admins hit in practice — documenting the workaround itself demonstrates troubleshooting rather than just following a guided path.
