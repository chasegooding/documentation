### Certificate Options
Certificate options change based on the option selected in **Type**.

{{< truetable >}}
| Setting | Description |
|---------|-------------|
| **Signing Certificate Authority** | (Required) Select a previously imported or created CA. Displays when **Type** is set to **Intermediate CA**. |
| **Key Type** | (Required) Select the key type from the dropdown list of options. Default is **RSA**. Select **EC** for EC curve certificates. See [Why is elliptic curve cryptography not widely used, compared to RSA?](https://crypto.stackexchange.com/questions/1190/why-is-elliptic-curve-cryptography-not-widely-used-compared-to-rsa) for more information about key types. |
| **Key Length** | (Required) Select the number of bits in the key used by the cryptographic algorithm from the dropdown list. Options are **1024**, **2048** or **4096**. For security reasons, a minimum key length of 2048 is recommended. |
| **Digest Algorithm** | (Required) Select the cryptographic algorithm to use from the dropdown list of options. Only change the default **SHA256** if the organization requires a different algorithm. |
| **Lifetime** | (Required) Enter the lifetime of the CA specified in days. |
{{< /truetable >}}

### Certificate Subject

{{< truetable >}}
| Setting | Description |
|---------|-------------|
| **Country** | (Required) Select the country of the organization from the dropdown list. |
| **State** | (Required) Enter the state or province of the organization. |
| **Locality** |(Required) Enter the location of the organization. For example, the city. |
| **Organization** | (Required) Enter the name of the company or organization. |
| **Organizational Unit** | Organizational unit of the entity. |
| **Email** | (Required) Enter the email address of the person responsible for the CA. |
| **Common Name** | Enter the [fully-qualified hostname (FQDN)](https://kb.iu.edu/d/aiuv) of the system. This name must be unique within a certificate chain. |
| **Subject Alternate Names** | (Required) Enter additional domains to secure for multi-domain support. Separate domains by pressing <kbd>Enter</kbd>. For example, if the primary domain is example.com, entering www.example.com secures both addresses. |
{{< /truetable >}}

### Basic Constraints

{{< truetable >}}
| Setting | Description |
|---------|-------------|
| **Enabled** | Select to activate this certificate extension. |
| **Path Length** | Enter the number of non-self-issued intermediate certificates that can follow this certificate in a valid certification path. Entering **0** allows a single additional certificate to follow in the certificate path. Cannot be less than 0. |
| **Basic Constraints Config** | Select the basic constraints extension that identifies whether the subject of the certificate is a CA and the maximum depth of valid certification paths that include this certificate. See [RFC 3280, section 4.2.1.10](https://www.ietf.org/rfc/rfc3280.txt) for more information. |
{{< /truetable >}}

### Authority Key Identifier

{{< truetable >}}
| Setting | Description |
|---------|-------------|
| **Enabled** | Select to activate this certificate extension. |
| **Authority Key Config** | Select the authority key identifier extension that provides a means of identifying the public key corresponding to the private key used to sign a certificate. This extension is used where an issuer has multiple signing keys (either due to multiple concurrent key pairs or due to changeover). The identification can be based on either the key identifier (the subject key identifier in the issuer certificate) or on the issuer name and serial number. See [RFC 3280, section 4.2.1.1](https://www.ietf.org/rfc/rfc3280.txt) for more information. |
{{< /truetable >}}

### Extended Key Usage

{{< truetable >}}
| Setting | Description |
|---------|-------------|
| **Enabled** | Select to activate this certificate extension. |
| **Usages** | Select the options that identify the purpose for this public key from the dropdown list. Is used for end entity certificates. Multiple usages can be selected. Do not mark this extension critical when the **Usage** is **ANY_EXTENDED_KEY_USAGE**. Using both **Extended Key Usage** and **Key Usage** extensions requires that the purpose of the certificate is consistent with both extensions. See [RFC 3280, section 4.2.1.13](https://www.ietf.org/rfc/rfc3280.txt) for more details. |
| **Critical Extension** | Select to identify this extension as critical for the certificate. The certificate-using system must recognize critical extensions, or it will reject the certificate. The certificate-using system can ignore non-critical extensions and still approve the certificate. |
{{< /truetable >}}

### Key Usage

{{< truetable >}}
| Setting | Description |
|---------|-------------|
| **Enabled** | Select to activate this certificate extension. |
| **Key Usage Config** | Select the key usage extension that defines the purpose (e.g., encipherment, signature, certificate signing) of the key contained in the certificate. The usage restriction might be employed when a key that could be used for more than one operation is to be restricted. For example, when an RSA key should be used only to verify signatures on objects other than public key certificates and CRLs, the Digital Signature bits would be asserted. Likewise, when an RSA key should be used only for key management, the Key Encipherment bit would be asserted. See [RFC 3280, section 4.2.1.3](https://www.ietf.org/rfc/rfc3280.txt) for more information. |
{{< /truetable >}}
