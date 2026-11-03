## 3. Literature Review

### 3.1 Privacy and Surveillance in Comparable Systems
Research on comparable platforms suggests that data collection in food apps is extensive while consent is often weak. Blancaflor et al. (2024) combined policy analysis with a user survey to examine how far Filipino users understood the geolocation consent they gave GrabFood and Foodpanda, finding notable distrust, with 26.7% very concerned that shared data could enable government tracking. Woodcock (2020) shows that surveillance also reaches the workers who deliver the food. His workers’ survey at Deliveroo found riders tracked by GPS and timed at every stage but given only vague performance feedback and no means to dispute deactivations or the data held about them. Zhao and Li (2025) take a regulatory angle, simulating stricter European GDPR-style consent rules on a Hong Kong delivery platform. When couriers could opt out of behavioural profiling, more chose to work, raising peak-hour orders served by 25.5% and platform profit by 10.2%. However, their model assumes couriers make informed, freely given choices, an assumption Woodcock’s evidence of information asymmetry calls into question. Together, these studies indicate that consent in food platforms is frequently lacking, and that there exist decisions which benefits users and businesses alike.

### 3.2 Food Safety and Health Risks
Research on food platforms shows that safety information is frequently left to vendor discretion. Auditing 711 menus on iFood, Brazil’s largest delivery app, Vicentini et al. (2026) found ingredient lists were often incomplete and only one menu carried an allergen warning; focus-group participants struggled to identify hidden allergens and called for mandatory allergen fields. Similarly, Nahle, Thaivalappil and Young (2025) found that only 16% of 1,000 Toronto restaurants disclosed allergens online where disclosure was voluntary. Mossenson et al. (2024) audited donations to an Australian food bank and found 4% of food by weight was unsafe or unsuitable, largely potentially hazardous items such as meat and ready meals, with over a tonne donated just one day before its use-by date, responsibility over these risks is also often contested. Dai and Wu (2023) modelled platform–restaurant interactions and showed that profit-seeking platforms pass costs onto restaurants, encouraging opportunistic behaviour. They argued that regulators should hold platforms, not only vendors, accountable. Lee, Shin and Ham (2026) found that Korean delivery users who experienced food-related harm were less likely than non-users to complain to the seller and more likely to expect no resolution, and called for accessible redress channels on these platforms.

### 3.3 Relation to ReMeal
These findings map onto ReMeal. Its missing consent screen and obstructed deletion reflect the nominal privacy policies seen elsewhere. Meanwhile, its absent allergen fields, Surprise Boxes with contents hidden until collection, and self-description as an “agent” without dispute channels shift responsibilities onto merchants and consumers, avoiding calls for accountability.

---
## 4. SE Code Clauses Analysis

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

## References (Harvard format)

Agre, P.E. (1994) ‘Surveillance and capture: Two models of privacy’, *The Information Society*, 10(2), pp. 101–127.

Blancaflor, E., Delfin, I.Z.L., Molate, A., Penafiel, A.I., Villaluz, A. and Balan, A.K. (2024) ‘Ethical use of geolocation data: Privacy concerns in food delivery applications in the Philippines’, in *Proceedings of the 2024 7th International Conference on Information Management and Management Science (IMMS 2024)*. New York: ACM, pp. 346–353. doi:10.1145/3695652.3695683.

Dai, X. and Wu, L. (2023) ‘The impact of capitalist profit-seeking behavior by online food delivery platforms on food safety risks and government regulation strategies’, *Humanities and Social Sciences Communications*, 10, 126. doi:10.1057/s41599-023-01618-w.

Lee, H., Shin, Y. and Ham, S. (2026) ‘Consumer risk perceptions and remedial trust in the food delivery era’, *Discover Food*, 6, 260. doi:10.1007/s44187-026-00987-w.

Mossenson, S., Giglia, R., Pulker, C.E., Chester, M., McStay, C. and Pollard, C.M. (2024) ‘Evidence for initiating food safety policy: An assessment of the quality and safety of donated food at an Australian food bank’, *Food Policy*, 123, 102589.

Nahle, R., Thaivalappil, A. and Young, I. (2025) ‘Food allergy labeling and disclosure practices on restaurants’ online menus in Toronto, Canada’, *Journal of Food Protection*, 88(7), 100533. doi:10.1016/j.jfp.2025.100533.

Vicentini, M.S., Freiria, C.N., Estigarribia, M.N., Cardoso, G.B., Vargas, F.M., Stedefeldt, E., Zanin, L.M., Medeiros, C.O., Ginani, V.C., Rolim, P.M., Rocha, T.E.S., Ferris, I.M., Soon-Sinclair, J.M., Winnall, L.M. and da Cunha, D.T. (2026) ‘Food hypersensitivity communication across physical and online foodservice menus in Brazil: Fragmented regulation and consumer experiences in a mixed-methods study’, *Food Control*, 193, 112628. doi:10.1016/j.foodcont.2026.112628.

Woodcock, J. (2020) ‘The algorithmic panopticon at Deliveroo: Measurement, precarity, and the illusion of control’, *ephemera: theory & politics in organization*, 20(3), pp. 67–95.

Zhao, Z. and Li, S. (2025) ‘The impacts of data privacy regulations on food-delivery platforms’, *Transportation Research Part C: Emerging Technologies*, 181, 105364. doi:10.1016/j.trc.2025.105364.
