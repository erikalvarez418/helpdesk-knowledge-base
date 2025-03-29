# How to Add a User to a Group in Active Directory

## Summary
Adding a user to a security or distribution group gives them access to resources such as file shares, email groups, printers, or applications.

---

## Common Scenarios
- User needs access to a shared drive
- Joining a department-specific group (e.g., HR, Finance)
- Granting access to Microsoft 365 features or apps
- Group membership required by Intune or Conditional Access

---

## Steps (Using ADUC)

1. Open **Active Directory Users and Computers**
   - Run: `dsa.msc`

2. Locate the user > Right-click > **Properties**

3. Go to the **Member Of** tab > Click **Add**

4. Type the name of the group (e.g., `Shared_HR_Drive`) > Click **Check Names**

5. Click **OK** to add the group

6. Click **Apply** > **OK**

> You can also open the group first and add the user via the **Members** tab.

---

## PowerShell Command

```powershell
Add-ADGroupMember -Identity "GroupName" -Members "username"
