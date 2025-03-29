# Printer Won’t Install via IP

## Summary
User is unable to install a network printer using an IP address. The printer may not appear during search, or an error occurs when attempting to install the driver.

---

## Common Symptoms
- “Printer not found” or “Unable to connect”
- Error: 0x00000709, 0x0000007e, or similar
- Print queue installs but doesn’t work
- Printer appears offline even though it’s online

---

## Quick Fixes
1. **Ping the Printer**:
   - Open Command Prompt
   - Run: `ping [printer IP]` (e.g., `ping 192.168.1.50`)
   - If it fails, the device may not be online or on the same network

2. **Try Installing Manually**:
   - Open `Control Panel > Devices and Printers > Add a printer`
   - Click “The printer that I want isn’t listed”
   - Select “Add a printer using a TCP/IP address or hostname”
   - Enter the IP address > Use existing driver or manual `.inf` file

---

## Advanced Troubleshooting
1. **Check Windows Print Services**:
   - Run `services.msc`
   - Ensure **Print Spooler** is running. Restart the service if needed.

2. **Use the Latest Driver**:
   - Download from the manufacturer’s website
   - Use “Add Printer” wizard → “Have Disk” → Browse to `.inf` file

3. **Enable LPD or LPR Port Monitor** (for older printers):
   - Go to `Control Panel > Programs > Turn Windows features on or off`
   - Check **Print and Document Services > LPD Print Service** and **LPR Port Monitor**

4. **Clear Printer Registry Entries (if stuck)**:
   - Open `regedit`
   - Navigate to: `HKEY_CURRENT_USER\Software\Microsoft\Windows NT\CurrentVersion\Devices`
   - Remove stuck or broken printer entries (only if safe to do so)

---

## Notes
- Always verify the printer is online and has a static IP or DHCP reservation.
- Avoid installing from shared printers on other user PCs unless intentional.

---

## Related Articles
- [Printer Shows Offline but Is Powered On](./printer-shows-offline.md)
- [How to Find a Printer’s IP Address](./find-printer-ip.md)
