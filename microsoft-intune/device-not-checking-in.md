# Intune Device Not Checking In

## Summary
Device is enrolled in Intune but not showing current status, receiving policies, or reporting activity. This usually means the device is not checking in properly.

---

## Common Symptoms
- Device shows as **"Not checked in"** for days
- Status = **Unknown** in Endpoint Manager
- Policies and apps not applying
- Intune says “Pending” for all tasks
- Remote actions (like wipe or sync) do not work

---

## Quick Checks

1. **Confirm Device is Online**
   - Check if the user has internet access
   - Ask the user to manually open **Settings > Accounts > Access work or school** > Click their account > Click **Info** > Scroll down to confirm **Last sync**

2. **Try Manual Sync**
   - In **Settings > Accounts > Access work or school**
   - Click the connected M365 account > Click **Info** > Click **Sync**

3. **Check Device in Endpoint Manager**
   - Go to [https://endpoint.microsoft.com](https://endpoint.microsoft.com)
   - Navigate to **Devices > All devices**
   - Search for the device > Review:
     - **Compliance status**
     - **Last check-in**
     - **Ownership** (Personal vs Corporate)
     - **OS platform** and version

---

## Advanced Troubleshooting

1. **Restart the Intune Management Extension**
   On the affected device (Windows only):

   - Open `Services.msc`
   - Restart **Microsoft Intune Management Extension**
   - Alternatively, run this in PowerShell:
     ```powershell
     Restart-Service -Name IntuneManagementExtension
     ```

2. **Check Enrollment Status**
   - Go to `Settings > Accounts > Access work or school`
   - If no account is listed, the device is not enrolled
   - Re-enroll using:  
     **Settings > Accounts > Access work or school > Connect > Work/School account**

3. **Review Intune Logs**
   - Logs are located at:  
     `C:\ProgramData\Microsoft\IntuneManagementExtension\Logs\`
   - Open `IntuneManagementExtension.log` to view sync events, errors, or delays

4. **Re-Enroll the Device (If Needed)**
   - Remove the work/school account from the device
   - Reboot
   - Re-add the account using **Company Portal** or **Access Work or School**

---

## Notes

- Devices must check in **at least once every 7 days** to stay compliant
- Hybrid-joined devices may be affected by **AD Connect** sync issues
- If multiple devices aren't checking in, check **Intune service health**

---

## Related Articles

- [App Deployment Not Working in Intune](./app-not-deploying.md)
- [Policy Not Applying to Device](./policy-not-applying.md)
- [Re-Enroll Device in Intune](./reenroll-device.md)
