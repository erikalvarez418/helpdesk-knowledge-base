# Escalation Playbook: Shared Mailbox Permission Issue

## Summary
User cannot access or send from a shared mailbox they should have access to. This playbook guides the steps to verify and escalate the issue.

---

## Symptoms

- "Cannot expand the folder" error in Outlook
- Shared mailbox missing from folder list
- Cannot send as or send on behalf of shared mailbox
- Access works in web but not desktop (or vice versa)

---

## Initial Troubleshooting (L1)

1. **Verify M365 Permissions**
   - Check if the user has **Full Access** and/or **Send As** permissions
   - Use Microsoft 365 Admin Center or PowerShell:
     Get-MailboxPermission shared@domain.com  
     Get-RecipientPermission shared@domain.com

2. **Re-add Mailbox in Outlook**
   - File > Account Settings > More Settings > Advanced > Add mailbox

3. **Try in Web**
   - Go to https://outlook.office.com > Profile icon > Open another mailbox

4. **Have User Reboot & Reconnect**
   - Auto-mapping may require sign-out/sign-in or profile reset

---

## Escalation Criteria

Escalate if:
- Permissions are correctly assigned but access still fails
- Auto-mapping not working across multiple users
- Send As fails despite proper permissions
- Mailbox is hybrid (on-prem) and sync issues are suspected

---

## Escalation Path

- Escalate to: **Exchange Admin or Microsoft 365 Admin**
- Include:
  - Shared mailbox name and email
  - Affected user(s)
  - Specific error or behavior
  - Permissions assigned (Full Access, Send As, Send on Behalf)
  - Steps tried (e.g., manual add, web test)

---

## Communication

- Priority:
  - **P2 – High** if user needs mailbox for job-critical tasks
  - **P3 – Medium** otherwise

- Notify: M365 Admins or escalation lead

---

## Notes

- Permissions can take 15–30 mins to propagate in cloud
- Full Access does not include Send As by default
- Mailboxes synced from on-prem must be adjusted in AD
