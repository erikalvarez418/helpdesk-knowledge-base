# Offboarding a User

## Summary
Proper offboarding ensures company data is secure, licenses are reclaimed, and access is removed in a timely manner.

---

## Pre-Offboarding Checklist

- Confirm last day with manager or HR
- Check for data ownership transfers
- Identify resources to revoke (email, shared folders, apps, etc.)

---

## Step-by-Step

1. **Disable Account**
   - In Active Directory or Entra ID
   - Optionally move to "Disabled Users" OU

2. **Reset Password**
   - Prevent unauthorized access before removal

3. **Revoke Access**
   - Remove licenses in Microsoft 365 Admin Center
   - Remove from shared mailboxes, Teams, and groups
   - Disable MFA

4. **Handle Device**
   - Collect physical device if applicable
   - Initiate wipe via Intune or local reimage

5. **Transfer Ownership**
   - Transfer files from OneDrive
   - Set up mailbox forwarding or shared access
   - Reassign ticket ownership, projects, or shared folders

6. **Document**
   - Confirm all actions in ticket
   - Note final status and storage of any user data (OneDrive, email export)

---

## Notes

- Follow your org’s HR and compliance requirements
- Retain mailboxes per legal hold policy, if needed
- Use PowerShell scripts for faster deprovisioning if doing in bulk
