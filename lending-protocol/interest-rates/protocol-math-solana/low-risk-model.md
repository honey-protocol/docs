---
description: Interest rate model for low risk assets
---

# Low risk model

## Objective

The low risk model is intended for low risk collaterals. It aims to maintain utilisation between 60% and 80%.

* Bluechip NFTs
* Capital efficient

## Graph view

<figure><img src="../../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
The spread between the borrow rate and the supply rate is due to capital inefficiency.

The less supplied funds are being utilised, the less supplied funds earn interest. As more of the supplied funds earn interest, the spread between interest paid by borrowers and earned by lenders tightens.
{% endhint %}

{% hint style="warning" %}
These values do not factor in admin fees. Higher the admin fees result in lower supply APRs.
{% endhint %}

## Table view

| Utilisation rate | Borrow APR | Supply APR |
| ---------------- | ---------- | ---------- |
| 0%               | 5.00%      | 0%         |
| 5%               | 8.75%      | 0.44%      |
| 10%              | 12.50%     | 1.25%      |
| 15%              | 16.25%     | 2.44%      |
| 20%              | 20.00%     | 4.00%      |
| 25%              | 23.75%     | 5.94%      |
| 30%              | 27.50%     | 8.25%      |
| 35%              | 31.25%     | 10.94%     |
| 40%              | 35.00%     | 14.00%     |
| 45%              | 38.75%     | 17.44%     |
| 50%              | 42.50%     | 21.25%     |
| 55%              | 46.25%     | 25.44%     |
| 60%              | 50.00%     | 30.00%     |
| 65%              | 57.50%     | 37.38%     |
| 70%              | 65.00%     | 45.00%     |
| 75%              | 72.50%     | 54.38%     |
| 80%              | 80.00%     | 64.00%     |
| 85%              | 110.00%    | 93.50%     |
| 90%              | 140.00%    | 126.00%    |
| 95%              | 170.00%    | 161.50%    |
| 100%             | 200.00%    | 200.00%    |

