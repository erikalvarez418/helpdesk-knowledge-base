# How to Create a New User in Active Directory

## Summary
Creating a new user account in Active Directory is a standard onboarding task. This guide walks through creating the account, setting an initial password, and applying group memberships.

---

## Prerequisites
- User info: First name, last name, username, job title, department
- Know which **Organizational Unit (OU)** to place the user in
- Verify any required **security or distribution groups**

---

## Steps to Create a New User in ADUC

1. Open **Active Directory Users and Computers**
   - Run: `dsa.msc`

2. Navigate to the correct **Organizational Unit (OU)**

3. Right-click in the blank space or on the OU > Choose **New > User**

4. Fill in the following:
   - First Name / Last Name
   - Full Name: Auto-filled (you can edit if needed)
   - User logon name: Usually `first.last` or per company standard

5. Click **Next**, then:
   - Set a temporary password (follow org password policy)
   - Check **User must change password at next logon**
   - Uncheck **User cannot change password**, unless required

6. Click **Next > Finish**

---

## Post-Creation Tasks

### Add to Security/Distribution Groups
1. Right-click the user > **Properties**
2. Go to **Member Of** tab > Click **Add**
3. Enter group names (e.g., `Domain Users`, `HR Shared Drive Access`, `Helpdesk`)

### Set Department, Job Title, Etc. (Optional)
- Still in **Properties**, go to the **Organization** tab
- Enter **Title**, **Department**, **Manager** if required

---

## PowerShell Alternative

```powershell
New-ADUser `
 -Name "John Smith" `
 -GivenName "John" `
 -Surname "Smith" `
 -SamAccountName "john.smith" `
 -UserPrincipalName "john.smith@domain.com" `
 -Path "OU=Users,DC=domain,DC=com" `
 -AccountPassword (ConvertTo-SecureString "TempPass123!" -AsPlainText -Force) `
 -Enabled $true `
 -ChangePasswordAtLogon $true
