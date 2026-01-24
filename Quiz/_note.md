Security Assertion Markup Language(**SAML**), Simple Object Access Protocal(**SOAP**)
Simple Authentication and Security Layer** (**SASL**) (LDAP)
secure access service edge (**SASE**) (ZTA, Cloud Access Security Broker (**CASB**), Secure Web Gateway (**SWG**))
 
# Authentication & Authorization
- Identity and Access Management (**IAM**) [Identification, authentication, Authorization, Accounting]
- Public Key Infrasturcture X.509 (**PKI**), Certificate Authorities (**CA**), Certificate revocation list(**CRL**), Certificate Signing Request (**CSR**)
- Windows: [Local Security Authority Subsystem Service (**LSASS**), Security Account Manager (**SAM**)], network [legacy **NT LAN Manager(NTLM)** > Kerberos (**TGT** ask for **TGS**)], Directory Service **Lightweight Directory Access Protocal(LDAP) standard x.500**
- (AWS implement) **Security Assertion Markup Language(SAML)** using HTTP/S and **Simple Object Access Protocal(SOAP)**
- Representational State Transfer (**REST**) < implemented using < **Open Authorization (OAuth)**, OpenID Connect (**OIDC**), **JSON Web Token (JWT)**
- passwordless [Hardware Security Module (**HSM**), Secure Enclave], hase-based message authentication code (**HMAC**), **Fast Identity Onlie (FIDO) Alliance** Universal 2nd Factor (U2F), FIDO2 [WebAuthn(your pc tpm), CTAP2(external tpm)], key fob token generator

# Enterprise Architecure
- Chief Information Security Officer (**CISO**), Security Openration Center (**SOC**) [Security Information and Event Management (**SIEM**), Security Orchestration, Automation, and Response (**SOAR**), Computer Security Incident Response Team (**CSIRT**)], 
- [Managerial, **Operational**, Technical(**file permissions**), Physical],
- Secure Administrative Workstations (**SAWs**), Jump Server, Out-of-Band (**OOB**)
- VPN [PPTP(Deprecated), SSL/TLS, **IPSec** [AH, ESP, SA, IKE, IKEv2]]
- **802.1x (Port-based Network Access)** < [Extensible Authenitcation Protocal(**EAP**), Remote Authentication Dia-In User Service(**RADIUS**)], Wired Equivalent Privacy (**WEP**) < WiFi Protected Access (**WPA**)
- Cloud [Zero Trusted Architecture (**ZTA**), Software-Defined Wide Area Network (**SD-WAN**), secure access service edge (**SASE**)]
- Managed Power Distribution Unit (**PDU**), hot plug power supply unit (PSU), uninterruptible power supply(**UPS**), 
- **closed-circuit** > open-circuit alarm

---

# Threat & Prevent
- supply chain, managed service provider(**MSP**)
- **[rooting(android), jailbreaking(Apple)], sideloading**
- **BT [bluejacking, blussnarfing, blueBorne]**
- CIS Benchmark, Security Technical Implementation Guides (STIGs) < Defense Information Systems Agency (DISA) 
- automate tool: **puppet**, chef, ansible, microsoft group policy
- **LDAPS (port 636), [Simple Authentication and Security Layer** (**SASL**), `STARTTLS`, **preferred mechanism** for AD]
- Simple Network Management Protocal (**SNMP**) [monitor, agents]
- [**SFTP**, FTPS{Explicit (**FTPES**), Implicit(FTPS > **suprsingly tricky to configure firewall**)}]
- {Simple Mail Transfer Protoca (**SMTP**)l, [Post Office Protocal (**POP**), Internet Message Access Protocal (**IMAP**)]}
- [Sender Policy Framework (**SPF**), Domain Keys Indentified Mail(**DKIM**), Domain-based Message Authentication, Reporting & Conformance(**DMARC**)], **Secure/Multipurpose Internet Mail Extesions (S/MIME)** > 11.1.7 Video
- Dota loss prevention **DLP**, Regulation [GDPR, HIPPA, PCI DSS]
- DNS Service [Berkley Internet Name Domain(BIND), Internet Systems Consortium(isc.org)], **DNSSEC**
- **Secure cookies** ['Secure', 'HttpOnly' (**XSS**), 'SameSite' (**CSRF**)], **Nonces (use only once)** 
- Full-disk/Volume Encryption, [DBMS, SQL] > [datebase(page)-level (transparent data encryption), record-level(Cell/Column)]

---

# Detecet & Response
- IR Cycle **[Preparation, Detecion, Analysis, containment, eradication, recovery, lesson learned]**
- [**Netflow** > IP Flow Information Export (**IPFOX**) IETF standard], **flow collector**(metadata and statistic about traffic), **network monitor**(CPU/Memory load, dus, net utilization, Simple Network Management Protocal (**SNMP**)), **heartbeat message**(availability), [Deep Packet Inspection (**DPI**), Packet Capture (**PCAP**)]**
- Security Content Automation Protocal (**SCAP**), Open Vulnerability and assessment language (**OVAL**), Extensible Configuration Chekclist Description format (**XCCDF**)

---

# Governance & Risk management & Compliance
- [Managerial, **Operational**, Technical, Physical], [Preventive, **Detective**, Corrective], [Directive, Deterrent, Compensating] Control
- Depolyment Model {**Brying your Own Device BYOD, Corporate-Owned Business Only COBO, Corporate-owned Personally-Enabled COPE, Choose Your Own Device CYOD**}
- Data [**owner, controller, processor, custodian**]
- Security Awareness Program
- Incident Response Plan (**IRP**), Disaster Recovery Plan (**DRP**)
- Single Loss Expectance (**SLE**), Annualized Rate of Occurrence (**ARO**), Annualized Loss Expectance (**ALE**)
- risk response {**avoid, accept, mitigate, transfer**}, risk registry, **key risk indicator (KRI)**, **risk owner**
- [Recovery Point Objective (**RPO**), maximum tolerable downtime (**MTD**), recovery time objective (**RTO**), work recovery time (**WRT**)], [mean time between failures (**MTBF**), mean time to repair (**MTTR**)]
- initial agreement [memorandum of understanding (**MOU**), nondisclosure agreement, memoradum of agreement(**MOA**), business parternship agreement (**BPA**), master service agreement (**MSA**)], detailed agreement [service-level agreement (**SLA**), statement of work (**SOW**)/ work order], rule of engagement (**RoE**)
- **Regulatory Assessment**: External, Laws; **Compliance Assessment**: Internal, rule, policy