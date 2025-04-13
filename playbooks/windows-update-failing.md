# Escalation Playbook: Windows Update Failing

## Summary
User reports failed Windows Updates or repeated update errors. This playbook outlines how to resolve simple issues and escalate deeper system-level failures.

---

## Symptoms

- Error codes like 0x800f081f, 0x8024402c
- “We couldn’t complete the updates”
- Device reboots and rolls back updates
- Windows Update stuck at a percentage

---

## Initial Troubleshooting (L1)

1. **Reboot and Retry Updates**
   - Often resolves stuck updates

2. **Run Windows Update Troubleshooter**
   - Settings > Update & Security > Troubleshoot > Additional troubleshooters > Windows Update

3. **Check for Disk Space**
   - User needs at least 10 GB free

4. **Use `sfc /scannow` and `DISM`**
   - Run in admin Command Prompt or PowerShell:
     sfc /scannow  
     DISM /Online /Cleanup-Image /RestoreHealth

---

## Escalation Criteria

Escalate if:
- Updates fail after multiple reboots and troubleshooting
- Errors relate to system corruption or rollback
- Updates are critical security patches
- Affects multiple devices across site

---

## Escalation Path

- Escalate to: **System Admin or Imaging Team**
- Include:
  - Device name and user
  - Specific update KB number(s)
  - Error code(s)
  - Troubleshooting completed
  - Last time updates worked

---

## Communication

- Priority:
  - **P2 – High** if update is required for compliance or security
  - **P3 – Medium** if not blocking work

- Notify: Endpoint management or patching team

---

## Notes

- Some cumulative updates require previous ones to be installed
- If system file corruption is found, a reimage may be necessary
