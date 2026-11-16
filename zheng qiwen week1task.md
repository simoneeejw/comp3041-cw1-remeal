## 2.2 Account Lifecycle & Friction Audit

  The registration process of ReMeal is designed for zero friction: users can enter via 1-click Google/Apple sign-in or a "Guest" mode without any barriers. 
However, this hides a classic "Consent by action" dark pattern—the UI omits any checkbox for Terms & Conditions, implying consent simply by clicking "Sign In,"
thereby stripping users of their right to review policies. Furthermore, the platform employs a Delayed Registration strategy, forcefully triggering an OTP phone
verification at checkout. Although a subtle "Verify later" link exists at the bottom, the prominent red WhatsApp support prompt indicates that the true goal is 
not security, but maximizing the harvesting of sensitive PII (Personal Identifiable Information) like phone numbers.

  In stark contrast to the frictionless entry, the exit path is deliberately obscured. The "Delete Account" button is buried at the bottom of the profile page,
and its confirmation modal is highly misleading: the text merely states "You will no longer be able to login" without any mention of data erasure. Moreover,
the "Yes" button is colored in the exact same bright green as the "Sign In" button, visually inducing accidental clicks. Most egregiously, when asked how to 
delete an account, customer support explicitly equated "Logout" with "Delete Account," directly concealing the fact that no data is actually erased. This proves
the button is merely a deceptive deactivation design.

   The T&Cs reveal a severe power imbalance. Clause 2.2 requires users to "send us an email requesting" account deletion, artificially creating high friction.
Conversely, Clause 14.0 grants the platform unilateral power to terminate accounts "for any reason" without warning. This design—where the platform can ban 
users with zero friction at any time, while users must go through a cumbersome application process to exit—exposes the nature of draconian terms and directly 
contradicts both the "fake deletion" button in the app and the dismissive support responses. 

 The designs above directly violate Google Play's mandatory "User Data" policy, which explicitly requires apps with account creation to provide both an "in-app 
deletion path" and an "external web link for deletion requests." The audit reveals that ReMeal not only fails to provide any external web link on its Play Store
listing, but its in-app path is also just a deceptive deactivation button. 

  Based on the four-step audit, ReMeal utilizes dark patterns to construct a "Roach Motel" cycle—easy to enter, impossible to exit. 

### Evidence

| Figure | Description |
| :--- | :--- |
| **2.2.1 – 2.2.3** | Pre-Registration Onboarding Pages |
| **2.2.4** | Extremely Low-Friction Registration Page |
| **2.2.5** | OTP Verification Page |
| **2.2.6** | Misleading "Fake Deletion" Modal |
| **2.2.7** | Dismissive Customer Support Chat |
| **2.2.8 – 2.2.9** | Terms & Conditions Clauses (2.2 and 14.0) |
| **2.2.10** | Compliance Comparison: Google Play Policy vs. ReMeal’s Violation |