## DERO Blockchain White Paper (Draft Version)

## Table of Contents
* **SUMMARY**
* **CHALLENGES**
  * **IDENTITY AND KYC: VERIFICATION AND LIMITING MISUSE**
  * **VOTING: SAFE, SECURE, AND TRANSPARENT** 
  * **ASSET MANAGEMENT: PRIVATE AND AUDITABLE**
  * **2FA AUTHENTICATOR: SECURE PASSWORD MANAGEMENT AND ACCESS**
  * **INTEGRATION WITH TELECOM GATEWAYS**
* **DERO KEY FEATURES**
* **DERO VIRTUAL MACHINE**
* **ROADMAP**
* **SPECIFICATIONS**
* **DERO BLOCKCHAIN DEVELOPMENT**
* **DERO PROJECT COMPANY**

## SUMMARY

  DERO is a new, experimental blockchain technology written in Golang with a focus on enhanced Privacy and Smart Contracts while maintaining the transparency and security of the blockchain. The goal is to create a unique state of the art blockchain technology with enhanced Reliability, Privacy, Security, Usability, and Portability by bringing together some of the best proven technologies like CryptoNote Protocol and Smart Contracts, thereby allowing for the creation of Private Smart Contracts.

  Blockchain is an open, distributed ledger that can record transactions between two parties efficiently, and in a verifiable and permanent way.

  CryptoNote Protocol uses a distributed public ledger that records all balances and transactions of its in-built currency like Bitcoin. Unlike Bitcoin, CryptoNote's transactions cannot be followed through the blockchain in a way that reveals who sent or received coins. The only people with access to the whole set of data about a transaction are the sender or receiver of the transaction.

  A smart Contract is a protocol intended to facilitate, verify, and enforce the negotiation or execution of a digital contract. Smart contracts allow for direct contract execution without a third party. These transactions are trackable and irreversible. Smart contracts were first proposed by Nick Szabo in 1994.

  For more details about Blockchain, CryptoNote Protocol, and Smart Contract see:
  * https://en.wikipedia.org/wiki/Blockchain
  * https://en.wikipedia.org/wiki/CryptoNote
  * https://cryptonote.org/whitepaper.pdf
  * https://en.wikipedia.org/wiki/Smart_contract


Some brief examples of what a smart contract is capable of managing without third-party intervention include: access authorization to a physical object like a building or internet-of-things (IoT) devices, asset management, trading, ticket purchasing, or share distribution. In some instances, an individual or organization would prefer not to reveal the details of the transaction or contract (i.e. participants, amounts, and contract terms) to the rest of the world. Dero brings true privacy to smart contracts for the first time on any blockchain.


Truly private smart contracts are a unique feature offered by DERO that other projects to date (April.1/2018) do not offer. Dero accomplishes this by keeping all ascepts of the transaction, smart contract, and users details private on the original blockchain without the need to trust sensitive or otherwise private information to second layer or off-chain solutions.

## CHALLENGES
* **Identification and know-your-client (KYC):**\
    Having briefly touched upon the need for privacy on the blockchain we must also address the need for some degree of transparency in certain limited situations. Dero will allow thoroughly verified and publicly known certifying authorities to add their signature to individual wallets, and only for those who have applied. This signature serves as confirmation that your identity has been verified by a certifying authority such as a Government, Bank, telecom operator, Visa, Mastercard, or other organizations as required.
    
When a service provider require verification of your KYC details, similar to what we’ve seen with exchanges, the process can now be made as simple as using a wallet with the appropriate certification. The service provider, vendor, or payment gateway will only get to see a basic signature that confirms it is authorized to use their services. No personal details are available in these situations. Only certifying authorities will have personal information for individual wallets and only with those who have submitted an application.

In places where KYC compliance is at its most stringent levels, trades would not be possible without pre-authorization from the appropriate authorities. On an individual level, you can choose whom you certify your wallet with, at your discretion. Given the need for robust privacy and security, Dero’s blockchain has been designed to allow full integration of hardware wallets with biometric protection.

* **Voting using safe, secure, and transparent smart contracts:**\
    Any organization may use Dero’s blockchain for a safe, secure, and transparent voting process that also keeps the identities of all voters anonymous in the eyes of the public. This is achieved through a type of private “voting smart contract” that is only made possible today on Dero’s blockchain. Aside from Dero, current voting solutions to date operate on public ledgers with public smart contracts that don’t obfuscate or shroud your network traffic from identification. Some workaround solutions have been proposed, such as off-chain computations and second layer solutions; however, these solutions leave a number of fundamental flaws that needlessly complicate wide scale adoption of blockchain technology for private voting processes.
    
To register for the voting process, an individual must apply to the certifying authority with their public Dero address and documentation as required. In this instance, the authority in charge will validate your wallet and allow for one (1) vote or more as defined by the smart contract. The details of such a contract should theoretically be public, transparent, and fully available in any democratic process.

A smart contract of this nature will, of course, require flexibility, and the ability to be reprogrammed to suit the needs of any party that chooses to utilize a private smart voting contract. To that end, the Dero development team is working to keep as much flexibility in the system as possible. 

* **ASSET MANAGEMENT: PRIVATE AND AUDITABLE** \
    With Dero, assets can be recorded, distributed, or traded on the blockchain. Perhaps the most critical issue today facing asset management on the blockchain is privacy. Consider for a moment how assets are recorded today. Most assets are recorded in a private or centralized database like you may find at the Department of Motor Vehicles. Organizations or departments often have limited hours, cumbersome access to information policies, and substantial overhead costs. Bringing asset management to Dero’s blockchain will allow individuals unrestricted use of their own data, by allowing 24/7 access to anything they have stored on Dero’s blockchain while simultaneously offering unparalleled privacy.
    
Any individual or organization that choose Dero’s blockchain for asset management will benefit from the highest levels of privacy by utilizing the CryptoNote protocol and complete SSL implementation across the entire network, among other critical features. For audits or tax purposes, all you have to do is provide a simple and convenient viewkey that will list all relevant history from the wallet. This view key can be easily programmed into tax software to reduce cost and human error, while insuring accuracy. It’s important to note that all details of wallets are entirely hidden from the rest of the network. As such, it is the individual wallet holders responsibility to make their relevant tax information known as required. 

* **2-Factor authentication: Secure password management and access:**\
	Dero plans to integrate one-time password (OTP) authenticators and passphrases. Subaddresses could be used as the username to keep public address information private, and, if required, a OTP password will appear in the wallet. An application programming interface (API) and software development kits (SDK) will be freely distributed to service providers to facilitate integration of their existing infrastructure with the Dero blockchain. This will create a significantly more secure environment for the users on a particular service or platform.
	
* **Integration with telecom gateways**\
	Dero’s blockchain was built in such a way as to allow integration with telecommunication gateways, to send and receive short message service (SMS a.k.a. text) messages. Once your wallet is certified with a telecom operator, you will be able to send text messages that take advantage of the privacy features from the CryptoNote protocol. For example, ring CT signatures are just one of many features used to hide your data. One-time password verified SMS data will be relayed to the appropriate wallet and held completely privately for only the recipient.
	
## DERO KEY FEATURES

- **CryptoNote privacy:** CryptoNote currencies use a distributed public ledger that records all balances and transactions of its in-built currency like Bitcoin. Unlike Bitcoin, CryptoNote’s transactions cannot be followed through the blockchain in a way that reveals who sent or received coins. Dero utilizes all aspects of the CryptoNote protocol’s privacy features in its new blockchain technology to protect the identities of all parties involved in a transaction.
- **Smart contracts:** A smart contract is a digital self-executing contract that is capable of enforcing the terms laid out by all participants in the contract. The goal of smart contracts is to significantly increase contract security while simultaneously reducing costs associated with traditional contracts.
- **Atomic swaps:** Atomic swaps make the exchange of one cryptocurrency for another possible without the need for a trusted third-party. To prevent one party from failing to send their coins, atomic swaps use something called hash time-locked contacts (HTLCs) to enable a trustless trading system.
- **Mobile and offline wallets:** As with any currency, multiple forms of storage and varying degrees of financial availability are required. Dero is bringing a complete spectrum of wallet storage options to users by providing solutions that range from mobile wallets on mobile devices to offline 2FA (Two Factor Authentication) biometric identification protected hardware wallets.
- **Lightweight wallet:** Instead of downloading the entire blockchain, a lightweight wallet connects to randomly selected decentralized nodes to utilize the data stored there. This dramatically reduces the amount of data required to transact on the network while maintaining the security of your private keys on your device, not the node the device is connected to.
- **Subaddresses:** This technology allows for the creation of additional public addresses for one wallet. This allows a user to differentiate where payments are coming from while preventing privacy loss caused by linking transactions to one public address.
- **Escrow services on the blockchain:** Escrow services may take advantage of Dero’s blockchain technology by using it as the trusted third party. In this instance, a financial instrument or an asset is recorded on the blockchain and held until the appropriate instructions are given, or contractual obligations have been fulfilled.
- **Address signing and certifying:** Comparable to the way a certifying authority may issue a passport or driver’s license, an individual may receive digital signatures and pre-authorizations that are stored on their individual wallet on the blockchain.
- **Voting:** Through the use of blockchain technology any group or organization may create a safe and transparent voting system that also maintains complete anonymity among voters.

## DERO VIRTUAL MACHINE

​    Smart Contracts on the DERO blockchain will run in a DERO Virtual Machine (DVM). DVM is a Turing complete 256-bit Virtual Machine runtime environment for DERO Smart Contracts with CryptoNote Protocol Privacy and additional modifications.
​    DVM is unique in its ability to execute Smart Contracts while maintaining the privacy and fungiblity of the identities involved in the Smart Contracts. DVM will support the Golang language for writing Smart Contracts with the possibility of Solidity in the future.
​    DVM is in the development phase, and several other features and optimizations are planned which may be added in the future.

## ROADMAP
* DERO Blockchain full Activation: Q1 2018. - Completed ahead of schedule
* GUI Wallets, Sub Addresses, Atomic Swap, Smart Contract Testing: Q2 2018.
* Smart Contract support on chain. Q3 2018. 
* Strategic market expansion.  

## SPECIFICATIONS
* PoW algorithm: CryptoNight
* Max supply: 18.4 million for first 8 years, Infinite ~157,000 DERO/year
* Block reward: Smoothly varying
* Block time: 120 seconds
* Difficulty: Retargets at every block
* Ticker: DERO

## DERO BLOCKCHAIN DEVELOPMENT
   DERO takes a utilitarian approach to development. From real world examples, use cases, community suggestions, it strives to develop a blockchain that can be deployed and widely used for practical applications. DERO welcomes everyone to participate in shaping its roadmap and technology by contributing directly to code development, proposing new ideas, or submitting comments and suggestions.
  DERO total premine 2 million. Premine will be locked to various heights for the next 4 years, and a portion of the premine will be used for various community activities. 
 * Total premine 2 million DERO
 * First 1 million locked for 4 years.
 * Second 0.5 million reserved for various activities. Unlocked at 10%, 20%, 30%, 40% respectively in years 1-4.
 * Third 0.5 million for development. Unlocked at 20%, 20%, 30%, 30% respectively in years 1-4.

## Areas we will strive to refine constantly in the future
* Reducing energy consumption of the network 
* Reducing block times 
* Increasing transactions per second 
* Reducing blockchain sync times and resource utilization
* Reducing blockchain size
* Increasing reliability and security of the network
* Secure hardware wallet with biometrics.
* Regular audits and updates of the core cryptography to negate the benefits of quantum computations.

## DERO PROJECT COMPANY :
   Plan to incorporate a company which will market, develop, maintain, and expand DERO.
Company would hire more developers, expand the marketing team, add advisors, and would be representing DERO to the world.

	


**Draft Version, This document will be updated based on community inputs.**
