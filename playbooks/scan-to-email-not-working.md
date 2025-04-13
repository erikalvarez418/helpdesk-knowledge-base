# Escalation Playbook: Scan to Email Not Working

## Summary
User is unable to scan documents from a multifunction printer (MFP) to email. Often caused by SMTP misconfiguration or expired credentials.

---

## Symptoms

- "Email failed to send" error on printer screen
- Jobs stay in queue or disappear silently
- Works for print but not for scan
- Affects multiple scan destinations

---

## Initial Troubleshooting (L1)

1. **Verify SMTP Settings**
   - IP address or hostname of SMTP server
   - Port (e.g., 25, 465, or 587)
   - TLS/SSL settings

2. **Check Credentials**
   - Test using a valid service account email
   - Confirm password hasn't expired

3. **Test Scan to One Email**
   - Try sending to IT/admin address
   - Helps determine if it’s destination-specific

4. **Check Network Access**
   - Printer should reach SMTP server IP
   - Ping test from another device on same subnet

---

## Escalation Criteria

Escalate if:
- SMTP settings appear correct but still fails
- Scan works for some but not all recipients
- Scan fails across multiple MFPs or locations
- Service account lockout or password reset is suspected

---

## Escalation Path

- Escalate to: **Exchange Admin or Infrastructure/Network Team**
- Include:
  - Printer make/model and IP
  - SMTP settings used (host, port, SSL, auth)
  - Destination addresses tested
  - Screenshots of error or logs (if possible)

---

## Communication

- Priority:
  - **P2 – High** if scanning is core to business ops  
  - **P3 – Medium** if isolated or non-critical

- Notify: Email admin or print support team

---

## Notes

- Office 365 requires authentication and TLS — legacy settings may fail
- Use app password or SMTP relay connector if standard credentials don’t work
