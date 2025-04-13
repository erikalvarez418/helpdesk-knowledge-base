# Cannot Access SharePoint Site

## Summary
User reports they are unable to access a SharePoint site or receive a permissions error.

---

## Common Symptoms

- "Access Denied" error
- 404 or site not found
- SharePoint opens but specific library or folder fails

---

## Quick Fixes

1. **Verify Permissions**
   - Go to the SharePoint site > Settings > Site Permissions
   - Check if user is added directly or via a Microsoft 365 group

2. **Try in Private Browser Window**
   - Rule out cached credentials or token errors

3. **Confirm Correct URL**
   - Double-check spelling, folder structure, or outdated bookmark

---

## Advanced Troubleshooting

- Confirm the user is part of the connected Team (if SharePoint is tied to a Team)
- Check if site is restricted via Conditional Access or guest access policy
- For synced folders, verify OneDrive client is not blocking access

---

## Notes

- If site was recently renamed or moved, links may need to be refreshed
- Admins can use SharePoint admin center to reassign ownership or restore access
