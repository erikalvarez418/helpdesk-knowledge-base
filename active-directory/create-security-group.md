# How to Create a Security Group in Active Directory

## Summary
Security groups are used to manage user access to resources like shared folders, applications, and permissions. They can also be synced to Microsoft 365 or used in Group Policy.

---

## Common Scenarios
- Creating a group for new department or project
- Group-based access for a shared folder
- Assigning permissions via Group Policy
- Managing membership in Microsoft 365 or Intune

---

## Steps (Using ADUC)

1. Open **Active Directory Users and Computers**

2. Right-click the correct **Organizational Unit (OU)** > Choose **New > Group**

3. Fill in the following:
   - **Group name** (e.g., `HR_SharedDrive`)
   - **Group scope**: Select **Global** (common for user/resource grouping)
   - **Group type**: Choose **Security**

4. Click **OK**

---

## PowerShell Command

```powershell
New-ADGroup -Name "HR_SharedDrive" -SamAccountName "HR_SharedDrive" -GroupCategory Security -GroupScope Global -Path "OU=Groups,DC=domain,DC=com"
