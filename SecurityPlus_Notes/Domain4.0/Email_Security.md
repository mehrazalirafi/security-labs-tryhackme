# Email Security Fundamentals

## 1. Email Security Challenges
- **Protocol Vulnerabilities**: SMTP lacks built-in authentication
- **Spoofing Prevalence**: Easy to forge sender addresses (check your spam folder)
- **Verification Difficulty**: No native way to confirm sender legitimacy
- **Solution**: DNS-based authentication protocols (SPF, DKIM, DMARC)

## 2. Mail Gateway Implementation
- **Position**: Email gatekeeper (screened subnet or cloud-based)
- **Functions**:
  - Evaluates inbound email sources
  - Blocks suspicious messages pre-delivery
  - Deployment options: On-premise or cloud-based

## 3. Email Authentication Protocols
| Protocol | Purpose                          | Implementation                     | Record Example                          |
|----------|----------------------------------|------------------------------------|-----------------------------------------|
| **SPF**  | Authorize sending servers        | DNS TXT record                     | `"v=spf1 include:mailgun.org ~all"`     |
| **DKIM** | Verify message integrity          | Digital signatures + DNS public key | `"v=DKIM1; p=MIGfMA0G...IDAQAB"`        |
| **DMARC**| Define failure handling           | DNS policy + reporting             | `"v=DMARC1; p=quarantine; rua=reports@example.com"` |

## 4. Protocol Functions
### SPF (Sender Policy Framework)
- Maintains authorized sender list in DNS
- Receiving servers validate originating IP
- Prevents unauthorized servers from sending domain emails

### DKIM (DomainKeys Identified Mail)
- Sending server adds digital signature to headers
- Public key in DNS enables signature verification
- Ensures message integrity (not altered in transit)

### DMARC (Domain-based Message Authentication)
- **Policy Enforcement**:
  - `p=none`: Monitor only
  - `p=quarantine`: Send to spam
  - `p=reject`: Block entirely
- **Reporting**:
  - Aggregate reports (rua)
  - Forensic reports (ruf)
  - Compliance monitoring (e.g., 89% compliance)

## 5. Implementation Process
1. **SPF Configuration**:
   - Identify authorized sending servers
   - Create DNS TXT record with include directives
2. **DKIM Setup**:
   - Generate public/private key pair
   - Configure mail server to sign outgoing messages
   - Publish public key in DNS
3. **DMARC Deployment**:
   - Define failure policies
   - Set up reporting addresses
   - Monitor and adjust policies based on reports

## Key Takeaways
1. **Layered Defense**: Combine SPF, DKIM, and DMARC
2. **DNS is Key**: Authentication relies on properly configured DNS records
3. **Monitor Reports**: DMARC reveals spoofing attempts and configuration issues
4. **Gradual Rollout**: Start with `p=none` policy before tightening restrictions
5. **Gateway Enforcement**: Mail gateways apply policies before delivery
