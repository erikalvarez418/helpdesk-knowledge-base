# Escalation Playbook: Network Down / Site-Wide Outage

## Summary
This playbook guides technicians through the initial steps and escalation path when an entire site loses connectivity — impacting all users, systems, or internet access.

---

## Symptoms

- No internet or internal network access for entire office/campus
- Users report "no connection" or offline cloud tools (Teams, Outlook)
- Phones, printers, and Wi-Fi are also down
- Cannot reach local servers or cloud resources from site

---

## Initial Troubleshooting (L1/L2)

1. **Confirm Scope**
   - Ask: Is the issue affecting all users?
   - Try accessing from wired and wireless devices
   - Attempt to reach local resources (e.g., printers or file servers)

2. **Check for Local Power or Equipment Outage**
   - Verify if network closet, firewall, or modem has lost power
   - Check for UPS alarms or blinking equipment lights

3. **Ping Gateway or Router**
   - From any device, run:
     ping 192.168.1.1 (or site gateway)
   - If no response, local gateway is likely down

4. **Check Known Outages**
   - Verify internet provider status page (if accessible)
   - Contact site staff to physically inspect modem/firewall

---

## Escalation Criteria

Escalate immediately if:
- Entire site cannot access the network or internet
- No onsite technician is available to reboot or inspect equipment
- ISP involvement is required
- Multiple sites are affected (could be upstream firewall/cloud issue)

---

## Escalation Path

- Escalate to: **Network Engineer or ISP Contact**
- Include:
  - Location name/code
  - Time issue began
  - Scope (all users, wired/wireless/both)
  - Result of ping/gateway tests
  - Whether reboot was attempted
  - Contact person onsite (if available)

---

## Communication

- Tag as **P1 – Critical**
- Notify: IT Lead + Network Team + Onsite Support Contact
- Update ticket every 30–60 minutes until resolved

---

## Notes

- If the issue is power-related, include facilities or maintenance in communication
- If phone systems use VoIP, inform phone vendor/team if service is also impacted
