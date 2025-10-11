### Hyperledger
Hyperledger is an open-source blockchain framework, set of standards, guidelines, and tools to build blockchains and related applications for use across various industries. Hyperledger is equip with all the required components to create enterprise-ready blockchain systems.

Unlike Ethereum, which is a public blockchain for transferring value and developing applications onto, whereas Hyperledger is a platform that gives developers modularised options for building blockchains or distributed ledgers that fit their specific needs.

### Blockchain layers

##### Blockchain architecture

<b>Hardware</b>
This is the ground floor of blockchain - The physical infrastructure. Think of servers, data centres, and mining rigs. They provide the computational power and storage that blockchain networks need to operate.
<u>Key components</u>:
- Nodes: Computers participating in the network
- Mining equipment: For proof-of-work (PoW) blockchains like Bitcoin
- Cloud infrastructure: Used by modern blockchains for storage
<b>Data</b>
Here is where the magic of blockchain happens: Transactions are grouped into blocks and recorded in an immutable, transparent ledger. Distributed ledger-based technologies help record transaction data and cryptographic hashes in a tamper-proof manner.
<u>Key components</u>:
- Blocks: Contain transaction data, timestamps, and hashes
- Merkle trees: Ensure efficient data validation
- Public ledger: A transparent record of all transactions
<b>Network</b>
The network is like a blockchain's nervous system. It enables communication between nodes in a blockchain and connects participants in the blockchain ecosystem, ensuring everyone is on the same page. The network is responsible for propagating transactions and ensuring synchronisation.
<u>Key components</u>:
- Peer-to-peer (P2P) protocols: Ensure decentralised communication
- Nodes: Verify and relay data across the network
- Protocol: Handles how transaction data is distributed
<b>Consensus mechanisms</b>
Ever wondered how blockchains ensure everyone agrees on the same data? That's where consensus mechanisms come in. It establishes an agreement among nodes on the validity of transactions and the state of the ledger, ensuring trust and preventing double-spending.
<u>Key components</u>:
- Consensus algorithm: Proof-of-work (Bitcoin), proof-of-stake (Ethereum post-merge), delegated proof-of-stake (Tron), etc...
- Validators: Nodes that confirm transactions and add them to the blockchain
- Fault tolerance: Ensures the network remains operational despite malicious nodes
<b>Application</b>
This is they layer you interact with - whether it's buying a non-fungible token (NFT), swapping tokens or playing a blockchain game. It is the topmost layer where end-users interact with the blockchain through decentralised applications (DApps) and smart contracts. It provides functionality and real-world use cases for blockchain.
<u>Key components</u>:
- Smart contracts: Self-executing programs on the blockchain
- DApps: Decentralised applications like Uniswap, Axie infinity and OpenSea
- Wallets: Interfaces for users to interact with blockchain networks.

#### Blockchain layers

<b>Layer 0: Foundation infrastructure</b>
Without layer 0, blockchains would remain isolated, unable to share data or resources. Layer 0 protocols allow cross-chain interoperability between L1 and L2 projects. Without this base layer, blockchains would operate in isolation, limiting their potential.

Polkadot and Cosmos are prime examples of layer 0 solutions. Polkadot's relay chain allows multiple blockchains to communicate and share information seamlessly, while Cosmos uses its Tendermint protocol to connect various blockchains in its ecosystem.

<b>Layer 1: Base blockchain protocol</b>
L1 is the backbone of blockchain technology, where the main network operates. This layer manages essential functions such as transaction validation, consensus mechanisms and data storage. It focuses on decentralisation, security, and immutability.

Bitcoin, Ethereum and Solana are the most well-known L1 blockchains. Bitcoin employs a proof-of-work (PoW) consensus to secure its network, while Ethereum enables smart contracts and DApps to run directly on its blockchain, offering programmability via proof-of-stake (PoS).

Solana, a later entrant, is designed with a proof-of-history (PoH) consensus mechanism and does not have the layered structure as described below.

<b>Limitations of L1 and the rise of L2</b>
L1 blockchains like Bitcoin and Ethereum have formed the core of blockchain technology since their inception. They are responsible for ensuring security, decentralisation, and immutability.

However, as blockchain adoption surged in the last decade, significant limitations of L1 became apparent, highlighting the need for improvements in scalability and efficiency. Some problems with L1's:
- Scalability bottlenecks: L1 blockchains process transactions on a global decentralised network. While this ensures security, it comes at the cost of speed. For instance, Bitcoin processes only about seven transactions per second (TPS), and Ethereum averages around 15-30 TPS, far below what is required for mass adoption
- High transaction costs: Limited scalability often leads to network congestion, driving up transaction fees during peak usage. This was especially evident during Ethereum's NFT boom in 2017, where gas fees soared to hundreds of dollars per transaction
- Energy-intensive mechanisms: Bitcoin's PoW system consumes significant energy, raising environment concerns and making it less sustainable. Although Bitcoin miners have increasingly adopted renewable energy sources, this shift highlights the industry's commitment to sustainability and reducing its environment footprint
- Limited customisation flexibility: L1 blockchains operate on rigid protocols, making it difficult to introduce changes or optimise performance without risking decentralisation or security

<b>Layer 2: Scaling solutions</b>
L2 built on top of L1 to address its scalability challenges. It introduces solutions to improve transaction speed and reduce costs without compromising the security of the base layer.

These solutions process transactions off-chain or through <font color="blue">side-chains</font>, lightening the load on L1. For example, the lighting network is an L2 solution for Bitcoin that facilitates faster and cheaper micro-transactions. 

Blew are the main types of L2 solutions typically seen on Ethereum L1:
- Rollups: Rollups process transactions off-chain and then batch them onto a single transaction on L1
	- Optimistic rollups: Assume transactions are valid by default and only verify them if there is a dispute, e.g., Arbitrum optimism
	- Zero-knowledge (ZK) rollups: Use cryptographic proofs to validate transactions, ensuring faster finality, e.g., ZKsync Starknet
- Plasma: Plasma chains are smaller blockchains that offload transactions from the main chain. They periodically settle the final state to L1, ensuring security. Plasma is particularly suited for micro-transactions
- Validiums: Validiums are similar to ZK-rollups but store transaction data off-chain, improving scalability even further. They are ideal for applications requiring high throughput and minimal on-chain storage
- State channel: State channels allow participants to conduct multiple transactions off-chain, with only the initial and final state recorded on the blockchain. This is commonly used for micropayments and gaming - for example, lights network for Bitcoin.
- Side-chains: Side-chains are independent blockchains that connect to the main chain via a two-way bridge. They offer customisation and faster processing but rely on their own consensus mechanisms
Each L2 solution caters to specific use cases and industries, collectively transforming blockchain technology into a more scalable and accessible ecosystem.

<b>Layer 3: Application (user facing)</b>
Layer 3 is where blockchain technology comes to life. It's all about user-facing applications - decentralised finance (DeFi) platforms, NFT marketplace, games, and wallets. This layer bridges blockchain technology with real-world use cases, making it accessible to end-users.

Popular DApps use as Uniswap (a decentralised exchange), OpenSea (an NFT marketplace) and Axie infinity (a blockchain-based game) operate at layer 3. They rely on L1 and L2 infrastructure for security and scalability while focusing on usability and innovation.

<u>Glossary</u>

<font color="blue">Side-Chain</font> - A separate blockchain network that connects to a parents blockchain, also known as a mainnet, via a two-way bridge, allowing for the secure transfer of digital assets between the two chains.
