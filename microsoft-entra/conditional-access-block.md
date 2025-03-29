# User Blocked by Conditional Access Policy

## Summary
Conditional Access policies control when, where, and how users can access Microsoft 365 and cloud apps. If misconfigured, they can prevent users from logging in.

---

## Common Symptoms
- "You can't get there from here" error
- User blocked from signing into Microsoft 365 apps
- Login works on one device but fails on another
- Blocked after traveling or changing locations

---

## Quick Checks

1. **Verify the Error Message**
   - Screenshot or copy the error
   - Look for phrases like "Blocked by Conditional Access" or "Sign-in was unsuccessful"

2. **Confirm the Policy Scope**
   - Go to [https://entra.microsoft.com](https://entra.microsoft.com)
   - **Identity > Conditional Access > Policies**
   - Review policies that apply to:
     - The user
     - Their group
     - The app they’re accessing (e.g., Exchange, SharePoint)

3. **Check Sign-in Logs**
   - Go to **Users > [User Name] > Sign-in logs**
   - Look for **Status: Failure**
   - Click the log entry to view **Conditional Access** tab for applied policy

---

## Resolution Options

- **Exclude User from Policy**  
  Edit the policy to temporarily exclude the affected user or group.

- **Adjust the Policy Conditions**  
  Common misconfigurations include:
  - Location restrictions (e.g., only trusted locations)
  - Device state (e.g., only compliant devices)
  - Sign-in risk level or MFA enforcement

- **Temporarily Disable the Policy**  
  If the impact is widespread and urgent:
  - Set policy to **Report-only**
  - Or disable until conditions are corrected

---

## Best Practices
- Never apply Conditional Access policies to **all users** without excluding a break-glass admin account
- Use **Report-only** mode to test changes before enforcing
- Document any user exclusions for security reviews

---

## Related Articles
- [Reset MFA for a User](./reset-mfa.md)
- [User Cannot Log Into Microsoft 365](../microsoft-365/user-cannot-login.md)
- [Password Reset Not Working](./entra-id-password-reset-not-working.md)
