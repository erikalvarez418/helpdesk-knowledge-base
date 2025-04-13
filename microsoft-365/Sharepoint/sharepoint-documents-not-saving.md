# SharePoint Documents Not Saving or Uploading

## Summary
User is unable to save, upload, or edit documents in a SharePoint library. This may be caused by browser issues, permission errors, or sync problems.

---

## Common Symptoms

- “Upload failed” or “Save failed” messages
- File opens in read-only mode
- Unable to save changes back to SharePoint
- AutoSave disabled in Word, Excel, or PowerPoint

---

## Quick Fixes

1. **Open in Browser**
   - Click “Open in Browser” to bypass desktop app issues

2. **Check Permissions**
   - User may have **View Only** access
   - Ask SharePoint admin to confirm Edit access

3. **Disable Protected View**
   - In the Office app, go to:
     File > Options > Trust Center > Trust Center Settings > Protected View  
   - Uncheck “Enable Protected View for files from the internet”

---

## Advanced Troubleshooting

- **Check File Lock**
  - Document may be locked if another user is editing or app didn’t close properly
  - Wait a few minutes or check the document status in the library

- **Rename and Reupload**
  - Save a local copy and re-upload to SharePoint

- **Update Office**
  - Outdated versions of Word, Excel, or PowerPoint may block saving

---

## Notes

- Shared files opened from email links may default to read-only
- Syncing issues may require unlinking and re-syncing the OneDrive library
