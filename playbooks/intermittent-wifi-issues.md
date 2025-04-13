# Escalation Playbook: Intermittent Wi-Fi Issues

## Summary
This playbook covers recurring or inconsistent Wi-Fi problems that affect multiple users or devices and require deeper investigation.

---

## Symptoms

- Users randomly disconnect from Wi-Fi
- Slow speeds or dropped Zoom/Teams calls
- Devices bounce between access points
- Some areas are worse than others

---

## Initial Troubleshooting (L1)

1. **Identify Pattern**
   - Who is affected (1 user vs many)?
   - Where are they located?
   - When does it happen (time of day, after reboot, etc.)?

2. **Basic Device Check**
   - Restart device and reconnect to Wi-Fi
   - Forget and re-add the network
   - Test on another network (hotspot or guest)

3. **Test Device Near AP**
   - Have the user move near a known access point
   - If connection stabilizes, it may be signal-related

4. **Check if Wired Works**
   - If hardline internet is fine, it’s likely Wi-Fi-specific

---

## Escalation Criteria

Escalate if:
- Multiple users across the same area report recurring Wi-Fi issues
- The same access point(s) consistently drop users
- Wi-Fi is impacting instruction, executive use, or operations
- Reboots and reconnects do not resolve the issue

---

## Escalation Path

- Escalate to: **Network Engineer or Wireless Infrastructure Team**
- Include:
  - Affected area(s)
  - Number of users/devices
  - SSID name and device types (Windows, iOS, etc.)
  - Approximate time window when issue occurs
  - Access point name (if visible from UniFi or dashboard)
  - Steps already taken (restart, reconnect, etc.)

---

## Communication

- Tag as **P2 – High** (P1 if affecting site-wide service)
- Notify: Network team and onsite support
- Update ticket at least every 2 hours or as advised

---

## Notes

- Ubiquiti/UniFi and Meraki dashboards can show signal strength and device movement
- Be wary of overcrowded APs or non-enterprise devices flooding the signal
