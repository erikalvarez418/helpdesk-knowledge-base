# OneDrive Not Syncing SharePoint Files

## Summary
User is unable to sync or access SharePoint files through OneDrive. This guide covers common causes and fixes for sync failures.

---

## Common Symptoms

- Sync status stuck at “Processing changes”
- Files not updating or appearing in local folder
- Red “x” icons or sync error messages
- SharePoint library not syncing to OneDrive

---

## Quick Fixes

1. **Restart OneDrive**
   - Right-click the OneDrive icon in the taskbar > Click **Close OneDrive**
   - Open OneDrive again from Start Menu

2. **Re-Sync the Library**
   - Go to the SharePoint site > Click **Sync**
   - This should launch OneDrive and begin syncing

3. **Check for Sync Conflicts**
   - Open OneDrive settings > View any errors
   - Resolve duplicate files or locked documents

---

## Advanced Troubleshooting

- **Reset OneDrive**
  - Run the following command:
    %localappdata%\Microsoft\OneDrive\onedrive.exe /reset
  - Reopen OneDrive after a few minutes if it doesn’t launch automatically

- **Check Storage Limit**
  - Ensure the user’s OneDrive or SharePoint storage quota isn’t full

- **Unlink and Re-link Account**
  - OneDrive settings > Account > Unlink this PC
  - Sign in again and set up sync

---

## Notes

- SharePoint libraries over 300,000 files can fail silently
- Folder names with special characters can also cause sync issues
