# Liquidations

## Liquidation of collateral

Liquidations are events where the protocol sells your NFT collateral, in order to pay back lenders.\
\
Below you'll see how Honey and other protocols tackle this issue, but the most important concept to remember, is that the lenders will always need to be paid back for the money they deposited. Most parameters in a lending protocol are built around making sure that the lender does not lose the money that he loans to borrowers, or else there would be no lenders, and no loans.

## When do liquidations occur ?

There are two reasons why a liquidation can occur. Too much interest has accrued without being paid back, or the value of the collateral provided has gone down.

{% hint style="info" %}
Liquidations are measured using a simple fraction called the Loan-To-Value (LTV):\
\
_Debt / Collateral value = LTV_\
__\
__If the numerator goes up (more debt), or if the denominator goes down (less collateral) then the LTV will increase, until it hits the liquidation threshold.
{% endhint %}

The higher the LTV, the more risky a loan becomes. Each market has a maximum LTV, called the **liquidation threshold**, which determines when a position is too high risk and must be liquidated.

<figure><img src="../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

## Liquidation thresholds

To ensure that borrowers never have more debt from lenders than the collateral they've provided, assets are liquidated before they get too close to being undercollateralised. How close positions can get to undercollateralisation is determined by the liquidation threshold.\
\
While each market can differ based on who the admin is, the Honey protocol has recommended values for admins when creating markets on Honey. By default, maximum LTV someone can borrow is 40%, and the position is liquidated at 65% LTV.

{% hint style="warning" %}
At a maximum LTV of 40%, the collateral's value would have to drop by 38% to be marked for liquidation.
{% endhint %}

## How does Honey run liquidations ?

Honey Finance uses a liquidation aggregator to keep markets safe, and better handle liquidation cascades.

There are currently 3 layers activated in the liquidation program:

* Bids (collection wide)
* Solvent AMM
* OTC

With 6 more layers coming soon:

* Hadeswap AMM
* Tensor AMM
* Elixir AMM
* Goatswap AMM
* Vaults
* Bids (individual NFTs)

Unlike other NFT lending protocols, Honey does not wait for NFTs to be liquidated before handling liquidations. This would result in the protocol, and ultimately the community, holding on to bad debt which it hopes to sell.

Instead, Honey prepares liquidations on collateral as soon as it's deposited into our markets, allowing liquidators to bid on potentially discounted NFTs, even if they positions are healthy. As the positions approach their liquidation thresholds, bidders will need to place the highest bid in order to receive the NFT.

The moment that an NFT crosses its liquidation threshold, it is immediately sold to the highest bidder. If there are no bids big enough to cover the debt, then Honey aggregates different NFT AMMs to find instant liquidity for the collateral. In all cases, collateral is sold instantly, to not allow bad debt to accrue in the protocol.
