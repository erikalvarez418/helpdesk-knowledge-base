# App Not Deploying in Intune

## Summary
An application assigned through Intune isn't installing on the user's device. This can happen due to detection rule errors, incorrect assignment, policy conflicts, or sync issues.

---

## Common Symptoms
- App status in Intune shows **Pending**, **Failed**, or **Not applicable**
- App never appears in Company Portal
- App installs on some devices but not others
- End user receives no error, but app isn’t installed

---

## Quick Checks

1. **Confirm App Assignment**
   - Go to [https://endpoint.microsoft.com](https://endpoint.microsoft.com)
   - Navigate to **Apps > All apps**
   - Click the app > Go to **Assignments**
   - Ensure the app is assigned to the correct **group** and set to **Required** or **Available**

2. **Check Device Group Membership**
   - Go to **Devices > All devices** > Click device
   - Scroll to **Primary user** > View user’s group memberships
   - Make sure user/device is in the correct Azure AD group tied to the app assignment

3. **Sync the Device**
   - Ask user to go to:
     - **Settings > Accounts > Access work or school** > Info > Click **Sync**
   - Or trigger sync from Intune portal:
     - **Devices > [Device] > Sync**

---

## Advanced Troubleshooting

1. **Review App Install Status**
   - In the Intune portal:
     - **Apps > Monitor > App install status**
     - Filter by the affected app and device
     - Look for messages like:
       - `Detection rule failed`
       - `Dependency failure`
       - `Install timeout`

2. **Check Detection Rules**
   - For Win32 apps:
     - If detection rule is incorrect, app will not report as installed
   - Example fix:
     - Change from exact file version match to folder/file existence

3. **Review Intune Logs on Device**
   - Logs are found at:
     ```
     C:\ProgramData\Microsoft\IntuneManagementExtension\Logs\
     ```
   - Open `IntuneManagementExtension.log` and search for:
     - `Install Failed`
     - `Detection failed`
     - `0x87D...` error codes

4. **Manually Test App Install**
   - Download the `.intunewin` package manually and install it on a test machine
   - This helps verify the issue is with the installer itself or Intune deployment

---

## Notes

- Some apps may require **reboot** to complete install
- Use **Available** assignment for optional installs (shows up in Company Portal)
- Use **Required** only when you want auto-installation without user interaction

---

## Related Articles

- [Device Not Checking In to Intune](./device-not-checking-in.md)
- [Intune Policy Not Applying](./policy-not-applying.md)
- [How to Create a Win32 App in Intune](./create-win32-app.md)
