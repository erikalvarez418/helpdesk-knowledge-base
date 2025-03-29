# Cannot Add a Shared Mailbox in Outlook

## Summary
User is unable to manually add a shared mailbox to Outlook. This can happen due to missing permissions, incorrect method, or Outlook profile issues.

---

## Common Symptoms
- Error: “The specified object was not found in the store”
- Shared mailbox not found or doesn’t appear
- Auto-mapping doesn't add it automatically
- Manual add fails or doesn’t save

---

## Quick Fixes

1. **Verify Permissions in Microsoft 365 Admin Center**
   - Go to [https://admin.microsoft.com](https://admin.microsoft.com)
   - Navigate to **Groups > Shared mailboxes**
   - Select the mailbox > Confirm user has:
     - ✅ **Full Access**
     - ✅ **Send As** (if applicable)
   - Note: Changes may take 15–30 minutes to apply

2. **Restart Outlook**
   - Close and re-open Outlook after permissions are added

---

## Manual Add Steps (If Auto-Mapping Fails)

1. Open Outlook

2. Go to **File > Account Settings > Account Settings**

3. Double-click the user’s account > Click **More Settings**

4. Go to the **Advanced** tab > Click **Add**

5. Type the name or email of the shared mailbox > OK > OK > Next > Finish

6. Restart Outlook — the mailbox should now appear in the folder pane

---

## Alternative: Add as Separate Mailbox Account

This method gives more control and improves sync reliability.

1. Go to **File > Add Account**

2. Enter the shared mailbox email address

3. If prompted, sign in using the **primary user's credentials**

4. Outlook will open the shared mailbox as a separate account

> ✅ Use this method if the user has Full Access but auto-mapping isn’t working.

---

## PowerShell Fix for Auto-Mapping (Admin Only)

1. Remove existing permissions:

```powershell
Remove-MailboxPermission -Identity "shared@domain.com" -User "user@domain.com" -AccessRights FullAccess
```

2. Re-add without auto-mapping:

```powershell
Add-MailboxPermission -Identity "shared@domain.com" -User "user@domain.com" -AccessRights FullAccess -AutoMapping:$false
```
