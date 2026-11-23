# 3.4 Issue 4: Risk Allocation in the Terms and Conditions and the Resulting Accountability Gap

Clauses 6.10, 7.2.2 and 9.2 of ReMeal's Terms and Conditions transfer to users and vendors risks that the platform itself partly generates. This is inconsistent with Clauses 3.01 and 1.02 of the Software Engineering Code of Ethics (SE Code). Primary accountability rests with ReMeal management while their software engineers bear a shared professional accountability, and partner vendors a narrower, operational share.

ReMeal Clause 6.10 limits their responsibility for refunds and disputes to cases that they deem "reasonable and justifiable", a standard that is determined only by them. This pattern can also be found in ReMeal Clause 7.2.2, where they place all risk of deterioration on the user using the term "attributable to you", an undefined ambigous phrase which places the responsibility of inspection solely to the user. ReMeal Clause 9.2 then meantions that "all liability" is given to the user, with the only solution given to be discontinued use. Furthermore, on instances where a delayed notification or an incorrect pick-up window caused by the system leads to late collection ReMeal Clause 7.2.2 permits ReMeal to attribute the delay to the user. Together, these provisions set out a narrow forward-looking responsibility while largely excluding backward-looking accountability and legal liability.

There are also clear breaches of SE Clauses as defined by IEEE within ReMeal. SE Clause 1.02 requires engineers to moderate stakeholder interests with the public good. In spite of this, situations where food is held at unsafe room temperatures is secluded by ReMeal Clause 9.2, putting organisational interest before public welfare. SE Clause 3.01 states that significant tradeoffs should be "clear to and accepted by" clients and available to users. ReMeal central tradeoff is providing access to low-cost food in turn for bearing all risk to the users. However, this message is only clear within legal text and undisclosed anywhere else within the application.

Therefore, the apparent forward-looking responsibility and the hidden backward-looking accountability and legal liability of each stakeholder can be summarised as below, along with the degree of which it is held.

- **ReMeal management** is responsible for designing fair terms and disclosing tradeoffs, and is accountable for refund and dispute outcomes. However, it seeks to exclude liability under Clause 9.2, subject to applicable law.
- **Software engineers** are responsible for building accurate timestamps, notifications and refund logic, and are accountable for explaining system-induced delays. They generally bear no personal liability.
- **Partner vendors** are responsible for maintaining food safety and honouring pick-up windows, and are accountable for responding to defects reported at collection (Clause 7.2.2). Their liability is limited to product-quality obligations.

Birsch's five criteria allow a closer assessment:

- **Causation.** Management set the terms and refund policy; engineers implement the rules and generate the logs that decide whether a delay is "attributable"; vendors control food condition. Each is a significant causal factor, illustrating the "problem of many hands".
- **Knowledge.** Management authored the terms. Engineers understand the system's failure modes, and Birsch holds that deliberately remaining ignorant of potential harm does not remove responsibility.
- **Intent.** There is no evidence of malice. However, as with Uber's sensor reduction (Lecture 5), accepting user harm to contain costs was a deliberate tradeoff.
- **Capacity.** Management holds full decision-making authority; senior engineers can recognise and escalate the risk, while junior developers working to specification have reduced capacity.
- **Freedom.** Commercial pressure reduces engineers' accountability and shifts it towards management. Vendors' freedom is constrained by ReMeal's platform terms.

Management therefore satisfies all five criteria most fully and is the principal accountable party. Engineers satisfy Causation, Knowledge and Capacity, and hold a duty under Clause 3.01 to raise the tradeoff. Vendors are accountable only for food safety within their control.

ReMeal may argue that it is an intermediary marketplace rather than a food producer, that limitation clauses are standard commercial practice, and that users control their own punctuality. Birsch also acknowledges that errors are unavoidable in complex software, so not every failure is blameworthy.

This justifies holding users responsible for genuine lateness. However, it does not justify ReMeal acting as sole arbiter of causation, using data only it controls, while excluding all review. Clause 9.2 applies only "to the extent permitted by law", implicitly conceding it may not be fully enforceable. Consistent with the SE Code, the appropriate remedy is transparency rather than silent exclusion. ReMeal should:

1. Define "attributable" delay with reference to system logs that users can access.
2. Disclose the allocation of risk clearly at checkout.
3. Ensure engineers escalate system-induced delays to management, as Clause 3.01 requires.