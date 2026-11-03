# ReMeal – Software Engineering Code of Ethics Analysis

## 4.1 Mapping the Issues to the SE Code

Below, each issue found in ReMeal is mapped to clauses from the ACM/IEEE-CS Software Engineering Code. For each issue, the exact wording of the clause is quoted, along with what the engineers could have done differently. All evidence was collected first-hand on Android in November 2026.

### Issue 1: Allergen and freshness information

The listings do not have a section for allergens, and Terms clause 5.3 states that ReMeal *"is not obligated to provide ingredient information or allergen information"*. This means the information depends on what each vendor decides to write. For example, a cake listing mentions almonds, but the Gula Cakery Mystery Bag only says its contents depend on *"the day's surplus"*.

This goes against **clause 1.03**, which asks engineers to have *"a well-founded belief it is safe"*, since users with allergies cannot know what they are buying. **Clause 1.04** also requires disclosing *"potential danger to the user"*. Adding a required allergen field, with "may contain" as the default for mystery bags, would solve both.

### Issue 2: Data transmission and sharing

ReMeal's Play Store page states that data *"isn't transferred over a secure connection"*. The decompiled manifest also sets `usesCleartextTraffic` to `true`, which allows unencrypted HTTP even though Android blocks it by default. On top of this, the Privacy Policy allows sharing with *"credit bureaus, alternative credit scoring agencies"* and advertisers, and the app includes Firebase Analytics and an advertising-ID permission. No consent screen appears in the app.

Turning cleartext traffic back on goes against **clause 3.12**, which asks engineers to *"respect the privacy"* of users. **Clause 3.13** limits data use to *"ways properly authorized"*; however, consent that is only assumed from using the app is weak authorisation for this kind of sharing.

### Issue 3: Inaccurate documentation and consent by default

ReMeal describes account deletion in three different ways. Terms clause 2.2 says users must send an email, the Play Store says users can submit a request, and the app itself has a button. This button's dialog only says *"You will no longer be able to login"* and does not say whether data is erased. The Privacy Policy also says users can limit targeted ads *"through our ReMeal app"*; however, the app only has two notification toggles, both switched on by default.

**Clause 6.07** states that engineers should *"be accurate in stating the characteristics of software"*, and **clause 1.06** says to *"avoid deception in all statements"*. The software partly meets the Code, since deletion works better than the documents say. However, keeping user-facing descriptions in line with the actual app is still part of the engineer's job.

### Issue 4: Payment and dispute handling

Terms clause 6.10 states that ReMeal takes responsibility for refunds only *"strictly if reasonable and justifiable"*. The app has a general support chat, but there is no dispute or refund option linked to orders. Terms clause 7.2.2 also requires users to report defects before leaving the vendor, even though mystery-bag contents are unknown until collection.

**Clause 3.01** asks that tradeoffs like this be *"available for consideration by the user"*, yet this one only appears in the Terms. Placing this risk on users also does not align with **clause 1.02**, which asks engineers to *"moderate the interests"* of the employer and the users. The refund policy itself is mostly a business decision outside the engineer's control, which is discussed in Section 4.3.

### Table 1: Summary of issues mapped to SE Code clauses

| # | Issue | Observable engineering decision | Clauses | Status |
|---|-------|---------------------------------|---------|--------|
| 1 | Allergen and freshness information | No dedicated allergen or ingredient field; information depends on vendor free text | 1.03, 1.04 | Breaks |
| 2 | Data transmission and sharing | Cleartext HTTP enabled in manifest; analytics and ad-ID SDKs; broad sharing; no in-app consent screen | 3.12, 3.13 | Breaks |
| 3 | Inaccurate documentation, consent by default | Three conflicting deletion descriptions; promised ad setting absent; marketing on by default | 6.07, 1.06 | Partly meets |
| 4 | Payment and dispute handling | Refund duty in Terms 6.10 but only generic support chat; inspection burden on user (7.2.2) | 3.01, 1.02 | Partly meets; partly outside engineer control |
