# Outlook Not Receiving Emails

## Summary
User reports that they are not receiving new emails in Outlook, even though others can send and receive normally. This can be caused by sync issues, filters, rules, or profile corruption.

---

## Common Symptoms
- Inbox not updating with new messages
- Only receiving emails in Outlook Web (OWA), not desktop app
- Messages delayed or appear all at once later
- No error, but emails just don’t show

---

## Quick Fixes

1. **Check Internet & Outlook Status**
   - Bottom bar in Outlook should say **"Connected to Microsoft Exchange"**
   - If it says **"Working Offline"** or **"Disconnected"**, reconnect or check network

2. **Check Outlook Web App (OWA)**
   - Go to [https://outlook.office.com](https://outlook.office.com)
   - If emails appear there but not in the desktop app, the issue is local

3. **Check Filters and View Settings**
   - In the Inbox, click **View > View Settings > Filter**
   - Clear any filters
   - Also try **View > Reset View**

4. **Check Rules**
   - Go to **File > Manage Rules & Alerts**
   - Disable or delete any rules that may be moving messages

---

## Advanced Troubleshooting

1. **Update the Folder**
   - Right-click Inbox > **Update Folder**
   - Or press `Shift + F9` to manually sync

2. **Repair the Outlook Profile**
   - `Control Panel > Mail > Email Accounts > Repair`

3. **Create a New Outlook Profile**
   - From Mail setup, add a new profile and test it
   - Set it as default if issue is resolved

4. **Check for Cached Mode Issues**
   - Go to **Account Settings > Change > Uncheck “Use Cached Exchange Mode”**
   - Restart Outlook and test

---

## Notes
- If user has shared mailboxes, check if those are syncing normally
- Widespread issues could be caused by a Microsoft service disruption — check [Microsoft 365 Health](https://portal.office.com/adminportal/home#/servicehealth) if you’re an admin

---

## Related Articles
- [Outlook Not Sending Emails](./outlook-not-sending.md)
- [Outlook Stuck on Loading Profile](./loading-profile.md)
- [Repair Outlook Profile](./repair-outlook-profile.md)
