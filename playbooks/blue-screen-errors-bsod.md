# Escalation Playbook: Blue Screen Errors (BSOD)

## Summary
A user reports their device crashes and displays a blue screen (BSOD). This playbook outlines how to collect basic diagnostics and escalate appropriately.

---

## Symptoms

- Device crashes with a blue screen
- User sees codes like: DRIVER_IRQL_NOT_LESS_OR_EQUAL, MEMORY_MANAGEMENT, etc.
- Crashes occur during boot or while using specific programs
- Automatic restart after crash

---

## Initial Troubleshooting (L1)

1. **Ask for the Stop Code**
   - Example: SYSTEM_THREAD_EXCEPTION_NOT_HANDLED
   - If user doesn’t see it, have them take a picture or ask when it happens

2. **Check if Device Reboots**
   - Did the device restart on its own?
   - Can they still log in?

3. **Try Booting into Safe Mode**
   - Hold Shift > Restart > Troubleshoot > Advanced Options > Startup Settings > Enable Safe Mode

4. **Ask About Recent Changes**
   - New drivers, software, or Windows updates?

---

## Escalation Criteria

Escalate if:
- BSOD occurs more than once
- Prevents normal use of device
- Stop code indicates driver/hardware issue
- Device is unbootable or unstable even in Safe Mode

---

## Escalation Path

- Escalate to: **Desktop Support or Endpoint Engineer**
- Include:
  - Device name, user, and serial
  - Approx. time of crash
  - Stop code (if known)
  - Recent changes (apps, updates, devices)
  - Safe mode result (worked or failed)

---

## Communication

- Priority: **P2 – High**
- Notify: Hardware or imaging team if replacement may be needed

---

## Notes

- Most BSOD logs are stored at: C:\Windows\Minidump
- Tools like BlueScreenView or WinDbg can analyze dump files
