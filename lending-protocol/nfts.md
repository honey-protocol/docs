---
description: Peer-To-Contract NFT loans
---

# Overview

Honey Finance hosts plenty of lending markets.

Each collateral (usually an NFT collection) has it's own lending market.

Lending markets match borrowers and lenders of a same collateral. Lenders supply liquidity (USDC or SOL) to an NFT collection's associated lending market. Borrowers can borrow this money by depositing their NFTs as collateral.

There are three main participants in Honey lending markets:

* **Borrowers:**&#x20;
* **Lenders**
* **Admins**

## Borrowers

Borrow money by depositing NFTs as collateral. Interest accrues on open positions with a variable [interest rate](interest-rates/). Each position has a loan to value ratio as well as a liquidation threshold. If the value of the collateral goes down, or the loan is not sufficiently paid down, the NFT can be liquidated.

When borrowing, users are allowed to withdraw based on their allowance. The allowance can be defined as, how much value are you able to receive as a percentage of the floor price.

{% content-ref url="borrowing.md" %}
[borrowing.md](borrowing.md)
{% endcontent-ref %}

## Lenders

Supply USDC or SOL to lending markets and receive yield from accrued interest or liquidations.&#x20;

{% content-ref url="lending.md" %}
[lending.md](lending.md)
{% endcontent-ref %}

## Admins

Create lending markets on the platform and set an admin fee. Liquidations and interest repayments will include this fee, generating revenue for the market admin. Admins can be DAOs, projects, or individuals.

{% content-ref url="market-admins/" %}
[market-admins](market-admins/)
{% endcontent-ref %}
