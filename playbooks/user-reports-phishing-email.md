# Escalation Playbook: User Reports Phishing Email

## Summary
A user has reported receiving a suspicious or phishing email. This playbook outlines how to investigate and escalate potential threats quickly.

---

## Symptoms

- Email asks for login info, payments, or clicks on strange links
- Impersonation of vendors, HR, or executives
- User reports “this email doesn’t look right”

---

## Initial Steps (L1)

1. **Thank the User & Get Details**
   - Ask for full message or screenshot
   - Have them right-click > Report > Phishing (if using Outlook)

2. **Do NOT Click Any Links or Open Attachments**

3. **Quarantine the Email (if not auto-detected)**
   - Go to Microsoft 365 Security Portal
   - Search user in **Email & Collaboration > Explorer**
   - Quarantine the message manually if needed

4. **Check Other Recipients**
   - Use **Threat Explorer** or **Microsoft Defender** to see if others received it

---

## Escalation Criteria

Escalate if:
- Email was sent to multiple users
- Contains credential-harvesting links
- Appears to spoof an internal domain or executive
- User clicked or submitted any info

---

## Escalation Path

- Escalate to: **Security or SOC team**
- Include:
  - Screenshot or .eml file of the phishing message
  - Time received and reported
  - Whether user clicked or opened anything
  - Threat Explorer summary (if available)

---

## Communication

- Priority:
  - **P1 – Critical** if users clicked or widespread
  - **P2 – High** if targeted but contained

- Notify: Security team + IT Manager

---

## Notes

- Educate user on proper reporting: use “Report” button in Outlook if available
- Use Defender’s **“Submit to Microsoft”** if email was not flagged by filters
