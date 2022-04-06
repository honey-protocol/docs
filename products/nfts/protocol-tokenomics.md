---
description: How does it all work together ?
---

# Protocol tokenomics

## How it works

We've prepared a quick diagram to go over the different transactions and interactions within the protocol. Borrowers use NFTs as collateral, and liquidity comes from SOL and USDC lenders. $HONEY is earned for providing liquidity into the system, and $HONEY can be staked to receive fees from the protocol.

These flows work the same across all chains.

![](<../../.gitbook/assets/image (3).png>)

## Where does liquidity come from ?

Lenders provide SOL or any SPL token compatible with their lending market. When supplying liquidity, they earn interest from borrowers, and exposure to the NFT collection of the market they selected. Additionally, the DAO can incentivise liquidity with $HONEY emissions.\
\
DAOs can fund their own lending markets to optimise capital efficiency of their treasuries, while ensuring the money doesn't leave the walls of their communities. DAOs can allocate $HONEY emissions to enable greater volume in their markets.

## Are funds safe ?

We are making security and safety of funds an absolute priority. On top of obtaining audits and open sourcing our code, we are implementing insurance funds to act as buffers to support potential undercollateralization (with cataclysmic drop in floor prices) or any kind of liquidity glitch. This insurance fund will be allocated from the DAO treasury, and will grow as revenue continues to be accrue.

The size of insurance fund will vary depending on market conditions and will always be voted upon by our DAO.

## How do you value my NFT collateral?

The value of your NFT is decided by the floor price of the collection it belongs to. This floor price is tracked with APIs which gather information from multiple different marketplaces while also scanning on-chain data. These APIs are aggregated with our own on-chain oracle called Pravda, which estimates the liquidity of a certain NFT collection, and also serves as a volatility index. We do our best to remove the outliers, and the oracle is fully open sourced, so it can be adjusted by the community and DAO.

Our current loan-to-value should hover at around 50% but this will rely on the volatility score given by Pravda, so an NFT with a floor price of 100 SOL will be eligible for a loan of maximum of 50 SOL.



## What if my NFT is rare ?

In this case, you can still get instant liquidity from borrowing, and liquidators will bid on your collateral. We will show you the best offer, which you can accept, and enter a peer-to-peer loan.\
\
This means that the vast majority of NFTs can benefit from the automation of a peer-to-contract system, however rarer and more valuable NFTs can benefit from price discovery by collectors themselves.
