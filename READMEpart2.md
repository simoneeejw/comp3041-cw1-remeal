## 1.3 Who Is Affected by ReMeal
  The users of ReMeal consist primarily of four groups. The first group is budget-conscious students and hungry users, 
who mainly purchase discounted "Surprise Boxes" before closing time to save on meal costs. The second group is small 
bakery owners, who use the platform to sell their unsold food at a discount for clearance. The third group is delivery 
workers, who are responsible for picking up the orders from the stores within specific time windows and delivering them 
to the users. The fourth group is the software developers and maintenance staff, who build and update the online trading system
that connects merchants with consumers.

## 2.1 Testing Method

  To collect first-hand evidence, our group downloaded ReMeal and conducted a complete UX walkthrough. Starting from phone number
registration, we tested the entire flow from browsing stores and adding "Surprise Boxes" to checkout. Additionally, we thoroughly 
reviewed the app's Terms of Use and the Google Play Data Safety section. Finally, we systematically analysed real user reviews on 
the app store to cross-verify the issues identified during our hands-on testing.
 
## 2.4 Findings for Issue 3

  Regarding the third issue, we observed that the registration barrier is extremely low, supporting quick 1-click sign-ups via Google and Apple.
However, there is no "Delete Account" option in the Settings page. When building the system, engineers deliberately coded a frictionless
registration process to rapidly acquire users, while intentionally omitting automated account-deletion APIs and UI buttons. Consequently, users
must manually email customer support to request deletion. This engineering decision creates a "wide-in, hard-out" barrier, severely restricting users' 
digital autonomy and constituting a classic "Roach Motel" dark pattern.

## 2.5 Findings for Issue 4: No Refunds & Unfair Blame Shifting

  Funds are locked immediately after checkout, and the system provides no after-sales or refund entry points. Based on our review of the in-app review system,
the only negative feedback consists of complaints about the packaged food being too simple or the side dishes not matching the user's taste; 
the reviews are overwhelmingly 4-5 stars, with almost no disputes regarding spoiled food or refunds. This absence is not a coincidence but a deliberate
concealment of dispute resolution channels. Furthermore, the platform defines itself merely as an "agent" providing matchmaking services, attempting
to shift the food quality risks entirely onto the merchants and consumers.
