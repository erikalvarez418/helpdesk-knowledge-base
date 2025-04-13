# Intune Policy Not Applying to Device

## Summary
A configuration profile, compliance policy, or security baseline in Intune is not applying to a device. This could be due to group assignment issues, sync delays, conflicts, or OS limitations.

---

## Common Symptoms
- Profile shows as **Pending**, **Failed**, or **Not Applicable**
- Settings do not show up on the device
- Device does not meet compliance despite being configured correctly
- User receives compliance errors on a compliant machine

---

## Quick Checks

1. **Verify Policy Assignment**
   - Go to [https://endpoint.microsoft.com](https://endpoint.microsoft.com)
   - Navigate to:
     - **Devices > Configuration profiles**
     - Or **Devices > Compliance policies**
   - Click the affected policy > Go to **Assignments**
   - Confirm the user or device group is included

2. **Check Group Membership**
   - Go to **Devices > [Device]**
   - Check **Primary user** > View user’s group memberships
   - Confirm user or device is part of the target group

3. **Trigger Manual Sync**
   - On the device:
     - **Settings > Accounts > Access work or school > Info > Sync**
   - Or in Endpoint Manager:
     - **Devices > [Device] > Sync**

---

## Advanced Troubleshooting

1. **Review Policy Deployment Status**
   - Go to:
     - **Devices > Configuration profiles > [Policy] > Device status**
   - Look for:
     - `Error`, `Conflict`, or `Not applicable`

2. **Understand 'Not Applicable'**
   - This usually means:
     - The policy doesn’t apply to the OS version
     - Targeted platform is incorrect (e.g., policy is for Windows 11, but device is on Windows 10)

3. **Check Conflicting Policies**
   - Two profiles setting the same value can conflict
   - Use **Intune > Reports > Policy Conflicts** to identify overlapping settings

4. **Review Intune Logs**
   - Logs found at:
     ```
     C:\ProgramData\Microsoft\IntuneManagementExtension\Logs\
     ```
   - Look in `IntuneManagementExtension.log` for:
     - `Policy conflict`
     - `Error applying configuration`
     - `Remediation failed`

---

## Notes

- Some profiles (like BitLocker or Defender) require reboot to take effect
- Settings in a **Custom OMA-URI** policy may silently fail without proper formatting
- Use **Security Baselines** only when you're not using other overlapping configuration profiles

---

## Related Articles

- [Device Not Checking In to Intune](./device-not-checking-in.md)
- [App Not Deploying in Intune](./app-not-deploying.md)
- [Re-Enroll a Device in Intune](./reenroll-device.md)
