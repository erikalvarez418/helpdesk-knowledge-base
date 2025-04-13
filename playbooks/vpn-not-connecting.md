# Escalation Playbook: VPN Not Connecting

## Summary
User is unable to connect to the company VPN, blocking access to internal systems or remote work capabilities.

---

## Symptoms

- VPN app fails to connect or times out
- “Unable to establish a connection” message
- User is stuck on "Connecting..." or sees authentication error
- Remote users cannot access internal drives, systems, or apps

---

## Initial Troubleshooting (L1)

1. **Confirm Internet Access**
   - User must have stable internet before VPN will connect

2. **Reboot and Retry VPN**
   - Restart device and test again

3. **Verify VPN Credentials**
   - Are they using their current password?
   - Check if recent password change broke cached credentials

4. **Check VPN Client Logs (if accessible)**
   - Common error codes: 789, 809, 800 (IKE, port, or protocol errors)

5. **Test on Hotspot or Alternate Network**
   - Rule out home/work firewall blocking VPN ports

---

## Escalation Criteria

Escalate if:
- VPN consistently fails for user after basic troubleshooting
- VPN failure impacts access to core systems (files, apps, payroll, etc.)
- Multiple users report VPN issues (may be a firewall or tunnel issue)
- User is offsite and you cannot reach VPN infrastructure remotely

---

## Escalation Path

- Escalate to: **Network Engineer or Firewall Admin**
- Include:
  - Username and device name
  - VPN client type (built-in, GlobalProtect, FortiClient, etc.)
  - Error message/code
  - Network they're on (home, hotspot, public Wi-Fi)
  - Approx. time issue started
  - Whether they’ve had VPN access before

---

## Communication

- Priority: **P2 – High**  
- Notify: Network/Security team + user's manager (if blocked from working)
- Update ticket every 2–4 hours or upon change

---

## Notes

- Password resets or expired certs are common causes — check both
- If MFA is used, verify authentication method (push, code, etc.)
- Don’t attempt to reinstall VPN
