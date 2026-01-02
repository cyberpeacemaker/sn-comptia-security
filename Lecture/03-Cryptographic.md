# 1. Algo
- Cryptanalysis, keyspace, key length, [RSA, ECC]
- hash (fixed length), collision, [SHA, MD5]
- cryptographic primitive [hash, symmetric cipher, asymmetric cipher]
- PKCS#1, [DSA, ECDSA]

# 2. PKI
- CA, digital certificate(public key), (X.509, IETF, PKCS)
- certificate signing request(CSR), **FQDN, CN, Subject alternative name(SAN)**, [CN, Distinguished name]
- revokem, suspend, Certificate revocation list(CRL), [published period < Validity Period], **Online Certificate Status Protocal(OSCP)**
- expiration, renewal, shelf-life, Key Management Interoperability Protocal(KMIP)
- key stored **tamper evident**, **cryptoprocessor** hardware [**TPM, HSM**], **secure enclave** (trusted execution environment TEE)
- [Escrow, M of N] EX: multiple key recovery agents

# 3. Solution
- Full-disk Encryption, self-encrypting drive **Volume**