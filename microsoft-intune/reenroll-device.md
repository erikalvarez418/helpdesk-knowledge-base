# How to Re-Enroll a Device in Intune

## Summary
If a device is not syncing, policies aren't applying, or the device is showing incorrect status in Intune, re-enrollment can resolve many persistent issues.

---

## Common Scenarios
- Device shows as **Not Compliant** or **Unknown** for days
- Policies or apps fail repeatedly
- Device appears in Intune twice or not at all
- Troubleshooting hasn't fixed the issue

---

## Method 1: Manual Unenroll and Re-Enroll (User-Side)

1. **Unenroll Device**
   - Go to **Settings > Accounts > Access work or school**
   - Select the work/school account > Click **Disconnect**
   - Confirm removal > Restart the device

2. **Re-Enroll Device**
   - Go back to **Access work or school > Connect**
   - Sign in with the user’s M365 credentials
   - Device will re-register and sync with Intune

---

## Method 2: Re-Enroll via Company Portal

1. Open **Company Portal** app

2. Select the device > Click **Remove**

3. After removal:
   - Restart device
   - Open Company Portal again > Sign in
   - Follow prompts to re-enroll

> 💡 Works best for BYOD or personal devices.

---

## Method 3: Use PowerShell (Admin-Side)

Run the following as **admin**:

```powershell
# Initiates re-enrollment
dsregcmd /leave
