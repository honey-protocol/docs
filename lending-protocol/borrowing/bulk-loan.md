# Bulk loan

{% hint style="info" %}
Bulk loan feature is in early testing, if you experience any issues, please let us know [on discord.](https://discord.com/honeydefi)
{% endhint %}

### How it works

Bulk loans allow borrowers to bundle multiple collaterals into a single loan.

* On Solana:
  * Users are able to hold one position backed by 11 collaterals
  * This means one loan is held by the user and this loan holds 11 NFTs as collateral
* On EVM chains (Polygon, Arbitum, ...)
  * Users can have unlimited positions, each with an unlimited amount of collaterals

### **Liquidations**

Each bulk loan only has 1 liquidation price. The liquidation price is based on the collection's floor.

You can keep track of how much the floor of a collection needs to fall in order to have your bulk loan liquidated.

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Unlike traditional lending, liquidating only 1 NFT collateral in a loan cannot improve the overall LTV of a position.
{% endhint %}

When your bulk loan is liquidated, the entire position is liquidated all at once, should there be enough bids to over all issued debt. Otherwise NFTs are liquidated one by one till the position regains a minimum health position.&#x20;

{% hint style="info" %}
You can add and remove collateral whenever you want, without having to repay your entire loan.
{% endhint %}



