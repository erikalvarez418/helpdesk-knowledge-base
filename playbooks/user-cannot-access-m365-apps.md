# Escalation Playbook: User Cannot Access Microsoft 365 Apps

## Summary
User cannot access apps like Outlook, Teams, or OneDrive — often due to licensing, sign-in, or sync issues.

---

## Symptoms

- "You don’t have a license" error
- Outlook or Teams says "We can’t sign you in"
- OneDrive setup fails or doesn't sync
- Apps stuck loading after login

---

## Initial Troubleshooting (L1)

1. **Check License Assignment**
   - Go to Microsoft 365 Admin Center > Active Users
   - Ensure a license like Microsoft 365 Business or E3 is assigned

2. **Check Sign-In Logs**
   - Use Entra ID > Sign-in logs to see failure reason (blocked, expired token, etc.)

3. **Test Apps in Web**
   - Go to:
     - Outlook: https://outlook.office.com
     - Teams: https://teams.microsoft.com
     - OneDrive: https://onedrive.live.com

4. **Reboot & Re-sign In**
   - Ask user to log out from apps > reboot > re-login with full UPN (e.g., user@domain.com)

---

## Escalation Criteria

Escalate if:
- License is assigned but access still fails
- User cannot access any core apps
- Sign-in logs show conditional access or token errors
- New account not syncing into Microsoft 365 after AD creation

---

## Escalation Path

- Escalate to: **M365 Admin or Identity Team**
- Include:
  - Affected user and apps
  - Licensing status
  - Sign-in error messages
  - Whether access works in web vs. desktop
  - Steps already attempted

---

## Communication

- Priority:
  - **P1 – Critical** if preventing all access on first day
  - **P2 – High** if user can’t access major apps

- Notify: Microsoft 365 Admin team + user’s manager if blocked

---

## Notes

- If new user, confirm replication has completed (for synced/hybrid accounts)
- Check conditional access policies or recent changes to app assignments
- Clearing Office credentials via Windows Credential Manager may help
