# How to Unlock a User Account in Active Directory

## Summary
User accounts can become locked due to multiple failed login attempts. This guide explains how to identify and unlock a locked-out account using ADUC or PowerShell.

---

## Common Scenarios
- User receives “Account has been locked” message
- Login attempts rejected despite correct password
- Account lockout policy has triggered after repeated failed logins

---

## Steps to Unlock Account

### Option 1: Using Active Directory Users and Computers (ADUC)

1. Open **Active Directory Users and Computers**
   - Run: `dsa.msc`

2. Navigate to the correct **Organizational Unit (OU)**

3. Right-click the affected user > Click **Properties**

4. Go to the **Account** tab

5. If the account is locked:
   - You’ll see a message: **“Account is locked out”**
   - Click **Unlock account**

6. Click **Apply** > **OK**

---

### Option 2: Using PowerShell

To unlock the account via PowerShell:

```powershell
Unlock-ADAccount -Identity username

Get-ADUser -Identity username -Properties LockedOut | Select-Object Name, LockedOut
