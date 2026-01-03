<samlp:Response xmlns:samlp="urn:oasis:names:tc:SAML:2.0:protocol"

xmlns:saml="urn:oasis:names:tc:SAML:2.0:assertion" ID="200" Version="2.0"

IssueInstant="2020-01-01T20:00:10Z " Destination="https://sp.foo/saml/acs" InResponseTo="100".

<saml:Issuer>https://idp.foo/sso</saml:Issuer>

<ds:Signature>...</ds:Signature>

<samlp:Status>...(success)...</samlp:Status>

<saml:Assertion xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

xmlns:xs="http://www.w3.org/2001/XMLSchema" ID="2000" Version="2.0"

IssueInstant="2020-01-01T20:00:09Z">

<saml:Issuer>https://idp.foo/sso</saml:Issuer>

<ds:Signature>...</ds:Signature>

<saml:Subject>...

<saml:Conditions>...

<saml:AudienceRestriction>...

<saml:AuthnStatement>...

<saml:AttributeStatement>

<saml:Attribute>...

<saml:Attribute>...

</saml:AttributeStatement>

</saml:Assertion>

</samlp:Response>