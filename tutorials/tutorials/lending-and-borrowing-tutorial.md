---
description: How to create NFT loans on Honey Finance
---

# Create a loan

{% tabs %}
{% tab title="Step 1 - Wallet" %}
### Connect wallet

You will first need to connect your Solana wallet to the application. Simply click connect wallet, select your wallet provider, and approve the prompt from your wallet provider to connect to the website.

![](<../../.gitbook/assets/image (6).png>)
{% endtab %}

{% tab title="Step 2 - Selection" %}
### Select a market

Head over to the borrow page, where you will see a list of available markets.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

Each market serves an NFT collection, select a market for an NFT that you own, and your NFTs from the selected collection will show up on the right.\


### Choose an NFT

![](<../../.gitbook/assets/image (11).png>)

Select an NFT from that collection, and deposit it onto the platform. At the moment, markets are limited to 1 loan per wallet, to protect markets at launch. This means only 1 of your NFTs at a time can be used as collateral in a market.\
\
Depositing the NFT creates a loan position, with a debt of 0 SOL. No interest is accruing until you borrow.
{% endtab %}

{% tab title="Step 3 - Borrow" %}
### Borrow SOL&#x20;

After depositing an NFT into a market, you can now borrow liquidity from lenders. The NFT you have deposited serves as collateral.

![](<../../.gitbook/assets/image (5).png>)

At the top left corner, you will find the **estimated value** of your collateral (NFT). This is value is read from Switchboard oracles, tracking the floor price of the collection.



Below you will see your **risk level**, as this goes up, your loan is more likely to get liquidated. Keep this low to not lose your collateral.



Your **allowance** is how much you can borrow from this NFT.



### Input a SOL value

Use the slider to select an amount of SOL you would like to borrow. This will automatically tell you how much USD worth of SOL you will receive.

![](<../../.gitbook/assets/image (9).png>)

\
The values to the right of the borrow form will update after you have selected a value. This is a preview of your position after you click `Borrow`.
{% endtab %}
{% endtabs %}

