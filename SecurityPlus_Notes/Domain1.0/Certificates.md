# Digital Certificates - Summary Notes

## 1. Digital Certificates
- A **public key certificate** binds a public key with a digital signature.
- Includes details about the key holder.
- A **digital signature adds trust**:
  - PKI uses Certificate Authorities (CAs) for additional trust.
  - A Web of Trust uses signatures from other users.
- **Certificate creation** can be built into the OS:
  - Windows Domain Services
  - 3rd-party options

## 2. What’s in a Digital Certificate?
- Uses **X.509** standard format.
- Contains:
  - Serial number
  - Version
  - Signature algorithm
  - Issuer
  - Name of cert holder
  - Public key
  - Extensions

## 3. Root of Trust
- Trust is foundational to IT security.
- Trust can come from:
  - Certificate Authorities
  - Secure hardware (HSM, Secure Enclave)

## 4. Certificate Authorities (CAs)
- Browsers trust certain CAs by default.
- A website's certificate is trusted if signed by a trusted CA.
- Trust is verified in real-time during the SSL/TLS handshake.

## 5. Third-party Certificate Authorities
- Built into all browsers.
- Certificates can be purchased.
- CA performs **identity verification** before issuing a certificate.

## 6. Certificate Signing Requests (CSR)
- Steps:
  1. Create a key pair (public/private)
  2. Generate CSR (includes public key and identity info)
  3. CA validates and signs the cert with its private key

## 7. Private Certificate Authorities
- You can act as your own CA.
- Useful for internal web servers.
- Tools: Windows Certificate Services, OpenCA

## 8. Self-Signed Certificates
- Used internally; doesn't need a public CA.
- Steps:
  - Build internal CA
  - Install internal CA's root certificate on devices

## 9. Wildcard Certificates
- Use **Subject Alternative Name (SAN)** extension in X.509.
- Allows one certificate to cover multiple subdomains:
  - `*.example.com` -> `www.example.com`, `mail.example.com`

## 10. Certificate Revocation
- **CRL (Certificate Revocation List)** is maintained by the CA.
- Reasons for revocation:
  - Key compromise (e.g., Heartbleed CVE-2014-0160)
  - Decommissioned servers
- CRL URLs can be found in the certificate's details.

## 11. OCSP and Stapling
- **OCSP (Online Certificate Status Protocol)**:
  - Browser queries CA for certificate status via HTTP.
  - More efficient than downloading a full CRL.
- **OCSP Stapling**:
  - Server "staples" OCSP response into SSL/TLS handshake.
  - Digitally signed by CA
  - Offloads traffic from CA

## 12. Browser Support for OCSP
- Modern browsers support OCSP.
- Some older browsers (e.g., old Internet Explorer) don't.
- Some browsers support OCSP but don’t enforce revocation checks.
