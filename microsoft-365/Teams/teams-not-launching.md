# Microsoft Teams Not Launching

## Summary
Microsoft Teams fails to open, crashes immediately, or gets stuck on the loading screen.

---

## Common Symptoms

- Teams never opens or closes immediately after launching
- Stuck on "Loading Microsoft Teams" screen
- No error message but app silently fails

---

## Quick Fixes

1. **Restart the App**
   - Fully close Teams from system tray
   - Use Task Manager to end `Teams.exe`

2. **Clear Teams Cache**
   - Close Teams
   - Navigate to:
     %appdata%\Microsoft\Teams
   - Delete the contents of the following folders:
     - `cache`
     - `blob_storage`
     - `databases`
     - `local storage`
     - `tmp`

3. **Restart Computer and Launch Teams Again**

---

## Advanced Troubleshooting

- Reinstall Teams:
  - Uninstall via Control Panel
  - Re-download from https://teams.microsoft.com/downloads
- Check for conflicting login accounts
- Try launching Teams in browser to isolate desktop issue

---

## Notes

- Teams updates itself — issues can occur after updates, especially with cached data
- Teams desktop app is separate from web version — test both
