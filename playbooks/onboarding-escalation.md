# Escalation Playbook: Onboarding Delay or Blocked

## Summary
This playbook handles situations where a new employee cannot start work on day one due to missing access, licensing, or equipment.

---

## Symptoms

- User cannot log in to computer or M365 apps
- Email account not created or licensed
- No hardware delivered or set up
- Missing app access or network permissions

---

## Initial Troubleshooting (L1)

1. **Verify Account Exists**
   - Check Active Directory or Entra ID
   - Confirm username, UPN, and group membership

2. **Check License Assignment**
   - Go to Microsoft 365 Admin Center > User > Licenses & Apps

3. **Check Hardware Status**
   - Is the laptop built and ready?
   - If shipped, get tracking and ETA

4. **Confirm App and Drive Access**
   - Are shared drives, apps, and Teams memberships provisioned?

---

## Escalation Criteria

Escalate if:
- Onboarding tasks were incomplete after ticket closure
- New hire cannot start work by 10 AM local time
- Hardware is missing or misrouted
- Licensing or system provisioning is broken

---

## Escalation Path

- Escalate to: **Account Provisioning, Imaging, or M365 Admin Team**
- Include:
  - New hire’s name and username
  - Start date and location
  - What’s missing (account, license, app, hardware)
  - Any completed steps (e.g., created in AD, but not licensed)

---

## Communication

- Priority: **P1 – Critical**
- Notify: Manager, provisioning lead, and onboarding coordinator

---

## Notes

- Always confirm onboarding tasks at least 48–72 hours before start date
- Document missed steps to improve handoff or automation processes
