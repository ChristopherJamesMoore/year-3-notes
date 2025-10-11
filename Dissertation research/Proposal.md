End-to-End Pharmaceutical Supply Chain Transparency System.

## Scope

- **Track medicines from start to finish**  
  Build a system to follow the journey of medicines from when they are made to when they reach pharmacies or customers.

- **Use of hyperledger blockchain**  
  Use Hyperledger (such as Fabric) to create a private blockchain. This allows trusted partners to securely share and access data.

- **Create records for each batch**  
  For every batch of medicine, the system will create a digital record that includes:
  - A batch ID  
  - A time and date stamp  
  - A digital signature from the manufacturer (stored as a hash)  
  - Updates at each point in the supply chain (e.g. production, shipping, delivery)

- **Use of hybrid storage**  
  The system will separate how data is stored to make it scalable and compliant:
  - **On the blockchain (on-chain):** Store important data like batch ID, timestamp, and hashed values that cannot be changed  
  - **Outside the blockchain (off-chain):** Store full documents and sensitive data in a secure database, so it can be deleted or updated if needed (e.g. for GDPR compliance)

- **Prevent fake medicines**  
  Help stop fake or unsafe medicines by making sure each batch can be verified and traced through the official supply chain.

- **Let consumers and pharmacists check medicines**  
  Allow end users to check a medicine’s authenticity by scanning a QR code that links to the batch record.

- **Follow data protection rules (e.g., GDPR)**  
  - Keep personal or sensitive data off the blockchain  
  - Make sure off-chain data can be deleted or changed to meet data protection laws

- **Control access for different stakeholders**  
  Manage who can see or add data, using Hyperledger's permission features. Roles include:
  - Manufacturers  
  - Distributors  
  - Regulators  
  - Pharmacists

- **Make records easy to audit**  
  Provide a clear log of all events and changes to help with regulatory checks and internal audits.

- **Make the system scalable and cost-effective**  
  Reduce costs and improve speed by only storing key data on the blockchain and keeping large files off-chain.

---

## Key deliverables

- **1. Requirements specification document**  
  A clear list of system features, technical needs, and compliance requirements based on research and stakeholder input.

- **2. System architecture design**  
  A detailed design showing how the blockchain, databases, user interfaces, and APIs will work together.

- **3. Blockchain network (Hyperledger)**  
  A working permissioned blockchain network with nodes for different partners (e.g. manufacturers, regulators).

- **4. Hybrid storage system**  
  A working storage setup that keeps sensitive data off-chain and secure, while linking it to hashed records on-chain.

- **5. Web and potentially mobile interfaces**  
  - A dashboard for supply chain partners  
  - A verification tool for consumers (QR code scanning)

- **6. Security and compliance report**  
  An assessment showing how the system protects data and meets GDPR and other regulatory standards.

- **7. Testing and QA reports**  
  Full testing results including functional, security, and performance testing.

- **8. Final deployment and training materials**  
  Support for going live with the system, including guides and training for end users.