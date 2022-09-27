---
description: Deposit NFT collateral to get a loan
---

# Borrowing

Borrowing on Honey is overcollateralised, meaning that borrowers must deposit more collateral than the amount they borrow.

Loans do not have fixed durations, meaning that interest accrues over time. As long as borrowers pay down their interest and the value of the collateral does not go down, positions can stay open indefinitely.

## Variable interest rates

Interest rates (also called Borrow APRs) are variable, which means they accrue over time at different speeds. If a variable interest rate is set to 365% Borrow APR, it means each day interest will accrue by 1%.

{% hint style="info" %}
Notice that Borrow APR does not compound, while supply APR does. That is why supply  APR is measured using APY. Click here to learn more about APR vs APY.&#x20;
{% endhint %}

## Loan to value

Loan to value (LTV) is an indicator of how much can be borrowed from a collateral's value. A 50% LTV means that half of a collateral's dollar value (floor price) is given out to the borrower as a loan.

Maximum LTV is determined by market admins, but can be no higher than 60%. Positions with higher LTVs have a higher risk of being liquidated for the as a small decrease in the value of the collateral could mean a liquidation.

## Liquidation threshold

A position's liquidation threshold determines the maximum LTV at which collateral can be liquidated. At the moment, liquidation thresholds for NFTs are set at 75% LTV.

_Example (1) : a borrower deposits an NFT worth 1000 USDC of collateral. They take out a loan worth 500 USDC. Their LTV is 50%. If the value of the collateral (floor price of collection) drops by 35%, their collateral is now worth 650 USDC. The new LTV would be \~ 77%, and will have crossed the liquidation threshold._

_Example (2) : a borrower deposits an NFT worth 1000 USDC of collateral. They take out  a loan worth 250 USDC. Their LTV is 25%. The value of their collateral would have to drop 66.5% in order for the liquidation threshold to be crossed._

