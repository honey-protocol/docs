---
description: >-
  Frequently asked questions about staking v3, staking as a service, and NFT
  farms
---

# Farms FAQ

### What does locking do ?

Locking starts the rewards for your NFTs. Once you're locked in, you're ready to go. If you're coming from v2, this lock button is the final step to complete the migration. This is made for collections who utilise the cooldown feature.&#x20;

Honey Genesis bee v3 farm has no cooldown period, so you can unlock at any time.

### Why is it more expensive ?

Depositing NFTs into programs requires Solana to create a wrapper around your NFT called an [associated token account](https://spl.solana.com/associated-token-account). For this wrapper to exist on the blockchain, it needs to contain SOL in order for validators to not disregard it as spam. Solana calls this [rent](https://docs.solana.com/implemented-proposals/rent).

When withdrawing, you get the SOL back.

### How do I stake in v3 ?

There are a lot of extra or optional steps in staking v3, we've decided to launch without bundling these steps to showcase them individually, we will however bundle unnecessary steps in the future. For example, when you deposit multiple NFTs, we can go ahead and assume you're going to lock the vault. When you unlock, we can assume you're going to withdraw.

These changes will be made to simplify the user experience.

At the moment, following each of the steps looks like [this](https://www.loom.com/share/481f7560e5204a82be65eebf5c47a42e)

### What is a vault ?

Your vault is a space on the blockchain where your NFTs are stored. Every farmer has their own vault which only they can withdraw from. The protocol (open source code) cannot mess with this as we don't have access to it.

### What are the options in Staking as a Service ?

The base rate includes the following **options** for NFT projects looking to host farms on Honey Finance:

* Rarity based staking
* Fixed reward staking ( X # of tokens / NFT )
* Variable reward staking ( X # of tokens / farm )
* Unstaking cooldown
* Delayed rewards
* Tiered rewards based on time staked
* Limit the number of NFTs that can be staked
