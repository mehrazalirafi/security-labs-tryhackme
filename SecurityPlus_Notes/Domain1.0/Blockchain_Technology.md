# Blockchain and the Blockchain Process

## What is Blockchain?
- **A distributed ledger**: A shared system to record and track transactions
- **Maintained by everyone on the network**:
  - Every node has a full copy of the ledger
  - Any new transaction is recorded and propagated across the network
- **Practical Applications**:
  - Payment processing
  - Digital identification
  - Supply chain monitoring
  - Digital voting

---

## Blockchain Process (Step-by-Step)

### 1. Transaction Request
- A digital transaction is initiated (e.g., Bitcoin transfer, data backup, medical record logging, title transfer)

### 2. Broadcast to the Network
- The transaction is broadcast to all nodes (computers) in the decentralized blockchain network

### 3. Transaction Verification
- Each node checks the validity of the transaction

### 4. Add to Block
- The verified transaction is grouped with others into a **new block**

### 5. Hashing the Block
- A cryptographic hash is calculated from the block's data
- This ensures **integrity** — if any transaction is altered, the hash will no longer match

### 6. Block is Distributed
- The newly created block (with its hash) is sent to all participants on the network

### 7. Blockchain Update
- The block is **added to the end** of the existing blockchain
- All nodes update their copy of the blockchain

---

## Security of the Blockchain
- If **any block is altered**, the hash changes
- This causes a mismatch across the chain, and the altered block is **rejected**
- This ensures:
  - **Immutability** of records
  - **Tamper detection**
  - High level of **trust and integrity**

---

© 2023 Messer Studios, LLC  
Source: ProfessorMesser.com
