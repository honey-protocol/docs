---
description: Explanation of fees in Honey's peer-to-contract protocol
---

# Fees

## Protocol fees

Honey charges a 10% commission on interest rates which go to the Honey DAO multisig wallet.

{% hint style="info" %}
If borrower's pay 100$ worth of interest to lenders, lenders will receive 90$, with the remaining 10$ going to the DAO.
{% endhint %}

## Admin fees

Lending pool creators can institute a fee in their lending pools. These admin fees also work as a commission on interest rates, and can range anywhere from 0% to 50% of the accrued interest in a lending pool.

Admin fees are deducted from the total interest paid at the same time as protocol fees.

{% hint style="info" %}
In a lending pool with a 5% admin fee, if borrower's pay 100$ worth of interest to lenders:\
\- lenders will receive 85$\
\- Honey DAO will receive 10$\
\- Pool admin will receive 5$
{% endhint %}

## Borrow fees

These fees are a commission on the debt issued by the protocol. Honey takes 1.5% of the debt upon borrowing on Solana.

{% hint style="warning" %}
Borrow fees on Honey's EVM beta (Polygon, Arbitrum, etc.) are currently set at 2%.
{% endhint %}

{% hint style="info" %}
If a borrower withdraws 100$ worth of debt, their debt will be 101.5$. The additional 1.5$ is protocol revenue which can be claimed by the DAO from the lending pool.
{% endhint %}

## Revenue

Currently, the Honey Development Association and Honey Labs are eligible to claim these fees to fund development of the protocol.
