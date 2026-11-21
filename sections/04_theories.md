## 4. Application of Ethical Theories

### 4.1 Why the SE Code Cannot Resolve ReMeal's Core Dilemmas

While the ACM/IEEE-CS Software Engineering Code pinpoints specific engineering failures in ReMeal—such as omitting mandatory allergen fields (Clauses 1.03, 1.04) and enabling cleartext HTTP (Clause 3.12)—it runs out in three distinct ways when applied to the platform's underlying dilemmas.

First, the Code exhibits **internal clause conflict**. Clause 1.04 requires engineers to disclose actual or potential dangers to users and the public, which applies to unlabelled food allergens and unencrypted traffic. However, Clauses 2.05 and 2.09 obligate engineers to protect employer confidentiality and avoid actions adverse to the employer's business interests unless a higher ethical concern overrides them. Because the Code provides no mechanical procedure for weighing public health risk against a startup's commercial survival, engineers must look beyond the Code to justify which duty takes precedence.

Second, ReMeal exposes the **wrong addressee** problem. The SE Code binds software engineers, not startup founders or legal teams. Core ethical failures—including Terms Section 5.3 (disclaiming allergen obligation), Terms Sections 6.10 and 7.2.2 (restricting refunds and requiring pre-departure inspection), and Privacy Policy Section 3C (sharing personal data with credit bureaus and advertisers)—are commercial policies dictated by management rather than unilateral coding errors.

Third, the Code is **silent on indirect stakeholders**. Its duties centre on direct users, clients, and employers, offering limited guidance when ReMeal's unlabelled mystery bags endanger non-users—such as an allergic housemate or family member who consumes food purchased by a student user.

---

### 4.2 Comparative Analysis: Mystery-Bag Allergen Omission and Risk-Shifting

To resolve these gaps, we apply **Kantian Deontology** and **Rule Utilitarianism** to ReMeal's central dilemma: *whether omitting mandatory allergen/freshness fields and locking payments without automated dispute channels is ethically defensible to keep merchant onboarding frictionless and surplus food affordable.*

*(Note for Week 2: Integrate Member 1's Klang Valley mystery-bag field audit photos and Member 4's checkout lock-in evidence here.)*

#### Kantian Deontology
Kantian deontology judges actions by moral duty and universalizability rather than commercial outcomes. Under Kant's Universal Law formulation, if every surplus-food platform omitted allergen disclosures and disclaimed all liability (Terms 5.3 and 9.2), consumers could never rationally trust digital food marketplaces, collapsing the very institution of food commerce into a contradiction. Under the Respect for Persons formulation, designing a checkout flow that hides safety-critical ingredients and blocks post-collection redress treats budget-conscious students merely as a means to clear vendor inventory and protect startup margins, stripping them of informed autonomy. From a Kantian standpoint, omitting allergen fields and redress channels is categorically impermissible, regardless of how much food waste the platform saves.

#### Rule Utilitarianism
Rule Utilitarianism evaluates which general engineering rule maximises long-term net social welfare. A permissive rule—allowing voluntary vendor free-text and blanket liability disclaimers—generates short-term utility through fast vendor onboarding, reduced food waste, and discounted meals. However, empirical evidence from comparable food platforms demonstrates that voluntary disclosure leaves the vast majority of menus without allergen warnings (Vicentini et al., 2026; Nahle, Thaivalappil and Young, 2025) and exposes consumers to unsafe, near-expiry items (Mossenson et al., 2024). Even a small probability of severe anaphylaxis or food poisoning imposes catastrophic harm that outweighs minor convenience gains, while unaddressed disputes erode long-term user trust (Lee, Shin and Ham, 2026). Conversely, a rule mandating structured allergen tags, "may contain" defaults, and a brief dispute window adds seconds to merchant listing time while preventing severe physical harm and sustaining platform adoption (cf. Zhao and Li, 2025).

#### Comparative Insight: Convergence and Divergence
Both theories converge in rejecting ReMeal's current design, demonstrating that public safety must override employer loyalty (resolving the Clause 1.04 vs. 2.09 conflict) and that management's legal disclaimers do not excuse ethical negligence. However, the two frameworks diverge on **acceptable uncertainty**. A strict Kantian rejects any mystery-bag workflow that prevents fully informed consent about exact ingredients, even if no user is ever harmed. Rule Utilitarianism, by contrast, permits the *mystery-bag* model to continue—preserving its environmental and affordability benefits—provided mandatory "may contain" allergen flags, preparation timestamps, and accessible refund channels reduce expected harm to a negligible level.

| Analytical Lens | Verdict on ReMeal's Current Design | Core Justification | Key Insight Added |
| :--- | :--- | :--- | :--- |
| **SE Code (v5.2)** | Breaks 1.03, 1.04; partly breaks 1.02, 3.01 | Focuses on concrete engineering actions (missing fields, locked checkout) | Runs out on management policies (wrong addressee), 1.04 vs. 2.09 clash, and indirect victims |
| **Kantian Deontology** | Categorically Impermissible | Violates universalizability and treats buyers as a mere means without informed consent | Establishes non-negotiable rights to safety disclosure and honesty regardless of profit or food-waste goals |
| **Rule Utilitarianism** | Net Harmful (Fails Utility Test) | Severe health risks (anaphylaxis/spoilage) outweigh minor vendor onboarding convenience | Justifies *regulated* mystery bags ("may contain" defaults + redress) that balance food-waste benefits with safety |