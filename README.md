# atlant-dex-contracts

<p align="center">
<img src="https://user-images.githubusercontent.com/12106540/29994000-3d005684-8fce-11e7-97ea-a16a6c607a3f.png" />
</p>

**ATLANT Decentralized Exchange (ADEX) contracts**

Exchange matching engine implemented as a smart contract written in Solidity language (Ethereum).

Order matching supported, as opposed to many existing exchange contracts (e.g. EtherDelta). Ethereum ERC20 tokens traded versus Ether.

## Supported features & benefits
* Order matching
* Any ERC20 token support
* Exchange decentralization
* Funds inaccessible for 3rd parties
* Optimized performance
* Reduced gas consumption

## Currency pairs
* Base currency: **ERC20 token (any)**
* Quote currency: **ETH**

Any ERC20 Ethereum token may be deposited to this exchange contract and subsequently traded versus Ether.

This includes a series of at least two transactions: a deposit transaction (ETH or ERC20 token) and an exchange transaction (providing amount & price). Token exchange is conducted by the contract automatically.

This contract references the rbt-solidity library, providing RB tree data structure for the order book implementation (orders sorted by price).

## Algorithmic complexity
* Order search **O(log n)**
* Order insertion **O(log n)**
* Order removal **O(log n)**

## Build instructions
**Test**
```
npm install -g ethereumjs-testrpc
./install-deps.sh
./testrpc.sh
truffle test
```

**Production**
```
./install-deps.sh
truffle compile
truffle migrate
```

Built with Truffle and OpenZeppelin.

Published under MIT license.
