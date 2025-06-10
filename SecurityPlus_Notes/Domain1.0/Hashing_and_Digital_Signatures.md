# Data Protection and Cryptographic Concepts

## Obfuscation
- **Definition**: Making information unclear or harder to interpret.
- **Key points**:
  - Not impossible to understand—just requires knowing how to read it.
  - Often hides data **in plain sight**.
  - **Example**: Steganography (hiding data in images).

## Steganography
- **Definition**: Greek for “concealed writing”; hiding data within other files or formats.
- **Properties**:
  - Message is invisible but exists.
  - Uses **covertext**: the visible document/file that contains hidden data.

### Common Techniques
- **Network-based**: Embed messages in TCP packets.
- **Images**: Hide data in image pixels.
- **Watermarks**: Invisible yellow dots in printed documents (e.g., machine identification codes).
- **Audio/Video Steganography**:
  - Audio: Embed data in audio tracks.
  - Video: Use image steganography across video frames.

## Tokenization
- **Definition**: Replacing sensitive data with a non-sensitive placeholder (token).
- **Key facts**:
  - Common in credit card processing.
  - Tokens are **not mathematically related** to original data (unlike encryption).
  - Example: Tap-to-pay systems use one-time tokens validated by a remote token service.

## Data Masking
- **Definition**: Hiding parts of data to protect sensitive info (like PII).
- **Details**:
  - May only obscure data from view, not remove it.
  - Based on permissions and view control.
  - Techniques include substituting, encrypting, masking out, shuffling.

## Hashes
- **Purpose**: Represent data as a fixed-length string (digest/fingerprint).
- **Characteristics**:
  - One-way function: Cannot retrieve original data.
  - Used for **password storage**, **file integrity**, and **digital signatures**.
  - Any minor change in input drastically changes the hash (avalanche effect).

### Hash Collisions
- **Definition**: Two different inputs generating the same hash.
- **MD5 Warning**: Known for collisions—**not secure** for important use.

### Practical Uses
- **File integrity**: Compare hash of downloaded files.
- **Password storage**: Store hashed & salted versions only.

## Password Salting
- **Definition**: Random data added to passwords before hashing.
- **Why it matters**:
  - Each user gets a unique salt.
  - Prevents attacks using rainbow tables.
  - Slows down brute-force attacks.

## Digital Signatures
- **Used for**:
  - **Integrity**: Ensures message wasn't altered.
  - **Authentication**: Confirms sender identity.
  - **Non-repudiation**: Proves message origin can’t be denied.

### Process
1. Hash the original message.
2. Encrypt the hash with sender’s **private key** → digital signature.
3. Receiver decrypts with sender’s **public key**.
4. Re-hash the message and compare to validate.
