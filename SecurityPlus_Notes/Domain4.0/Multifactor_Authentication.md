# Multifactor Authentication (MFA) Summary

## 🔒 MFA Fundamentals
- **Purpose**: Verify identity using multiple independent factors  
- **Core Principle**:  
  > "Layered authentication reduces compromise risk"  
- **Key Benefit**:  
  Significantly enhances security beyond single-factor methods  

---

## 🧩 Authentication Factors
### 1. Something You Know
| **Type**       | **Characteristics**                     | **Examples**               |
|----------------|-----------------------------------------|----------------------------|
| Password       | Secret phrase/character string          | `P@ssw0rd!`               |
| PIN            | Numeric code (not stored on cards)      | 4-6 digit ATM codes        |
| Pattern        | Visual sequence only known to user      | Phone unlock patterns      |

### 2. Something You Have
| **Type**            | **Characteristics**                     | **Security Level** |
|---------------------|-----------------------------------------|--------------------|
| Smart Card          | Physical card + PIN required            | ⭐⭐⭐⭐           |
| USB Security Key    | Contains digital certificate            | ⭐⭐⭐⭐⭐          |
| Hardware Token      | Generates time-based codes (TOTP)       | ⭐⭐⭐⭐           |
| Phone (SMS/App)     | Receives codes via text/authenticator   | ⭐⭐⭐             |

### 3. Something You Are (Biometrics)
| **Type**       | **Implementation**                      | **Considerations**               |
|----------------|-----------------------------------------|----------------------------------|
| Fingerprint    | Mathematical representation stored     | Cannot be changed if compromised |
| Iris Scan      | Unique eye pattern analysis             | High accuracy but expensive      |
| Voice Print    | Voice pattern recognition               | Environmental sensitivity        |
| **Limitation**: Not foolproof - should combine with other factors  

### 4. Somewhere You Are (Location)
| **Method**            | **Technology**                          | **Limitations**               |
|-----------------------|-----------------------------------------|-------------------------------|
| IP Geolocation        | IPv4 address mapping                    | Inaccurate with VPNs/Proxies  |
| GPS Positioning       | Mobile device location services         | Requires signal reception     |
| Network Proximity     | Nearby WiFi/cellular networks           | Spoofing vulnerabilities      |
| **Note**: Rarely used alone due to reliability issues  

---

## 🔑 MFA Implementation Principles
1. **Layering**:  
   Combine factors from different categories (e.g., password + token)
2. **Adaptive Authentication**:  
   Adjust requirements based on risk context (location, device, behavior)
3. **Fallback Mechanisms**:  
   Include recovery options (backup codes, alternate methods)
4. **User Experience**:  
   Balance security with usability (e.g., biometrics on mobile)

---

## ⚠️ Security Considerations
- **SMS Vulnerabilities**: SIM swapping attacks
- **Biometric Limitations**: Cannot be changed if compromised
- **Token Security**: Physical protection required
- **Location Spoofing**: GPS/IP manipulation techniques
- **Best Practice**: Use phishing-resistant methods (FIDO2 security keys)

---

## 💡 Key Takeaways
1. MFA **significantly reduces** account takeover risks
2. **Phishing-resistant factors** (security keys) provide strongest protection
3. **Avoid SMS** where high security is required
4. Biometrics should be **supplemental** not primary factors
5. **Context-aware MFA** provides optimal security/usability balance
