# Cannot Connect to Wi-Fi

## Summary
User is unable to connect to a wireless network. The network may appear in the list of available networks, but connection attempts fail or show limited connectivity.

---

## Common Symptoms
- "Can't connect to this network" error message
- Wi-Fi is connected but shows "No Internet"
- Frequent disconnects or drops
- Network not appearing in list

---

## Quick Fixes
1. **Toggle Airplane Mode**: Turn on and off from the Action Center or `Settings > Network & Internet`.
2. **Restart the PC** and Wi-Fi router (if possible).
3. **Forget the network** and reconnect:
   - Go to `Settings > Network & Internet > Wi-Fi > Manage known networks`
   - Select the network > Forget > Reconnect and re-enter password

---

## Advanced Troubleshooting
1. **Update Wi-Fi driver**:
   - Open Device Manager (`devmgmt.msc`)
   - Expand "Network adapters"
   - Right-click Wi-Fi adapter > Update driver

2. **Reset TCP/IP Stack**:
   Run the following commands in Command Prompt (as admin):
   ```bash
   netsh winsock reset
   netsh int ip reset
   ipconfig /release
   ipconfig /renew
   ipconfig /flushdns
