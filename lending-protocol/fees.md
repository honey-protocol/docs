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

Market creators can institute a fee in their markets. These admin fees also work as a commission on interest rates, and can range anywhere from 0% to 50% of the accrued interest in a market.

Admin fees are deducted from the total interest paid at the same time as protocol fees.

{% hint style="info" %}
In a market with a 5% admin fee, if borrower's pay 100$ worth of interest to lenders:\
\- lenders will receive 85$\
\- Honey DAO will receive 10$\
\- Market admin will receive 5$
{% endhint %}

## Borrow fees

These fees are a commission on the debt issued by the protocol. Honey takes 1.5% of the debt  upon borrowing.

{% hint style="info" %}
If a borrower withdraws 100$ worth of debt, they will withdraw 101.5$ from the lending pool. Their debt upon borrowing will be set at 101.5$, and they will receive the requested 100$.
{% endhint %}

{% hint style="warning" %}
Borrow fees are currently set to 0% on our Solana NFT lending beta and replaced by a minimum interest of 150 bps on debt.
{% endhint %}

## Revenue

Currently, the Honey Development Association and Honey Labs are eligible to claim these fees to fund development of the protocol.
