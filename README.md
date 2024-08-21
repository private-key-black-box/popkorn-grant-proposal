# POPKORN Growth Grants Proposal

## Title

POPKORN: Proof Of Private Key Ownership Requiring Nothing - A Revolutionary Approach to Blockchain Authentication

## Project Background

POPKORN is an innovative wallet solution built on Mina, leveraging Protokit, to revolutionize how users interact with blockchain applications. By utilizing zero-knowledge proofs for authentication and transaction authorization, POPKORN eliminates the need for complex seed phrase management and simplifies digital signatures.

The platform addresses the critical issue of private key management, which has long been a significant barrier to mainstream blockchain adoption. POPKORN's approach not only enhances security but also dramatically improves user experience, making blockchain interactions as simple and intuitive as traditional web applications.

## Proposal Overview

### Problem

Traditional blockchain interactions require users to manage private keys and sign transactions, creating a significant barrier to entry and increasing the risk of fund loss due to mismanagement. This complexity hinders widespread adoption and limits the potential of blockchain technology.

### Solution

POPKORN introduces an innovative approach using zero-knowledge proofs for user authentication and transaction authorization without exposing or requiring direct management of private keys. Key features include:

1. Generation of proofs for each transaction
2. Use of zkApp accounts with locked permissions set to proofOnly
3. Leveraging native nonce of zkApp accounts to prevent proof reuse
4. Transformation of passwords to public keys for enhanced security

### Grant scope

For this grant proposal we intent to make a MVP dApp that implements the POPKORN solution. It will be a multisig dApp that can receive tokens and send tokens after receiving X amount of proofs (instead of signatures). 

### Ecosystem Impact

1. User Adoption: By simplifying the user experience, POPKORN lowers the entry barrier for new users in the Mina ecosystem, potentially driving widespread adoption.
2. Developer Adoption: Easier dApp integration encourages more developers to build on the Mina platform.
3. Innovation Catalyst: POPKORN introduces new design patterns for secure, user-friendly blockchain interactions, spurring further innovation in the space.

### Audience

1. Non-technical users seeking simpler blockchain interactions
2. Developers aiming to integrate user-friendly authentication methods into their dApps
3. Wallet providers interested in offering enhanced security and usability features

## Architecture & Design

### Detailed Design/Architecture

1. Proof Generation and Usage:
   - Utilize zkApp accounts with locked permissions set to proofOnly
   - Generate a keypair within the circuit, discarding the private key after proof creation
   - Proofs are generated and used immediately, without storage, enhancing security
   - Use the native nonce of the zkApp account (with incrementNonce set to true) to prevent reuse

2. Authentication Flow:
   - User initiates a transaction
   - POPKORN generates a one-time proof
   - The proof is immediately used for authentication and discarded
   - Each transaction requires a new proof, ensuring unique authentication for every action

3. Integration with Existing Systems:
   - Implement as a feature within the Multisig MVP dApp.

4. Security Measures:
   - Employ nonces and timestamps to ensure proof uniqueness
   - Store public key derived from user password, rather than password hash
   - Implement JWT-like mechanisms for enhanced security

### Vision

Our vision is to make POPKORN the standard for blockchain authentication and transaction authorization. We aim to:

1. Develop a comprehensive SDK for easy integration into dApps
2. Expand POPKORN's capabilities to support various authentication scenarios and complex transaction types
   
### Existing Work

Our team previously built a POPKORN prototype at ZkHack Krakow, winning first prize from Mina. This prototype demonstrated the core concept of using zero-knowledge proofs for authentication.
- [Github link](https://github.com/private-key-black-box/frontend)


### Production Timeline

We aim for a production-ready version within 3 months of funding.

## Budget & Milestones

### Milestones

1. Complete core proof generation and verification logic
2. Implement zkApp account with proofOnly permissions
5. Implement transaction handling through zkApp transaction for Multisig dApp

### Project Timeline

3 months

### Budget Requested

30,000 MINA

### Budget Breakdown

- Core POPKORN functionality (proof generation, use and discard flow): 15,000 MINA
- Multisig dApp: 15,000 MINA

### Wallet Address

[MINA Wallet address to be added]

## Team Info

### Team Members

- arjanjohan - [Github](https://github.com/arjanjohan) - [Twitter](https://twitter.com/arjanjohan)
- Kacper [Github](https://github.com/cleanerzkp) - [Twitter](https://twitter.com/0xcleaner)

### Team Achievements

- First prize at ZkHack Krakow for POPKORN prototype
- Both Kacper and arjanjohan are EthGlobal finalists (EthGlobal Brussels)

### Proposer Github

[Popkorn Github link](https://github.com/private-key-black-box/frontend)

### Proposer Experience

Our team has demonstrated expertise in zero-knowledge proofs and blockchain development, as evidenced by our win at ZkHack Krakow with the POPKORN prototype.

## Risks & Mitigations

### Risks

1. Potential vulnerabilities in the proof generation or verification process
2. Resistance from users or developers accustomed to traditional key management
3. Future compatibility issues with existing dApps and wallets

### Mitigations

1. Conduct thorough security audits and implement a bug bounty program
2. Develop comprehensive educational materials and provide excellent developer support
3. Work closely with the Mina community to ensure seamless integration and backwards compatibility where possible
      
## Additional Considerations
- We will explore similarities and potential synergies with zkLogin from Sui
- The design's invasiveness and impact on existing zkApps requires further ecosystem discussions
- Supporting HD keys is currently out of scope, focusing instead on simplifying user experience through proof-based authentication
- We plan to host workshops and hackathons to encourage developer adoption and gather feedback for continuous improvement
