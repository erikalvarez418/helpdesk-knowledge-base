# How to Repair an Outlook Profile

## Summary
Corrupt or misconfigured Outlook profiles can cause issues with sending/receiving mail, syncing shared mailboxes, or startup problems. Repairing the profile can fix most user-specific Outlook issues.

---

## Common Symptoms
- Outlook stuck on **Loading Profile**
- Cannot send or receive email
- Shared mailboxes not syncing
- Calendar or folders not updating
- Frequent prompts for password

---

## Quick Repair (Recommended First)

1. Open **Control Panel** > Search for **Mail** > Click **Mail (Microsoft Outlook)**

2. Click **Email Accounts**

3. Select the affected email account > Click **Repair**

4. Follow the prompts to complete the repair

---

## Manual Repair Steps

If the quick repair doesn’t fix the issue:

1. **Remove and Re-add the Profile**
   - In **Mail Setup**, click **Show Profiles**
   - Select the current profile > Click **Remove**
   - Click **Add...** > Create a new profile name
   - Enter the user's email address and password

2. **Set the New Profile as Default**
   - After creation, select **Always use this profile**
   - Choose the new profile and click **Apply** > **OK**

3. Restart Outlook and test functionality

---

## PowerShell Check (Optional for Admins)

You can check the user's connection status to Microsoft 365 via:

```powershell
Test-OutlookConnectivity -Identity user@domain.com
```
