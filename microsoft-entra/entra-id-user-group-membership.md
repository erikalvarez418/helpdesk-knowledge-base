# How to View and Manage a User’s Group Membership in Entra ID

## Summary
Managing a user’s group membership in Entra ID (Azure AD) helps control access to apps, resources, Microsoft 365 services, Conditional Access, and Intune policies.

---

## Common Scenarios
- User needs access to Teams, SharePoint, or M365 apps
- Troubleshooting missing access or licenses
- Onboarding or offboarding tasks
- Assigning roles or device policies via dynamic groups

---

## View Group Membership (Entra Admin Center)

1. Go to [https://entra.microsoft.com](https://entra.microsoft.com)

2. Navigate to **Identity > Users** > Search for the user

3. Click on the user’s name

4. In the left panel, click **Groups**

5. Review the **Membership** tab:
   - Includes direct assignments and dynamic group memberships
   - You’ll see group name, type (security or Microsoft 365), and source

---

## Add User to a Group

1. While viewing the user’s **Groups** tab, click **+ Add memberships**

2. Select the desired group(s) > Click **Select**

3. Changes take effect immediately for most services

---

## Remove User from a Group

1. In the same **Groups** tab under the user profile

2. Select the group > Click **Remove**

> ⚠️ Don’t remove users from dynamic groups — those are based on rules and can’t be modified manually.

---

## PowerShell Alternative (For Admins)

### View All Groups:
```powershell
Get-AzureADUserMembership -ObjectId user@domain.com
```

### Add User to Group:
```powershell
# Connect to Azure AD
Connect-AzureAD

# Add user to group
Add-AzureADGroupMember -ObjectId <GroupObjectID> -RefObjectId <UserObjectID>
```

## Notes

- Dynamic groups are managed using rules (e.g., department, location)
- Some apps and policies (like Intune or Conditional Access) apply only through group assignment
- Always document group additions/removals for audit trails

---

## Related Articles

- [Add User to a Group in Active Directory](../active-directory/add-user-to-group.md)
- [Remove User from a Group](../active-directory/remove-user-from-group.md)
- [User Blocked by Conditional Access](./conditional-access-block.md)

