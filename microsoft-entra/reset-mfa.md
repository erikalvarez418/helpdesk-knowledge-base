# How to Reset a User’s MFA in Entra ID (Azure AD)

## Summary
Users may need their Multi-Factor Authentication (MFA) reset if they get a new phone, lose access to their authenticator app, or are locked out of their account.

---

## Common Scenarios
- User got a new phone and can’t access Authenticator app
- User lost or reset their device
- MFA prompt not working, stuck at sign-in
- Admin asked to reset MFA setup

---

## Reset MFA in Microsoft Entra Admin Center

1. Go to: [https://entra.microsoft.com](https://entra.microsoft.com)

2. In the left menu, click **Users**

3. Search for the affected user > Click their name

4. In the toolbar, click **Authentication methods**  
   *(If you don’t see it, go to the top-right “...” > Authentication methods)*

5. Click **Require re-registration for multifactor authentication**

6. Click **Yes** to confirm

> ✅ This will force the user to set up MFA again the next time they sign in

---

## Optional: Remove Existing MFA Methods

1. From the **Authentication methods** page

2. Under **Methods**, remove any existing entries:
   - Microsoft Authenticator
   - Phone
   - FIDO2 key
   - Email (if applicable)

3. Click **+ Add authentication method** if you want to preconfigure a method

---

## What the User Sees
On next login, they’ll be prompted to register for MFA again, as if it were their first time:
- Set up Authenticator app or receive text/call
- Choose their preferred verification method

---

## Notes
- This does **not** disable MFA permanently — it only resets the registration
- If Conditional Access policies are applied, ensure they’re not blocking the reset process
- If the user cannot complete the MFA prompt, use a **break-glass admin account** to help

---

## Related Articles
- [User Can’t Log Into Microsoft 365](../microsoft-365/user-cannot-login.md)
- [Check Conditional Access Policy Blocks](./conditional-access-block.md)
- [Reset User Password in AD](../active-directory/reset-user-password.md)
