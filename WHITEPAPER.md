# BOSAGORA BizNet
**A Network to Enable Smart Contracts**

_NOTE: This document is under development. Please check regularly for updates!_

## Motivation

Agora has been developing mainnet since June 2019. Coinnet will be launched later this year.
Currently, smart contracts are essential for implementing NFT and DeFi, and they have a lot of influence on cryptocurrency as a whole.
In response to these market demands, we plan to prepare BizNet, a blockchain network that supports smart contracts that existing developers can easily adapt without learning obstacles.

## Design Principles

The new chain "**BizNet**" will continue to be maintained after it is created in the Agora ecosystem.
After "**Agora Coinnet**" is opened, it will be operated side by side with "**BizNet**".
Here are the design principles of BizNet:

1. **Standalone Blockchain**: technically, BizNet is a standalone blockchain, instead of a layer-2 solution. Most BizNet fundamental  technical and business functions should be self-contained so that it can run well even if Agora stopped for a short period.
2. **Ethereum Compatibility**: The first practical and widely-used Smart Contract platform is Ethereum. To take advantage of the relatively mature applications and community, BizNet chooses to be compatible with the existing Ethereum mainnet. This means most of the **dApps**, ecosystem components, and toolings will work with BizNet and require zero or minimum changes; BizNet node will require similar (or a bit higher) hardware specification and skills to run and operate.


## Consensus

Based on the above design principles, the consensus protocol of BizNet is to fulfill the following goals:

1. Blocking time should be the same as Ethereum network.
2. It requires limited time to confirm the finality of transactions, e.g. around 1-min level or shorter.
3. There is no inflation of native token: There is no reward for block creation. The BOA may be moved between the BOA token of the Ethereum mainnet and the native token of BizNet using a bridge.
4. It is compatible with Ethereum system as much as possible.

### Proof of Authority

Although Proof-of-Work (PoW) has been recognized as a practical mechanism to implement a decentralized network, it is not friendly to the environment and also requires a large size of participants to maintain the security.

Ethereum and some other blockchain networks, such as [MATIC Bor](https://github.com/maticnetwork/bor), [TOMOChain](https://tomochain.com/), [GoChain](https://gochain.io/), [xDAI](https://xdai.io/), do use [Proof-of-Authority(PoA)](https://en.wikipedia.org/wiki/Proof_of_authority) or its variants in different scenarios, including both testnet and mainnet. 
PoA provides some defense to 51% attack, with improved efficiency and tolerance to certain levels of Byzantine players (malicious or hacked). 

### Proof of Stake

BizNet will continue to upgrade as Ethereum is upgraded to PoS. BizNet will start with PoA initially, but will be upgraded gradually to PoS.

### Reward

There is no reward for block creation in PoA. However, rewards will be paid when switched to PoS.


## Token

The BOA token of Ethereum and Biznet is defined as follows:

1. BOA can circulate on both networks, and flow between them bi-directionally via a BOA Bridge.
2. The total circulation of BOA should be managed across the two networks, i.e. the total effective supply of a token should be the sum of the  token’s total effective supply on both BizNet and Ethereum.

