# Escalation Playbook: Account Locked Out Repeatedly

## Summary
A user is repeatedly locked out of their Microsoft 365 or AD account due to failed logins. This could be due to saved credentials, mobile apps, or malicious attempts.

---

## Symptoms

- Account gets locked shortly after reset
- User is unable to stay logged in
- Lockout occurs multiple times a day

---

## Initial Troubleshooting (L1)

1. **Reset Password**
   - Use Active Directory or Entra ID
   - Ensure a strong, new password is used

2. **Force Log Out of All Sessions**
   - In Entra ID: User > Sign-in logs > Invalidate sessions

3. **Check Device Credentials**
   - Mobile device: Remove and re-add email account
   - Windows/Mac: Clear saved credentials from Credential Manager or Keychain

4. **Review Sign-In Logs**
   - Go to Entra ID > User > Sign-in logs
   - Look for failed sign-ins from unexpected locations or IPs

---

## Escalation Criteria

Escalate if:
- Lockouts continue after password reset and credential clearing
- Suspicious login attempts from outside expected regions
- Multiple users experience similar patterns

---

## Escalation Path

- Escalate to: **Security or Identity Team**
- Include:
  - Affected user
  - Times of lockouts
  - Sign-in locations or IPs from logs
  - Password reset status
  - Known devices using the account (BYOD, shared workstations, etc.)

---

## Communication

- Priority:
  - **P2 – High** if repeated and unresolved
  - **P1 – Critical** if login attempts are global or targeted

- Notify: Identity or Security lead, especially for executive accounts

---

## Notes

- Outlook mobile and Apple Mail are common offenders with stale passwords
- Shared devices can also retry with old credentials from cached sessions
