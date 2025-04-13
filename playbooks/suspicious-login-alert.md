# Escalation Playbook: Suspicious Login Alert

## Summary
An alert or log shows a login attempt from an unexpected location, device, or IP. Quick response helps prevent unauthorized access.

---

## Symptoms

- Alert from Microsoft Defender or Entra ID Risk Policies
- User receives alert email for unknown sign-in
- Admin notices login from unusual country, device, or time

---

## Initial Steps (L1)

1. **Confirm with User**
   - Ask if they were traveling, using VPN, or working offsite

2. **Review Sign-In Logs**
   - Go to Entra ID > Users > Sign-in logs
   - Filter by time, location, risk level, app used

3. **Check for MFA Usage**
   - Was MFA required?
   - Did the user approve or deny an unexpected request?

4. **Check Session Duration and Actions**
   - Did the session access Teams, Outlook, or attempt changes?

---

## Escalation Criteria

Escalate if:
- Login was not made by the user
- High-risk sign-in marked by Defender or Entra ID
- Login bypassed MFA
- Changes were made during session (mail rules, password reset, etc.)

---

## Escalation Path

- Escalate to: **Security Team or Microsoft 365 Incident Response Lead**
- Include:
  - Username and UPN
  - Sign-in location, IP address, and time
  - Risk level shown (low/medium/high)
  - Whether user verified activity
  - Any mailbox rule or setting changes

---

## Communication

- Priority: **P1 – Critical**
- Notify: Security, IT Director, and user’s manager if account access is compromised

---

## Notes

- Accounts with recent suspicious sign-ins should be monitored or temporarily disabled
- Use **Defender > Hunting > Identity logs** for deeper review
