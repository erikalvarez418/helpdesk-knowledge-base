# Teams and SharePoint Permissions Not Syncing

## Summary
A user added to a Microsoft Team cannot access its linked SharePoint site or vice versa. This is usually caused by sync delay, broken group link, or manual permission override.

---

## Common Symptoms

- User is in the Team but gets “Access Denied” on SharePoint
- User was removed from Team but still has SharePoint access
- Files available in Teams but not via SharePoint (or vice versa)

---

## Quick Fixes

1. **Wait 15–30 Minutes**
   - Group membership sync from Teams to SharePoint can take some time

2. **Verify Group Membership**
   - Go to Microsoft 365 Admin Center > Groups > Active Groups
   - Search for the Team > Open the group and check **Members**
   - If the user isn’t listed, add them directly to the M365 group

3. **Remove/Re-add User to Team**
   - Forces membership refresh across Teams, SharePoint, and OneDrive

---

## Advanced Troubleshooting

- **Manually Grant Access in SharePoint**
  - Go to Site > Settings > Site Permissions
  - Add the user manually with correct role (Edit/Read)

- **Use SharePoint Admin Center**
  - If Team was deleted or group was broken, relink or recreate site permissions

---

## Notes

- Teams, SharePoint, and OneDrive share Microsoft 365 Groups under the hood
- Avoid editing SharePoint permissions directly unless necessary — use Teams/M365 group when possible
