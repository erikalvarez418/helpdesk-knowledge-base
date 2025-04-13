# Escalation Playbook: Printer Not Printing (Network Printer)

## Summary
User is unable to print to a shared or network printer. This may be due to driver issues, offline queues, or network misrouting.

---

## Symptoms

- Jobs stuck in queue with “Error” or “Offline” status
- Printer is pingable but unresponsive
- Test page fails or spools indefinitely
- Works for some users but not others

---

## Initial Troubleshooting (L1)

1. **Check Physical Printer**
   - Power, display, paper, toner, and error lights
   - Is it awake and connected via Ethernet/Wi-Fi?

2. **Verify IP Address**
   - Compare printer IP to expected address
   - Ping from user’s device:
     ping 192.168.x.x

3. **Clear Print Queue**
   - Control Panel > Devices and Printers > Right-click printer > See what’s printing > Cancel all

4. **Try Reinstalling Printer**
   - Remove and re-add using IP address

5. **Test from Another Device**
   - See if issue is user/device-specific

---

## Escalation Criteria

Escalate if:
- Multiple users affected
- Printer unreachable via IP
- Queue service fails to restart
- Issue persists after reinstall/reboot

---

## Escalation Path

- Escalate to: **Infrastructure or Print Services Team**
- Include:
  - Printer model and IP address
  - Usernames/devices affected
  - Steps already tried (queue clear, reinstall, ping test)
  - Screenshot of queue or error

---

## Communication

- Priority:  
  - **P2 – High** if shared office or classroom printer  
  - **P3 – Medium** if alternate printer exists

- Notify: Print support team or site lead

---

## Notes

- Some printers use static DHCP — confirm IP hasn’t changed
- If installed via print server, ensure server is reachable
