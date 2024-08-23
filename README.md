- # POPKORN: Zero-Knowledge MultiSig for Mina Protocol

## Project Background

POPKORN is an innovative MultiSig wallet solution built on Mina, leveraging O1js, to streamline how users interact with blockchain applications. By utilizing zero-knowledge proofs for authentication and transaction authorization, POPKORN creates a faster, more user-friendly MultiSig experience with fewer pop-ups, while maintaining robust security.

## Proposal Overview

### Problem

Traditional MultiSig wallets often require complex coordination and multiple interactions, creating a barrier to adoption and efficient use. This complexity can deter users from leveraging the enhanced security benefits of MultiSig solutions.

### Solution

POPKORN introduces a streamlined approach to MultiSig wallets on Mina:

1. Faster proof generation for each transaction by multiple users
2. Efficient MultiSig dApp to aggregate and verify proofs
3. Significantly reducing the number of pop-ups and user interactions

### Grant Scope

We will develop an MVP MultiSig dApp implementing the POPKORN solution, capable of receiving and sending tokens after collecting the required number of proofs from authorized users.

### Ecosystem Impact

1. User Experience: Simplifying MultiSig interactions to encourage wider adoption of secure wallet solutions on Mina.
2. Developer Tools: Providing an easier framework for integrating MultiSig functionality into Mina dApps.
3. Ecosystem Growth: Attracting new users to Mina through user-friendly, secure wallet options.

### Audience

1. Existing Mina users seeking more efficient MultiSig solutions
2. New users looking for secure, easy-to-use wallet options on Mina

## Architecture & Design

### Detailed Design

//add the drawing

1. Wallet Connection and Multisig Setup:
   - Users connect their standard Mina wallet to the POPKORN dApp
   - Within the dApp, users can create a new multisig wallet
   - Setup includes specifying signers, confirmation threshold, hierarchy and other parameters

2. Multisig Wallet Creation:
   - Users define the number of signers and required confirmations
   - Network fee (1 MINA) for new account setup is covered by the deployer
   - 
3. Transaction Proposal and Signing:
   - Any signer can propose a transaction from the multisig wallet
   - Other signers are notified and can review the transaction
   - POPKORN generates zero-knowledge proofs for signer approval, replacing traditional signatures

4. Proof Aggregation and Execution:
   - The multisig contract receives and verifies proofs from authorized signers
   - Proofs are aggregated until the required threshold is met
   - Once the threshold is reached, the transaction is automatically executed

5. Wallet Management:
   - Users can modify the number of signers and required confirmations after creation
   - The dApp provides a user-friendly interface for managing the multisig wallet

### Vision

To establish POPKORN as the go-to MultiSig solution on Mina, we aim to:

1. Provide a seamless, user-friendly interface for creating and managing multisig wallets
2. Minimize user interactions required for secure MultiSig transactions while maintaining robust security
3. Support various authentication scenarios

### Production Timeline

We target a production-ready MultiSig dApp within 3 months of funding.

## Budget & Milestones

### Milestones

1. Develop core proof generation and verification logic
2. Implement MultiSig dApp smart contract
3. Create user-friendly wallet interface
4. Integrate proof aggregation and verification
5. Conduct testing and security audits

### Project Timeline

3 months

### Budget Requested

30,000 MINA

### Budget Breakdown

- Core POPKORN functionality: 12,000 MINA
- MultiSig dApp development: 12,000 MINA
- User interface and wallet integration: 3,000 MINA
- Testing, auditing, and documentation: 3,000 MINA

### Wallet Address

B62qrNc1QFe8Sr1ioGaanuDQ9aLvcpcNVpcwMDBtTmaXXH72cLtStBV
B62qjfxgtyYsjpfKZGQ4AACvH96uVY5TAwjkW1DubWfwP2nbEqjrrSy

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

1. Potential vulnerabilities in proof handling
2. User adoption challenges
3. Compatibility with existing Mina infrastructure

### Mitigations

1. Rigorous security audits and leveraging Mina's native security features
2. Focus on intuitive UX design and user education
3. Close collaboration with Mina community for seamless integration

## Additional Considerations

- Explore synergies with other Mina ecosystem projects
- Prioritize scalability for growing user base
