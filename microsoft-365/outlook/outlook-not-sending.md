# Outlook Not Sending Emails

## Summary
User reports that emails stay stuck in the Outbox or never reach recipients. This guide covers quick and advanced troubleshooting steps.

---

## Common Symptoms
- Email stuck in **Outbox**
- "Send/Receive error" message
- Mail appears to send but never arrives
- Outlook says **"Disconnected"** or **"Working Offline"**

---

## Quick Fixes

1. **Check Internet Connection**
   - Make sure the device is online and connected to the network

2. **Force Send/Receive**
   - Click **Send/Receive > Send/Receive All Folders**
   - Or press `Ctrl + M`

3. **Toggle Work Offline**
   - Go to **Send/Receive tab**
   - If **Work Offline** is highlighted, click it to reconnect

4. **Restart Outlook**
   - Fully close Outlook and re-open to refresh connection

---

## Advanced Troubleshooting

1. **Test in Outlook Web App (OWA)**
   - Log in at [https://outlook.office.com](https://outlook.office.com)
   - If sending works here, the issue is with the local Outlook client

2. **Clear Stuck Items**
   - Go to **Outbox** > Move stuck messages to **Drafts**
   - Try re-sending or editing them

3. **Repair Outlook Profile**
   - Go to **Control Panel > Mail > Show Profiles**
   - Click **Email Accounts > Repair** on the affected profile

4. **Create New Outlook Profile**
   - In **Mail Setup**, choose **Add...** to create a new profile
   - Set the new profile as default and test again

5. **Check for Large Attachments**
   - Emails over 20–25MB may not send
   - Use OneDrive or compress large files

---

## Notes
- If emails send fine in OWA but not in the desktop app, focus on profile or local network issues
- If multiple users are affected, escalate to M365 admin to check Exchange Online status

---

## Related Articles
- [Outlook Not Receiving Emails](./outlook-not-receiving.md)
- [Outlook Stuck on Loading Profile](./loading-profile.md)
- [Repair Outlook Profile](./repair-outlook-profile.md)
