# VoteCast - ETHGlobal London 2024 Project
![ETHGlobal_London_Banner](https://github.com/ethglobal-london-2024/votecast/assets/8581537/79d0c6ea-d927-4fd7-afd3-5e8d7ade533b)

## About
Enable Cross-Chain DAO Participation on the Farcaster Network

We empower Farcaster users to participate in DAO governance, irrespective of the underlying blockchain network. 

Our product enables users to cast votes on proposals across different chains directly from their Safe ERC4337 wallet on the Base Network, streamlining the governance process and fostering greater community involvement.

## Impact and Vision
By bridging the gap between Farcaster users and DAOs across different blockchain networks, our project aims to democratize participation in decentralized governance. We envision a future where the barriers to cross-chain interaction are minimized, enabling a more inclusive, transparent, and efficient governance landscape. 

## Core Features and Workflow
**Unified Voting Interface:** Our Farcaster Frame serves as a one-stop voting portal, allowing users to engage with multiple DAOs across various blockchain networks without leaving the Farcaster environment. This integration not only simplifies the voting process but also enhances user experience by consolidating governance activities into a single, intuitive platform.
**Smart Wallet Integration with Safe:** At the heart of our system lies the association between each Farcaster ID and an ERC-4337 compliant smart wallet. In our case that is a Safe wallet with ERC4337 module.
**Cross-Chain Communication via LayerZero:** To facilitate voting across different blockchains, our framework utilizes LayerZero. When a Farcaster user casts their vote, the system automatically generates a message through LayerZero, targeting the specified destination chain (e.g., Arbitrum) with an encoded UserOperation. This process ensures that votes are accurately and efficiently relayed across networks, preserving the integrity and intent of each user's participation. The only requirement is for the user to have enough voting power on the destination chain. 
**Seamless Interaction with Destination Chains:** Upon receipt of the cross-chain message, the LayerZero receiver on the destination chain initiates a call to the EntryPoint contract. This action triggers the appropriate voting mechanism on the destination chain, effectively counting the user's vote in the targeted DAO proposal.
**Fee Management via Coinbase Paymaster:** To address the challenge of on-chain transaction fees, our system incorporates the Coinbase Paymaster for fee handling. This integration ensures that users can participate in cross-chain governance activities without being deterred by varying gas fees, thereby promoting higher engagement and participation rates within DAOs.
**Cross-Chain Communication via ChainLink:** CCIP to enhance cross-chain transactions security


## Farcaster Frame
https://github.com/ethglobal-london-2024/frame-dao-voting

## LayerZero Cross Chain Vote
https://github.com/ethglobal-london-2024/layerzero-cross-chain-vote

## Chainlink CCIP Cross Chain Vote
https://github.com/ethglobal-london-2024/ccip-cross-chain-vote

# Deployed Contracts

## Base Mainnet

- SourceVoterOApp - https://basescan.org/address/0xCeeF0be32E21205b14a9ABa2A23A54248556D3a7

## Arbitrum One Mainnet

- DestinationVoterOApp - https://arbiscan.io/address/0xCeeF0be32E21205b14a9ABa2A23A54248556D3a7
