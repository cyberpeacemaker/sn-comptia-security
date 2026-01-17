# Protocal
- (SSL)/TLS, cipher suites: ECDHE-RSA-AES128-GCM-SHA256 > TLS_AES_256_GCM_SHA384 
- "Hash key derivation function (HKDF) is the mechanism by which the shared secret established by D-H key agreement is used to derive symmetric session keys."
- Lightweight Directory Access Protocal (LDAP) (**Vulnerable**),  ([AD > Directory Service, LDAP > Communication Protocal]), ([LDAP > searching, Kerberos > Authentication])
- **LDAPS (port 636), [Simple Authentication and Security Layer** (**SASL**), `STARTTLS`, **preferred mechanism** for AD]
- Simple Network Management Protocal (**SNMP**) [monitor, agents]
- [**SFTP**, FTPS{Explicit (**FTPES**), Implicit(FTPS > **suprsingly tricky to configure firewall**)}]
- {Simple Mail Transfer Protoca (**SMTP**)l, [Post Office Protocal (**POP**), Internet Message Access Protocal (**IMAP**)]}
- [Sender Policy Framework (**SPF**), Domain Keys Indentified Mail(**DKIM**), Domain-based Message Authentication, Reporting & Conformance(**DMARC**)], **Secure/Multipurpose Internet Mail Extesions (S/MIME)** > 11.1.7 Video
- Dota loss prevention **DLP**, Regulation [GDPR, HIPPA, PCI DSS]
- DNS Service [Berkley Internet Name Domain(BIND), Internet Systems Consortium(isc.org)], **DNSSEC**- 
- **BT [bluejacking, blussnarfing, blueBorne]**
| Protocol | Port | Encryption Type | Uses STARTTLS Command? |
|----------|------|-----------------|------------------------|
| SMTP     | 587  | Explicit        | Yes                    |
| SMTPS    | 465  | Implicit        | No (Secure by default) |
| LDAP     | 389  | Explicit        | Yes                    |
| LDAPS    | 636  | Implicit        | No (Secure by default) |
| SASL     | N/A  | Auth Framework  | No, but it runs inside the TLS tunnel |


# App
- Context Aware Authentication
- Microsoft SDL, Open Worldwide Application Security Project **(OWASP)** [Software Assurance Maturity Model, Framework, Top10]
- **Secure cookies** ['Secure', 'HttpOnly' (**XSS**), 'SameSite' (**CSRF**)], **Nonces (use only once)** 
- Structured exception handler (SEH), **custome error handler**, both clint and server validation

q2, q3, q8, q10