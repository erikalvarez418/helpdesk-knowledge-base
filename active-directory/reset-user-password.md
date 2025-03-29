# How to Reset a User's Password in Active Directory

## Summary
Resetting a user's password in Active Directory allows them to regain access to their account when they forget or are locked out.

---

## Common Scenarios
- User forgot their password
- Password expired and user can't log in
- Helpdesk receives request to reset credentials

---

## Steps to Reset Password

### Option 1: Using Active Directory Users and Computers (ADUC)

1. Open **Active Directory Users and Computers**
   - Run: `dsa.msc`

2. In the left pane, navigate to the correct **Organizational Unit (OU)**

3. Right-click the user account > Click **Reset Password**

4. Enter the new password

5. (Optional but recommended)
   - ✅ Check **User must change password at next logon**
   - ❌ Uncheck **User cannot change password** unless policy requires it

6. Click **OK** to apply the change

---

### Option 2: Using PowerShell

If using RSAT or remote PowerShell, run:

```powershell
Set-ADAccountPassword -Identity username -Reset -NewPassword (ConvertTo-SecureString "NewP@ssword1" -AsPlainText -Force)
