# 04 — Exchange Online: Mailboxes, Groups & Mail Flow Rules

## Objective
Configure shared mailbox delegation, a distribution group, and mail flow (transport) rules to demonstrate messaging governance and security controls.

## Steps Taken

**1. Shared mailbox**
Created a shared mailbox, **IT-Support** (IT-Support@Diasporapay.onmicrosoft.com), via **Exchange admin centre > Recipients > Mailboxes**.

![Shared mailbox created successfully](../screenshots/04-exchange/01-shared-mailbox-created.png)

Delegated access configured under the mailbox's **Delegation** tab:
- **Send as**: Emmanuel Igbonaya, Samuel Kennedy
- **Read and manage (Full Access)**: Emmanuel Igbonaya, Samuel Kennedy

![Mailbox delegation permissions](../screenshots/04-exchange/02-mailbox-delegation.png)
![Mailbox delegation members](../screenshots/04-exchange/03-mailbox-delegation-members.png)

Full mailbox list, including the break-glass account and all test users:

![Mailboxes list](../screenshots/04-exchange/04-mailboxes-list.png)

**2. Distribution group**
Created **All-Staff-Announcements**, a Microsoft 365 group, with all test users (Emmanuel Igbonaya, Finance, Jesse Onojah, Samuel Kennedy) added as members and Jesse Onojah as owner.

![Distribution group created](../screenshots/04-exchange/05-distribution-group-created.png)

**3. Mail flow rules**
Two transport rules created under **Mail flow > Rules**, both confirmed **Enabled**:

| Rule | Condition | Action |
|---|---|---|
| **New Rule external** | Sender is external/internal → sender located outside the organization | Prepend the subject with `[EXTERNAL]`; set audit severity to High |
| **Block auto-forwarding** | Recipient is outside the organization; message type is auto-forward | Reject/block the message |

![Mail flow rule for external senders](../screenshots/04-exchange/06-mail-flow-rule-external.png)

Both rules confirmed live and enabled:

![Both mail flow rules enabled](../screenshots/04-exchange/07-mail-flow-rules-enabled.png)

The external-sender rule was also configured with an append-disclaimer variant, adding the message:
> "CAUTION: This email originated from outside the organisation. Do not click links or open attachments unless you recognise the sender and know the content is safe."

## Notes
Blocking auto-forwarding to external domains is one of the most commonly requested real-world mail flow controls, since it closes a well-known channel for data exfiltration via compromised mailboxes.
