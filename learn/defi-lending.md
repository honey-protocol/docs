---
description: The basics of decentralised lending & borrowing
---

# DeFi lending

## **🔑 Key terms**

Below are the fundamental concepts you should be aware of before using any decentralised lending protocol. This list is not exhaustive and will grow over time. The more of these you learn, the more fruitful your DeFi journey will be.

## Collateral

Asset(s) supplied by the borrower to the lender, which can be sold in case the borrower does not pay back their loan. In DeFi, the collateral you provide is usually greater than the loan you receive, we call this overcollateralisation. - [read more](https://www.investopedia.com/terms/c/collateral.asp)

If you pay back your loan, you will receive your collateral NFT back. This also means the NFT you provide as collateral will be worth more than the loan you receive.



## Collateral ratio

C-ratio or Collateral ratio represents the value of your collateral (your deposited NFT) divided by the value of your loan. In overcolalteralised loans, this ratio should always be greater > 1, and because it is expressed in percentages, it will always be greater than 100%.

![Example: Your NFT (collateral) is worth 100 SOL, you borrow 50 SOL. Your C ratio = 200%](<../.gitbook/assets/image (2).png>)



## Loan-to-Value ratio

LTV, or Loan-to-Value is a ratio (expressed in percentages) of how much you've borrowed divided by the value of your collateral. - [read more](https://www.investopedia.com/terms/l/loantovalue.asp)\
\
It's the inverse equation of the the collateralisation ratio.

![Example: Your NFT (collateral) is worth 100 SOL, you borrow 50 SOL. Your LTV = 50%](<../.gitbook/assets/image (1).png>)

## Health factor

Tracking the health of your loans is incredibly important to avoid bad surprises. Remember, all loans in DeFi must be overcollateralised, because we can't track you down if you don't pay back the lenders. The more your loan is overallateralised, the healthier it is.\
\
If the value of the collateral (the NFT) dips below a certain point, the protocol must trigger a liquidation to guarantee the lenders are paid back. A health factor of 0 means your loan is below this liquidation threshold, and can be liquidated. A health factor approaching 100% means your Loan to value is below 10%. This means your collateral is worth 10x more than your loan.

Having a high health factor doesn't guarantee you will not get liquidated, in a catastrophic market down turn, even healthy positions get sold off. - read more



## APR vs APY

Annual Percentage Returns vs Annual Percentage Yields. The difference is in how they are calculated. APR usually takes the average returns on an investment and annualises it by multiplying daily returns by the number of days in a year.

APY does the same, but usually compounds these returns. Most APYs in DeFi are measured with daily compounding.

APRs represent linear growth while APYs represent exponential growth. Thus, APYs will usually be higher than APRs. The higher the APR, the exponentially higher the APY on the same investment.

