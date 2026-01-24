# 1. Concept
- [Confidentiality, Integrity, Availability] + Non-repudiation
- NIST [Identify, Protect, Detect, Respond, Recover]
- framework, legal compliance, gap analysis (third-party consultants),
- [subject, object], **IAM**[Identification, authentication, Authorization, Accounting]

# 2. Controls
- CISO, SOC, DevSecOps, [CIRT, CSIRT, CERT]
- category [Managerial, **Operational**, Technical(**file permissions**), Physical], 
- function type [Preventive, **Detective**, Corrective], [Directive, Deterrent, Compensating]
- **Managerial** controls provide oversight of the information system. Examples could include **risk identification or a tool** allowing the evaluation and selection of other security controls.
- **Operational** control involves people, such as **hiring security guards** and performing training programs.
- **Technical** controls are the implementation of a system, such as hardware, software, or firmware. For example, firewalls, antivirus software, and OS access control models are technical controls. For the server's security, segregating that equipment from normal employee access is important.
- **Physical** controls such as alarms, gateways, locks, lighting, and security cameras deter and detect access to premises.

- **Corrective** controls eliminate or reduce the impact of a security policy violation. A corrective control occurs after an attack. In this scenario, these actions aim to directly address the damage caused by the outage and improve the recovery process.
- **Preventive** controls eliminate or reduce the likelihood that an attack can succeed. The company implements this control to avert a potential incident from occurring.
- **Detective** controls may not prevent or deter access, but they will identify and record an attempted or successful intrusion. A **security camera** would be a type of detective control.

- **Directive** control enforces a rule of behavior, such as a policy, best practice standard, or standard operating procedure (SOP).
- **Compensating** controls are a substitute for a principal control, as recommended by a security standard, and afford the same (or better) level of protection. However, they use a different methodology or technology.
- **Deterrent** controls may not physically or logically prevent access, but they psychologically discourage an attacker from attempting an intrusion. Deterrent controls could include signs and warnings of legal penalties against trespass or intrusion.

| Control                          | Family      | Function   | Type         |
| -------------------------------- | ----------- | ---------- | ------------ |
| Data Encryption Policy           | Managerial  | Preventive | Directive    |
| Record-Level Encryption          | Technical   | Preventive | Preventive   |
| SOC Monitoring for SQL Injection | Operational | Detective  | Detective    |
| Security Cameras in Server Room  | Physical    | Detective  | Deterrent    |
| Isolating the DB After a Hack    | Technical   | Corrective | Compensating |


4 9 12