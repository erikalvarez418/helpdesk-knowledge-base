# Escalation Playbook: Email Delivery Failure

## Summary
User reports their email to an external or internal recipient isn’t being delivered. This playbook helps identify if it's a user-side issue or a mail flow/server problem.

---

## Symptoms

- “Message not delivered” bounce-back
- NDR (Non-Delivery Report) with error codes like 5.1.1, 5.7.1, etc.
- External recipients never receive emails
- Internal emails delay or disappear

---

## Initial Troubleshooting (L1)

1. **Review Bounce Message**
   - Ask user to forward the full bounce-back
   - Note the error code (e.g., 550 5.1.1 = invalid recipient)

2. **Check Recipient Email Address**
   - Confirm correct spelling and domain
   - Ensure recipient account still exists (if internal)

3. **Send a Test Email**
   - Try sending to yourself or another address
   - Ask recipient to check spam/junk folder (for external)

4. **Test in Outlook Web**
   - Rule out client issues by using https://outlook.office.com

---

## Escalation Criteria

Escalate if:
- Multiple users are impacted
- Email fails to external domains (could be outbound block, DNS, or blacklist)
- Mail flow rules, transport connectors, or SPF/DKIM/DMARC may be involved
- Delivery failures persist across devices and apps

---

## Escalation Path

- Escalate to: **Microsoft 365 Administrator or Email Security Team**
- Include:
  - Sender & recipient email addresses
  - Time sent
  - Full bounce-back/NDR
  - Test results (webmail, other accounts)
  - Whether other users are affected
  - Screenshots of errors (if no NDR available)

---

## Communication

- Priority:  
  - **P2 – High** if impacting external comms or executives  
  - **P3 – Medium** if limited to internal or isolated cases

- Notify: M365 Admins and user's manager if blocked from business ops

---

## Notes

- Common external bounce causes:
  - Recipient server blocked your domain (check public blocklists)
  - SPF/DKIM/DMARC misconfigurations
  - Blacklisting or malware flags

- Internal delivery issues may involve mail flow rules or licensing issues
