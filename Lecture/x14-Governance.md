# 1. Policy
- General Data Protection Regulation (**GDPR** EU), California Consumer Privacy Act (**CCPA**)
- "Newly created accounts with simple or default passwords are an easily exploitable backdoor"
- MITRE ATT&CK framework, NIST Special Publication 800-61
- offboarding > credential changed immediatly
- **stakeholder, board, committee, regulatory agency**
- regulatory requirements are reason for adopting standard
- **ISO/IEC 27001 standard provide ISMS framework, NIST 800-63, Health Insurance Portability and Accoutability Act (HIPAA), Payment Cart Industry Data Security Standard (PCI DSS), Fedaral Information Processin Standards (FIPS)**
- [**policy, process, standard, guidline**]
- **{standard:implementaion, policy:business practice}**
- [healthcare, financial, telecommunication, energy, education, gorvenment]
- [**owner, controller, processor, custodian**]
- Owner(e.g., Head of Finance) decides that a file is "Top Secret," **Custodian** (e.g., IT Admin) actually applies the encryption and sets the folder permissions.
- Under General Data Protection Regulation (**GDPR**), the **Controller** is the "brain" (deciding the purpose), **Processor** is the "hands" (doing the work, like a cloud provider).
To illustrate how these roles function together, let's look at a **Healthcare App** scenario (like an app that tracks patient vitals). This shows how the hierarchy works in a high-stakes environment.
* **Owner Fails:** Data is under-classified (e.g., "Public" instead of "Private"), leading to a leak.
* **Controller Fails:** Data is collected without consent, leading to a massive fine.
* **Custodian Fails:** A technical bug leaves a database open to the internet.
* **Processor Fails:** The cloud provider has a hardware breach that affects millions of clients.


# 2. Change
- policy, procedure, technology must changed often
- **Fit-gap**
- **Acceptable use Policy (UAP)**
- **mainatenance window**
- Software Development Life Cycle (SDLC)

q2, q12, q16, q18