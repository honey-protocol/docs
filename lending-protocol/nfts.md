---
description: Peer-To-Contract NFT loans
---

# Overview

Honey Finance is composed of multiple lending markets. Each collection has an associated lending market which must be approved by veHONEY holders.

Lending markets match borrowers and lenders of a same collection. Lenders supply liquidity (USDC) to an NFT collection's associated lending market. Borrowers can borrow this supplied liquidity by depositing their NFTs as collateral.

There are three main participants in Honey lending markets:

* **Borrowers:**&#x20;
* **Lenders**
* **Admins**

## Borrowers

Create a new position by depositing NFT collateral into a lending market and borrowing liquidity from lenders. Interest accrues on open positions with a variable interest rate. Each position has a loan to value ratio as well as a liquidation threshold. If the value of the collateral goes down, or the loan is not sufficiently paid down, the NFT can be liquidated.

{% content-ref url="borrowing.md" %}
[borrowing.md](borrowing.md)
{% endcontent-ref %}

## Lenders

Supply USDC to lending markets and receive yield from accrued interest or liquidations.&#x20;

{% content-ref url="lending.md" %}
[lending.md](lending.md)
{% endcontent-ref %}

## Admins

Create lending markets on the platform and set an admin fee. Liquidations and interest repayments will include this fee, generating revenue for the market admin. Admins can be DAOs, projects, or individuals.

{% content-ref url="market-admins.md" %}
[market-admins.md](market-admins.md)
{% endcontent-ref %}



## Liquidations

An NFT can be used to create a debt position in a corresponding lending market. Each market is based around an NFT collection, and quotes the floor price of the associated collection as the value of the collateral.

When borrowing, users are allowed to withdraw based on their allowance. The allowance can be defined as, how much value are you able to receive as a percentage of the floor price.