# How to Disable or Enable a User Account in Active Directory

## Summary
Disabling a user account temporarily prevents login access without deleting the user or their data. Enabling the account restores access when needed.

---

## Common Scenarios
- Offboarding or user leaving the company
- Security hold or investigation
- Temporary leave of absence
- Reinstating a returning employee or contractor

---

## Steps to Disable a User Account (ADUC)

1. Open **Active Directory Users and Computers**
   - Run: `dsa.msc`

2. Navigate to the correct **Organizational Unit (OU)**

3. Right-click the user account > Click **Disable Account**

4. A small down arrow will appear on the user icon to indicate the account is disabled

---

## Steps to Enable a User Account

1. Open ADUC and find the user

2. Right-click the account > Click **Enable Account**

3. Ensure the account is not locked out or expired, and reset the password if needed

---

## PowerShell Commands

### Enable Account:
```powershell 
Enable-ADAccount -Identity username

```
### Disable Account:
```powershell
Disable-ADAccount -Identity username

```
