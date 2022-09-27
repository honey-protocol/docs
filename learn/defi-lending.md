---
description: The basics of decentralised lending & borrowing
---

# DeFi lending

## **🔑 Key terms**

Below are the fundamental concepts you should be aware of before using any decentralised lending protocol. This list is not exhaustive and will grow over time. The more of these you learn, the more fruitful your DeFi journey will be.

## Collateral

Asset(s) supplied by the borrower to the lender, which can be sold in case the borrower does not pay back their loan. In DeFi, the collateral you provide is usually greater than the loan you receive, we call this overcollateralisation. - [read more](https://www.investopedia.com/terms/c/collateral.asp)

If you pay back your loan, you will receive your collateral NFT back. This also means the NFT you provide as collateral will be worth more than the loan you receive.



## Allowance

Allowance determines how much a borrower is able to withdraw from the value of their collateral.

In overcollateralised markets, allowance is always worth less than the estimated value of the collateral. It's measured using [LTV](defi-lending.md#loan-to-value-ratio), but it is not the same thing as LTV.

While the allowance marks the limit of what a borrower can manually borrower, a borrower's LTV can go above the allowance if interest accrues, or if the value of their collateral decreases.&#x20;

Allowance is adjusted and increased after loans are partially paid back, but it will never go above the market's predefined parameters.

## Loan-to-Value ratio

LTV, or Loan-to-Value is a ratio (expressed in percentages) of how much you've borrowed divided by the value of your collateral. - [read more](https://www.investopedia.com/terms/l/loantovalue.asp)\
\
It's the inverse equation of the the collateralisation ratio.

![Example: Your NFT (collateral) is worth 100 SOL, you borrow 50 SOL. Your LTV = 50%](<../.gitbook/assets/image (1) (1) (1).png>)

## Debt

Debt is the amount of money that is being used by borrowers. It has left the protocol, and is insured by collateral provided by borrowers.

{% hint style="warning" %}
"‘... 'debt’ is a legally enforceable promise from a debtor to a creditor to pay an interest rate and eventually repay the principal. Therefore, ‘debt’ cannot exist without legal agreements and cannot be enforced without courts of law." [_Yearn disclaimer_](https://yearn.finance/disclaimer)\
\
Meaning that debt in DeFi simply emulates how credit works in the traditional financial system, but it is not legally the same thing.
{% endhint %}

Debt in DeFi is overcollateralised. The interest rate, sometimes referred to as borrow APR accrues on debt, which increases the amount owed to lenders.

## APR vs APY

Annual Percentage Returns vs Annual Percentage Yields. The difference is in how they are calculated. APR usually takes the average returns on an investment and annualises it by multiplying daily returns by the number of days in a year.

APY does the same, but usually compounds these returns. Most APYs in DeFi are measured with daily compounding.

APRs represent linear growth while APYs represent exponential growth. Thus, APYs will usually be higher than APRs. The higher the APR, the exponentially higher the APY on the same investment.

