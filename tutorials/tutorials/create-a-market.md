---
description: Create an unverified market
---

# Create a market

**Requirements for listing:**

* Market admin must hold at least 50k veHONEY
* NFT collection must use [metaplex standard](https://docs.metaplex.com/programs/token-metadata/token-standard)
* Collection must have a Switchboard oracle or create one

## Step 1 - Create a market

{% tabs %}
{% tab title="NFT collection name" %}
This will act as the name for your market.&#x20;

It can be changed at a later date by creating a pull request on github and pinging the Honey Labs team in our discord's builders channel.
{% endtab %}

{% tab title="Magic Eden link" %}
This field allows the team and community to fill in any missing information about your collection by querying Magic Eden or your Solana marketplace of choice.

It isn't used to run any of Honey's infrastructure, but instead ties your market to an existing collection.

Using collections supported by Magic Eden makes creating an oracle much easier down the road, as you will be able to query floor prices via Magic Eden's API.
{% endtab %}

{% tab title="Verified Creator" %}
{% hint style="info" %}
**This step is critical. Inputing an incorrect verified creator will render your market unusable.**
{% endhint %}

Most NFTs using [Metaplex's NFT standard](https://docs.metaplex.com/programs/token-metadata/token-standard) will have one or more addresses listed as verified creators.

Usually, this address will point to the candy machine which minted the NFTs.



## How to find the verified creator ?

We recommend going to Magic Eden and finding the page associated to this particular collection.

Once on that page, view the _details_ page for that NFT. On the NFT's page, you can scroll down to _details_ and find a field called **Mint address**. You can then pick whichever explorer you feel most comfortable with, this example uses Solscan:

![](<../../.gitbook/assets/image (2).png>)

On the explorer page for the NFT, you'll find a field called **Creators**. This will show the distribution of royalties, with the check mark indicating that a creator address is a verified creator address.

In most cases, the verified creator with 0% royalties will be the candy machine used to mint the NFT. Select this address and input it into Honey's market creation tool.



## Which verified creator to pick ?

In cases where your NFT collection has multiple verified creators, we recommend using the candy machine address.

**If your verified creator address is used by more than 1 collection, you should NOT use it. As other collections sharing the verified creator address could then be used as collateral in your market.**

Using the candy machine of a particular collection reduces this risk.
{% endtab %}
{% endtabs %}

## Step 2 - Setup an oracle

{% hint style="info" %}
Oracles are programs which value the collateral used in the market.

Honey Labs recommends using two separate oracles per market, a price oracle, and a TWAP oracle to average the price.
{% endhint %}

{% tabs %}
{% tab title="Collection has no oracle" %}
### Step 1 - Switchboard

Navigate to [app.switchboard.xyz](https://app.switchboard.xyz) and select the **NFT Floor Price (SOL)** card in the popular collections list.\


### Step 2 - Pick template

Select any pre-made option. For this example, we will use the **Solana Monkey Business Floor Price** template which you can find [here](https://app.switchboard.xyz/template/aafff881-ef69-4867-bbda-cdf1ee83dc31/feed/948e6922f14acff92999605999667831c7b11ebc1472de4a9e7c103ac5744e07).

<figure><img src="../../.gitbook/assets/image (3) (3).png" alt=""><figcaption><p>List of templates</p></figcaption></figure>

Select the template by clicking the `Add to Cart` button followed by the `Configure feed` button in your cart.\


### Step 3 - Configure your template

Start by naming your new price feed. Get this out of the way right now so you don't forget to do it later:

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption><p>Edit feed name</p></figcaption></figure>

For this example, we'll create a price feed for the Anon Club NFT collection, and will thus name our new price feed **Anon Club Floor Price.**

We now need to edit our feed to track Anon Club instead of SMBs.

Click on the three dots menu item, and this time navigate to the`View Details` button. You'll notice that this template is fetching the SMB floor from 3 different sources (SMB marketplace, SolanaFloor, and Magic Eden).

{% hint style="info" %}
**Select the correct sources for your price feed.**\
**-** Make sure to source your floor price from marketplaces with high enough volume. Low volume marketplaces can have their floor prices be more easily manipulated.\
\- Sourcing from aggregators is a good idea.
{% endhint %}

### Step 4 - Edit price feeds

Once you are on the `View Details` modal of your price oracle, you should see an option to `Edit Feed` at the bottom right corner.

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption><p>Edit Feed</p></figcaption></figure>

This will allow us to input the sources which will inform the oracle about the collection's floor price.

In our case, most of the volume for the Anon Club collection goes through Magic Eden, so we will get rid of the SMB marketplace price feed and the SolanaFloor price feed.

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>Click the X top right corner</p></figcaption></figure>

We're now left with our Magic Eden price feed. If you click `Test` you'll see the floor price of SMB in SOL. To change this, swap the names of the Magic Eden collection:\
\
https://api-mainnet.magiceden.dev/v2/collections/solana\_monkey\_business/stats

Becomes:

https://api-mainnet.magiceden.dev/v2/collections/\<YOUR\_COLLECTION\_NAME>/stats\
\
Check Magic Eden's link for your NFT collection, and use the same suffix. In our Anon Club example, Magic Eden uses the link: https://magiceden.io/marketplace/888\_anon\_club so we replace \<YOUR\_COLLECTION\_NAME> with `888_anon_club`.\
\
Now if we click `Test`, we should get the floor price of Anon Club.

{% hint style="info" %}
By picking the SMB template, we already have a 3rd step in our ME price feed which divides the received value by the needed decimals using `DivideTask` and `Scalar`.&#x20;
{% endhint %}

###

### Step 5 - Checkout

Once you are done configuring your price feeds, add it to your cart, and proceed to checkout.

<figure><img src="../../.gitbook/assets/image (1) (3).png" alt=""><figcaption></figcaption></figure>

Before you fund the oracle, you will need to tell Switchboard how long you want to fund it for, and how frequently you want it to update. The more often the oracle updates, the more expensive it will be.

Lowering values such as Batch size will lower the cost of the oracle, as well as it's security.

You can decide how frequently you want your oracle to update it's price. This is up to you and should be a function of your collection's volatility, but we generally recommend keeping it under 1 hour.

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption><p>Expected volatility = update more frequently</p></figcaption></figure>

You're all set ! You can now proceed checkout and fund the oracle with your phantom wallet.
{% endtab %}

{% tab title="Collection already has an oracle" %}
Even if your collection has an oracle on Switchboard, it's strongly recommended that you create your own.

Two oracles should exist for a market, a price oracle, tracking a floor price API for a given collection, and a TWAP oracle, which averages the given price over a set period of time.

{% hint style="info" %}
Technically, any integer value received from the oracle will work for your market. Oracles can provide a constant number, or be manually set (no API tracking). If you have a use for this, then you are free to do so.
{% endhint %}



### Step 1 - Switchboard

Navigate to [app.switchboard.xyz](https://app.switchboard.xyz) and select the **NFT Floor Price (SOL)** card in the popular collections list.\


### Step 2 - Pick template

Select the option that corresponds to the floor price of your NFT collection.
{% endtab %}
{% endtabs %}











