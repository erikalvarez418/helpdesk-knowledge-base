```markdown
# How to Add a Group to a Shared Folder’s Permissions

## Summary
Applying folder access to a security group (instead of individual users) makes permissions easier to manage and audit.

---

## Steps

1. On the file server, right-click the shared folder > **Properties**

2. Go to the **Security** tab > Click **Edit**

3. Click **Add**, type the name of the **security group** > Click **Check Names** > OK

4. Assign permissions:
   - Read
   - Modify
   - Full Control (rare — only for admin groups)

5. Click **Apply** > **OK**

---

## Optional: Update Sharing Permissions
If the folder is shared via the **Sharing** tab:
1. Click the **Sharing** tab > **Advanced Sharing**

2. Click **Permissions** > Add the same group and assign basic sharing permissions

> You still need to set NTFS permissions under the **Security** tab.

---

## Best Practices
- Use groups like `DeptName_Read`, `DeptName_Modify` for clarity
- Avoid giving individual users permissions directly
- Always verify access after adding the group

---

## Related Articles
- [Create a Security Group](./create-security-group.md)
- [Add a User to a Group](./add-user-to-group.md)
