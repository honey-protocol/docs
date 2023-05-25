---
description: Supply liquidity to NFT collections to receive yield
---

# Lending

Lenders can supply supply liquidity to lending markets and earn interest on fees paid by borrowers. The interest paid by borrowers determines the supply APR, which is an interest rate on the assets supplied by lenders.

Liquidations serve to pay back the loans from borrowers and repay the lenders. Liquidations close open positions, which means lenders are paid back their principle + interest.

## Isolated Risk Markets

Each lending market or pool on Honey lives in isolation. Risk is not carried over from one market to another, and if one suffers a cascade of liquidations, it will not affect the overall protocol.

Thus each lending pool has a different risk profile, interest rate, and collateral type. Supplying liquidity as a lender means choosing which lending pool has the most favorable parameters.

## Utilisation rate

The utilisation rate in a lending pool expresses how much of the deposited liquidity is current being borrowed. Each market has an optimal utilisation rate, which attempts to balance capital efficiency (using as much supplied as possible) and lender solvency (lenders being able to withdraw funds at any moment).

Interest rates for both lenders and borrowers are a function of the utilisation rate in each lending pool. Higher utilisation in a lending pool implies there is a high demand for borrowing, and a low supply of lending. Interest rates will adjust to this supply and demand:

* **High utilisation:** Increase interest rates to incentivise more lending.
* **Optimal utilisation:** Lenders can withdraw capital when needed, and borrowers have access to liquidity.
* **Low utilisation:** Reduce interest rates to incentivise borrowing.

## Auto-compounding

Deposited liquidity in Honey auto-compounds, meaning that whenever interest is paid by borrowers, it is immediately added back in the liquidity pool.

This allows the interest rate perceived by lenders to compound over time. Calculations for _Estimated APY_ annualise the current interest rate, and compound it at a weekly rate.
