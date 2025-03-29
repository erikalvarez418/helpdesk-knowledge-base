# Outlook Crashes on Startup

## Summary
Outlook crashes immediately after launch or during the profile loading stage. This issue is commonly caused by corrupted profiles, add-ins, or outdated software.

---

## Common Symptoms
- Outlook opens briefly, then closes
- Error: "Microsoft Outlook has stopped working"
- Crashes when clicking specific folders or emails
- Looping crash on launch
- Safe Mode works, but normal mode does not

---

## Quick Fixes

1. **Start in Safe Mode**
   - Press `Windows + R` > type: `outlook.exe /safe` > Enter
   - If Outlook opens here, the issue is likely caused by an add-in

2. **Disable Problematic Add-ins**
   - In Safe Mode: Go to **File > Options > Add-ins**
   - At the bottom, choose **COM Add-ins** > Click **Go**
   - Uncheck all add-ins and restart Outlook normally
   - Re-enable one at a time to isolate the issue

---

## Advanced Troubleshooting

1. **Repair Office**
   - Go to **Control Panel > Programs > Programs and Features**
   - Right-click **Microsoft Office** > Choose **Change**
   - Select **Quick Repair** first, then **Online Repair** if needed

2. **Create a New Outlook Profile**
   - Go to **Control Panel > Mail > Show Profiles**
   - Click **Add...**, name the new profile, and set it as default
   - Outlook will rebuild from scratch — sync may take time

3. **Check Windows & Office Updates**
   - Go to **Settings > Update & Security > Windows Update**
   - Also open Outlook > File > Office Account > **Update Options > Update Now**

4. **Run the Microsoft Support and Recovery Assistant (SaRA)**
   - Download from: [https://diagnostics.outlook.com](https://diagnostics.outlook.com)
   - Use the “Outlook keeps crashing” scenario

---

## Notes
- If Outlook crashes after a recent Windows or Office update, check for rollback guidance or known issues on the [Microsoft 365 Health Dashboard](https://portal.office.com/adminportal/home#/servicehealth)
- Large .OST or corrupted PST files can also cause crashes — archive or remove if needed

---

## Related Articles
- [Repair Outlook Profile](./repair-outlook-profile.md)
- [Outlook Not Sending Emails](./outlook-not-sending.md)
- [Outlook Stuck on Loading Profile](./loading-profile.md)
