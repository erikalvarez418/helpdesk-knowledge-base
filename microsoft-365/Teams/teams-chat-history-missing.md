# Teams Chat History Missing

## Summary
User reports chat messages are missing, incomplete, or not syncing across devices.

---

## Common Symptoms

- Messages visible on one device but not another
- Recent chats missing after sign-in
- Unable to find specific messages from previous days

---

## Quick Fixes

1. **Sign Out and Back In**
   - Fully sign out of Teams
   - Close the app, relaunch, and sign back in

2. **Clear Teams Cache**
   - Navigate to: %appdata%\Microsoft\Teams
   - Delete folders: `Cache`, `IndexedDB`, `Local Storage`

3. **Check in Teams Web App**
   - https://teams.microsoft.com
   - If messages appear here, issue is with the local desktop app

---

## Additional Checks

- User might be looking in the wrong chat — search using keywords
- Deleted chats cannot be recovered unless via eDiscovery (admin-level)

---

## Notes

- Chat sync relies heavily on Teams cache and account token freshness
- Admins can run content searches in M365 compliance center if needed
