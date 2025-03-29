# Printer Shows Offline but Is Powered On

## Summary
User is trying to print to a network or local printer, but Windows shows the printer status as "Offline" even though it’s powered on and connected.

---

## Common Symptoms
- Printer status shows "Offline" in `Control Panel > Devices and Printers`
- Print jobs get stuck in queue
- User unable to print even though printer works for others

---

## Quick Fixes
1. **Restart the Printer**
   - Power off the printer for 30 seconds
   - Power it back on and wait for full initialization

2. **Check Network Connection**
   - For network printers: Ping the IP address
   - For USB printers: Ensure cable is securely connected

3. **Disable “Use Printer Offline”**
   - Go to `Control Panel > Devices and Printers`
   - Right-click the printer > See what's printing
   - Click **Printer** tab > Uncheck **Use Printer Offline**

---

## Advanced Troubleshooting
1. **Restart Print Spooler Service**
   - Open `services.msc`
   - Right-click **Print Spooler** > Restart

2. **Reinstall the Printer**
   - Remove printer from Devices and Printers
   - Go to `Settings > Devices > Printers & scanners` > Add Printer
   - Use IP address for direct setup if needed

3. **Manually Assign a Port**
   - Go to printer properties > **Ports tab**
   - Verify correct IP address or USB port is selected
   - If not, click **Add Port** > Standard TCP/IP Port > Enter IP

---

## Notes
- For shared printers, verify the hosting PC is online and not in sleep mode.
- Static IP or DHCP reservation is recommended for network printers to avoid port mismatch.

---

## Related Articles
- [Printer Won’t Install via IP](./printer-wont-install.md)
- [Cannot Print to Shared Printer](./cannot-print-to-shared-printer.md)
