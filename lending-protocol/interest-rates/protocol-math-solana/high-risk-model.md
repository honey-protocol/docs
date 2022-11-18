---
description: Interest rate model for low risk assets
---

# High risk model

## Objective

The high risk model is tailored for high risk collaterals. It aims to maintain optimal utilisation between 40% and 60%, while attempting to minimise the risk of 100% utilisation.&#x20;

* Novel assets
* Volatile assets
* Protect lenders

## Graph

<figure><img src="../../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
The spread between the borrow rate and the supply rate is due to capital inefficiency.

The less supplied funds are being utilised, the less supplied funds earn interest. As more of the supplied funds earn interest, the spread between interest paid by borrowers and earned by lenders tightens.t
{% endhint %}

{% hint style="warning" %}
These values do not factor in admin fees. Higher the admin fees result in lower supply APRs.
{% endhint %}

## Table

| Utilisation rate | Borrow APR | Supply APR |
| ---------------- | ---------- | ---------- |
| 0%               | 10%        | 0%         |
| 5%               | 17.5%      | 0.88%      |
| 10%              | 25%        | 2.50%      |
| 15%              | 32.5%      | 4.88%      |
| 20%              | 40%        | 8.00%      |
| 25%              | 47.5%      | 11.80%     |
| 30%              | 55%        | 16.50%     |
| 35%              | 65%        | 21.88%     |
| 40%              | 70%        | 28%        |
| 45%              | 72.5%      | 32.63%     |
| 50%              | 75%        | 37.50%     |
| 55%              | 77.5%      | 42.63%     |
| 60%              | 80%        | 48.00%     |
| 65%              | 107.5%     | 69.88%     |
| 70%              | 135%       | 94.50%     |
| 75%              | 162.5%     | 121.88%    |
| 80%              | 190%       | 152%       |
| 85%              | 217%       | 184%       |
| 90%              | 245%       | 220.5%     |
| 95%              | 272.5%     | 258%       |
| 100%             | 300%       | 300%       |
