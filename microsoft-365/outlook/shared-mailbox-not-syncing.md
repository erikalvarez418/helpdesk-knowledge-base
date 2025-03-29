# Shared Mailbox Not Syncing in Outlook

## Summary
User reports they cannot see recent emails or changes in a shared mailbox. This can result from sync delays, permission issues, or profile corruption.

---

## Common Symptoms
- Shared mailbox inbox is empty or out-of-date
- Folders don’t expand or update
- Cannot send from shared mailbox
- Shared mailbox is missing completely from Outlook

---

## Quick Fixes

1. **Restart Outlook**
   - Fully close and relaunch Outlook

2. **Check in Outlook Web (OWA)**
   - Go to [https://outlook.office.com](https://outlook.office.com)
   - Click user profile (top right) > **Open another mailbox**
   - If shared mailbox appears here but not in desktop app, it's a local issue

3. **Remove and Re-add Shared Mailbox**
   - Go to **File > Account Settings > Account Settings**
   - Double-click account > **More Settings**
   - Under **Advanced**, remove the shared mailbox > OK
   - Close Outlook, reopen, then re-add it

---

## Advanced Troubleshooting

1. **Check Auto-Mapping**
   - If the user was added via a group, auto-mapping may fail.
   - Use PowerShell to remove and re-add access with `AutoMapping:$false`.

   Example:
   ```powershell
   Remove-MailboxPermission -Identity "SharedMailbox" -User "username" -AccessRights FullAccess
   Add-MailboxPermission -Identity "SharedMailbox" -User "username" -AccessRights FullAccess -AutoMapping:$false
   ```

2. **Manually Add as Additional Account**
  - Instead of relying on auto-mapping:
  - Go to File > Add Account
  - Enter the shared mailbox email address
  - Sign in if prompted (use delegated access if required)
  - The shared mailbox will appear as a separate account with full mailbox functionality

3. **Check Permissions in Microsoft 365 Admin Center**
  - Go to https://admin.microsoft.com
  - Navigate to Groups > Shared mailboxes
  - Select the mailbox and confirm the user has:
  - ✅ Full Access
  - ✅ Send As (if needed)
Click Edit next to each permission type to adjust
Changes can take 15–30 minutes to take effect
