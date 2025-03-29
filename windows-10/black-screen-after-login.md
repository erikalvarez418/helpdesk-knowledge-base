# Black Screen After Login

## Summary
User logs into Windows 10 and is met with a black screen. The mouse may or may not be visible, and no desktop, taskbar, or start menu appears.

---

## Common Symptoms
- Black screen with mouse cursor after login
- Ctrl + Alt + Del works, but nothing else
- User hears startup sounds but sees no UI
- Screen flashes briefly before going black again

---

## Quick Fixes
1. **Try Restarting Explorer**
   - Press `Ctrl + Shift + Esc` to open Task Manager
   - Click **File > Run new task**
   - Type: `explorer.exe` → Press Enter
   - If desktop loads, consider rebuilding the user profile

2. **Check Display Output**
   - Press `Windows key + P` → Tap arrow keys to switch display mode (use `Enter` to select)
   - This helps if Windows is projecting to a non-existent monitor

---

## Advanced Troubleshooting
1. **Boot into Safe Mode**
   - Force restart PC 3x to trigger Recovery Mode
   - Go to **Advanced options > Startup Settings > Enable Safe Mode**
   - Once booted, check:
     - Startup apps
     - Display drivers in Device Manager
     - Corrupted profile or recent Windows updates

2. **Check for Profile Corruption**
   - Log in with another account (admin, if possible)
   - If alternate account loads fine, original user profile may be corrupt
   - Solution: Create a new profile, transfer data

3. **Update or Roll Back Display Driver**
   - Open Device Manager > Display adapters
   - Right-click your GPU > Choose **Update Driver**
   - If issue started after update: **Roll back driver**

4. **Disable Fast Startup**
   - Open `
