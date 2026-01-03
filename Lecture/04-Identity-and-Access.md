# 1. Autehntication
- biometric metric: [fakse rejection, false acceptance, crossover error, throughput, failure to enroll]
- hard autehntication token [cert-based, OTP(timestamp, HMAC), Fast Identity Onlie (FIDO) Universal 2nd Factor (U2F)], **key fob token generator**
- Attestation

# 2. Authorization
- [Discretionary, Mandatory(write up, read down)] Access Control, Access control list (ACL)
- [role, **attribute**]-based access control
- rule-based access control [RBACm, ABACm, MAC, **nondiscreationary**], User Access Control (UAC) (**prompted when require priviledge**, sudo) > Contional Access
- 4.2.6 **demo video**
- privileged access management (PAM), **secure administrative workstaion (SAW)**, **zero standing privilege (ZSP)** [temporary elevation, password vaulting/brokering, ephemeral credential]

# 3. Identity management
- Windows Authentication [Local/Interactive logon (**Local Security Subsystem Service LSASS**), network [Kerberosm, legacy **NT LAN Manager(NTLM)**], remote (not directly in local network)]
- Directory Service (most) based on **Lightweight Directory Access Protocal(LDAP)**
- Ticket Granting Ticket (TGT) > (ask for) > Ticket Granting Service (TGS), TGS Session Key, **Note that the user's password (or hash) is never transmitted through the network for security.**, [service session key, service ticket]
- Service Provider > (redirect) > Identity Provider (IdP)
- (AWS implement) **Security Assertion Markup Language(SAML)** using HTTP/S and **Simple Object Access Protocal(SOAP)**
- Representational State Transfer (REST) < implemented using < Open Authorization (OAuth) , **JSON Web Token (JWT)**

**2-step !== multi-factor**

q5, q8, q11, q14, q15, q17, q19