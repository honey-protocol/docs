# Peer-to-Peer FAQ

## Borrower FAQ

* **Who owns my NFT when in escrow ?**

The protocol holds on to the NFT collateral in an escrow account. Nobody can withdraw from this account unless the loan is repaid or the loan is liquidated.

* **What happens to airdrops during loan ?**

When collateral is withdrawn, all tokens sent to the escrow can be claimed. This means airdrops during the duration of the loan go to whoever withdraws the collateral.

## Lender FAQ

* **Are lender fees paid out during a liquidation ?**

No lenders fees are applied during liquidations, only borrower fees paid at the beginning of the loan.

## Risks

* **What if the floor of the NFT drops below the amount borrowed ?**

The value of the floor is not relevant in the Honey P2P protocol, but it can incentivise borrowers to let their loans be liquidated, especially in cases where the floor drops below the amount borrowed.

## Verified collections

* **How to get new collections verified ?**

Collections can fill out [this form](https://tally.so/r/npbzL8) to apply for verification. Verifying collections on Honey P2P is at the sole discretion of the team and should take 3-4 days to go through.

* **Are unverified collections safe ?**

Honey P2P is permissionless, which means anybody and everybody can use it. This potentially includes scammers so always double check the information provided is correct. On the other hand, being verified is no guarantee of a project not being a scam or a rug pull.

## Payments

* **What currencies does Honey P2P support ?**

Honey P2P supports USDC. While it could support any SPL token (wSOL, SRM, SDHW, etc.) the protocol limits it to only one token to not segregate supply and demand. USDC is favoured over SOL to allow more complex loans and financial derivatives to be built in Honey P2P, which could not be denominated in volatile tokens.



