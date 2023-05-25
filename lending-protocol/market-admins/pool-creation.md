---
description: Permissionless Lending Pools
---

# Pool creation

Anybody with a certain amount veHONEY can spin up a lending pool for any given NFT collection.

**Requirements for listing:**

* Pool admin must hold at least 50k veHONEY
* NFT collection must use [metaplex standard](https://docs.metaplex.com/programs/token-metadata/token-standard) and EIP-721 (+ more standards comming soon)
* Collection must have a Switchboard or [Hivemind](http://localhost:5000/o/0iIgSZYwSypHqRZjZ9zl/s/VCstantoChab6VNFv1ak/) oracle

Most fields in the lending pool creation are mutable, and be changed at a later date.

{% hint style="danger" %}
Pool admins have full control over their pools and their oracles. This means pool admins could act maliciously resulting in the loss of user funds. Please be careful when using unverified pools on Honey Finance.
{% endhint %}

