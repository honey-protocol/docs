---
description: Deposit NFT collateral to get a loan
---

# Borrowing

Borrowing on Honey is always overcollateralised, meaning that borrowers must deposit collateral that is worth more than the amount they borrow.

Loans do not have fixed durations, meaning that interest accrues over time. As long as borrowers pay down their interest and the value of the collateral does not go down, positions can stay open indefinitely.

## Variable interest rates

Interest rates (also called Borrow APRs) are variable, which means they accrue over time at different speeds. If a variable interest rate is set to 365% Borrow APR, it means each day interest will accrue by 1%.

The variability of the rates are determined by supply and demand. This means the more surplus of liquidity there is in a lending pool (more money being supplied than what is needed) the more rates will go down (and vice versa).

{% hint style="info" %}
Notice that Borrow APR does not compound, while supply APR does. That is why supply APR is measured using APY. Click [here](../../learn/defi-lending.md#apr-vs-apy) to learn more about APR vs APY.&#x20;
{% endhint %}

## Loan to value

Loan to value (LTV) is an indicator of how much can be borrowed from a collateral's value. A 50% LTV means that half of a collateral's dollar value (floor price) is given out to the borrower as a loan.

Maximum LTV is determined by pool admins, but users cannot currently select values higher than 50%. Positions with higher LTVs have a higher risk of being liquidated as a small decrease in the value of the collateral could mean liquidation.

## Liquidation threshold

A position's liquidation threshold determines the maximum LTV at which collateral can be liquidated. At the moment, liquidation thresholds for NFTs are set at 65% LTV.

Each lending pool has its own liquidation threshold based on the risk of the underlying collateral. Liquidation thresholds are at the discretion of pool admins, who manage lending pools on Honey.

## Risk level

To make tracking positions more intuitive, Honey features risk levels for each position. The risk level represents how close a position is to its liquidation threshold.

{% hint style="info" %}
If a loan reaches its liquidation threshold, the risk level will display as 100%.\


_If the liquidation threshold is 65%, and a user has a position with a 32.5% LTV, their risk level will be 50%._
{% endhint %}

