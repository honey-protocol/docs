# Liquidations

## Liquidation of collateral

Liquidations are events where the protocol sells your NFT collateral, in order to pay back lenders.\
\
Below you'll see how Honey and other protocols tackle this issue, but the most important concept to remember, is that the lenders will always need to be paid back. Most parameters in a lending protocol are built around making sure that the lender does not lose the money that he loans to borrowers, or else there would be no lenders, and no loans.

Liquidations are triggered when health factors reach 0.

## When do liquidations occur ?

A liquidation will take place when the value of your NFT collateral dips, and is no longer sufficiently overcollateralised. The more the value of your collateral decreases, the more lenders are at risk of not being paid back.\
\
_Example: Your NFT is worth 100 SOL, you borrow 60 SOL (60% LTV ratio). If the floor price of this NFT were to drop by 41% or more, the loan would be undercollateralised, since you've borrowed more than the lender currently holds._

{% hint style="info" %}
**Reminder**: undercollateralisation is dangerous in DeFi, since the lender has given you more than the collateral you've given them. What's to stop you from runnning away with the money ? That's why we have to stop undercollateralised positions from ever existing.
{% endhint %}

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

## Liquidation thresholds

One of the worst thing that can happen to a protocol is not being able to pay back lenders who deposited funds into the platform. To ensure that does not happen, assets are liquidated before they get too close to undercollateralisation.\
\
The protocol will never allow for loans to have a collateralisation ratio below 120%. This is the minimum liquidation threshold, however each lending market may vary.

## How does Honey run liquidations ?

Honey Finance utilises NFT pools[ ](https://app.solvent.xyz/)alongside our DAO's backstop liquidity program (BLP). The pool model allows instant liquidity to be available for NFTs while the BLP is used to stop liquidation cascades.\
\
With the backstop liquidity program (BLP), individual members of the Honey DAO will be able to bid on collateral and purchase them in case of liquidations. This means bidders are purchasing long positions with a bidding price at the liquidation threshold.

Both of these solutions allow us to sell NFTs instantly, and monitor how much liquidity we have backing each NFT if we want to sell it. This also means lenders earn exposure to different NFTs depending on which lending markets they select.
