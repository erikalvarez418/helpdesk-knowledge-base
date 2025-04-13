# Escalation Playbook: Software Installation Failure

## Summary
User is unable to install or access software required for their job. May be blocked by permissions, Intune deployment issues, or licensing.

---

## Symptoms

- App doesn’t appear in Company Portal
- Intune install status shows failed or pending
- “You do not have permission to install” error
- License activation fails post-install

---

## Initial Troubleshooting (L1)

1. **Check Intune Assignment**
   - Endpoint Manager > Apps > Check if user/device is in the assignment group

2. **Verify Device Status**
   - Is the device compliant and synced?
   - Manually sync via: Settings > Accounts > Access work or school > Info > Sync

3. **Manual Install (if allowed)**
   - Download app installer and attempt manual install
   - Note error messages

4. **Check for Licensing Requirements**
   - Some apps require named-user or group-based license assignments

---

## Escalation Criteria

Escalate if:
- Assigned app fails to deploy after sync
- User cannot install manually due to policy
- Software is required to do primary job duties
- Licensing is not available or showing incorrect status

---

## Escalation Path

- Escalate to: **Intune Admin or App Deployment Team**
- Include:
  - Username and device name
  - App name/version
  - Intune assignment status
  - Install error (screenshot or code)

---

## Communication

- Priority:  
  - **P2 – High** if app is essential  
  - **P3 – Medium** if app is optional or workaround available

- Notify: App manager or department lead if user is blocked

---

## Notes

- Many apps require detection rules — bad rules = failed install
- Use `Company Portal` vs `Required` deployments appropriately
