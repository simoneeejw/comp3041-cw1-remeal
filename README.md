

### 4.2 Justification of Normative Ethical Theories
To evaluate the engineering choices in ReMeal, we use two complementary ethical theories: Kantian Deontology and Rule Utilitarianism.

Kantian deontology assesses actions based on duty and moral rules rather than end results. Kant's Categorical Imperative states that software engineers must treat users as rational human beings with rights, never merely as tools for company revenue. Building 'Roach Motel' account traps or withholding allergen lists directly violates the moral duty of honesty and respect for human autonomy. A policy of deceiving users cannot be turned into a universal rule without destroying public trust in software.

In contrast, Rule Utilitarianism focuses on consequences. It evaluates actions by asking what moral rules produce the greatest overall benefit for society. A software rule that mandates clear allergen warnings and HTTPS data protection produces far more long-term public welfare than an unprincipled rule allowing cost-cutting, which exposes thousands of everyday consumers to food poisoning and data leaks.

---

### 4.3 Analysis of Code Insufficiency and Value Tension (~160 words)
While the ACM/IEEE-CS Software Engineering Code provides valuable guidelines, it encounters critical limits when applied to real software products.

First, the Code suffers from internal clause tensions. For example, Clause 1.04 requires engineers to disclose any potential dangers to the public, such as food temperature risks or missing allergen labels. However, Clause 2.05 and Clause 2.09 command engineers to protect employer confidentiality and support their employer's business interests. If raising food safety alarms hurts the startup's reputation or reveals merchant problems, these two clauses clash directly. The Code cannot mechanically decide which duty wins.

Second, the Code suffers from the 'Wrong Addressee' problem. The Code is written for software engineers, but decisions such as strict 'no-refund' terms and legal liability disclaimers are dictated by business owners. When corporate managers demand these features to maintain cash flow, professional guidelines alone cannot force management compliance.

Broader ethical theories resolve these gaps. Under Rule Utilitarianism, preventing physical harm (food poisoning) creates vastly greater social good than protecting a startup's private profits, clearly establishing that public health must override company loyalty.

---

### 4.4 Plan and Roadmap for Part 2 Completion 
In Part 2, our group will build upon this foundation by conducting in-depth technical verification. We will inspect live network traffic using proxy tools to audit actual data transmissions, test user pickup experiences across local bakeries, and formulate concrete redesign recommendations to resolve the ethical and safety issues identified.
