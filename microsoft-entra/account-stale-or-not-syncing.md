# Account Is Stale or Not Syncing from Active Directory

## Summary
User accounts synced from on-prem Active Directory to Entra ID (Azure AD) may stop syncing, show outdated info, or fail to appear in Microsoft 365. These are commonly referred to as "stale" accounts.

---

## Common Symptoms
- User exists in on-prem AD but not in Entra ID
- Name, email, or group changes don’t reflect in Microsoft 365
- License can't be assigned because user doesn't show up
- Sync status shows errors in Azure AD Connect
- User can't log into Microsoft 365 after being created in AD

---

## Quick Checks

1. **Verify the User Exists in Active Directory**
   - Open ADUC and confirm the user is in the correct **Organizational Unit (OU)**

2. **Check if the OU is Included in Sync Scope**
   - On the server with **Azure AD Connect**, run:
     - **Azure AD Connect > Configure > Customize synchronization options**
   - Confirm the OU is selected for sync

3. **Force a Manual Sync**

Open **PowerShell** as admin on the AD Connect server:

```powershell
Start-ADSyncSyncCycle -PolicyType Delta
Use -PolicyType Initial for a full sync (use sparingly)
```

## Advanced Troubleshooting

### Check Sync Status in Microsoft Entra Admin Center

1. Go to [https://entra.microsoft.com](https://entra.microsoft.com)
2. Navigate to: **Identity > Users**
3. Filter by: **Directory sync enabled**
4. Click the affected user and look at **Source of authority**:
   - `Windows Server AD` = Synced from on-prem
   - `Azure AD` = Cloud-only

---

### Check Synchronization Errors

1. Open **Event Viewer** on the AD Connect server
2. Navigate to:
   - **Applications and Services Logs > Directory Synchronization**
3. Look for **sync or export errors**

---

### Check Attribute Flow Rules

- Verify that the following attributes are valid and unique:
  - `proxyAddresses`
  - `userPrincipalName`
  - `mail`
- Duplicate or malformed values can silently block sync.

---

## Recovery Options

If the account appears corrupt:

1. Remove the user from the sync scope (move out of synced OU)
2. Run a **delta sync**
3. Wait for the account to be removed from Entra ID (up to 30 minutes)
4. Move the user back into the correct OU
5. Run a **full sync**

As a last resort:

- Convert the account to **cloud-only** (not ideal in hybrid environments)
- Recreate the account from scratch (must be approved)

---

## Notes

- Always ensure the **Azure AD Connect server** is healthy and up-to-date
- Run regular sync health checks
- Use **Azure AD Connect Health** if available (requires Azure AD Premium)

---

## Related Articles

- [Reset a User’s Password in Active Directory](../active-directory/reset-user-password.md)
- [User Cannot Log Into Microsoft 365](./user-cannot-login.md)
- [Entra ID: Reset MFA for a User](./reset-mfa.md)
