# User Cannot Log Into Microsoft 365 or Entra ID

## Summary
User is unable to sign into Microsoft 365, Teams, Outlook, or other cloud services. This can be caused by incorrect credentials, account lockouts, license issues, MFA problems, or Conditional Access policies.

---

## Common Symptoms
- "Your account or password is incorrect"
- "We couldn’t sign you in"
- MFA prompt not appearing or failing
- Works in some apps but not others
- Login works in browser but not desktop apps

---

## Quick Fixes

1. **Check Credentials**
   - Confirm the user is entering the correct **UPN** (e.g., `user@domain.com`)
   - Reset the user’s password if unsure

2. **Try in Private Browser**
   - Open an incognito/private window
   - Go to [https://portal.office.com](https://portal.office.com)
   - Sign in using full credentials

3. **Test with Outlook Web App (OWA)**
   - Go to [https://outlook.office.com](https://outlook.office.com)
   - If it works here, desktop app may have cached credentials

---

## Troubleshooting Steps

1. **Check Account Status in Entra ID**
   - Go to [https://entra.microsoft.com](https://entra.microsoft.com)
   - Go to **Users > [username]**
   - Confirm:
     - ✅ Account is not **disabled**
     - ✅ Account is not **locked out**
     - ✅ Account is not **expired**

2. **Reset Password & MFA (if needed)**
   - If login issues continue, reset:
     - 🔐 Password
     - 🔁 MFA (use [Reset MFA guide](./reset-mfa.md))

3. **Check Sign-in Logs**
   - Go to user’s **Sign-in logs**
   - Look for failed attempts and reasons
   - Common blocks:
     - Conditional Access
     - Sign-in risk policy
     - Device not compliant

4. **Check for Licensing Issues**
   - Go to **Microsoft 365 Admin Center > Active users**
   - Ensure user has proper license (e.g., Microsoft 365 E3 or Business Premium)
   - Missing licenses = blocked services

---

## Notes
- Hybrid AD environments: Ensure password sync is working via **Azure AD Connect**
- Cloud-only users: Confirm identity source is set to **Cloud** not **External**
- Account changes may take a few minutes to propagate across services

---

## Related Articles
- [Reset MFA for a User](./reset-mfa.md)
- [User Blocked by Conditional Access](./conditional-access-block.md)
- [Password Reset Not Working](./entra-id-password-reset-not-working.md)
- [Reset User Password in Active Directory](../active-directory/reset-user-password.md)
