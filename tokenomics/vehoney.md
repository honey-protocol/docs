---
description: Time weighted governance
---

# veHONEY

Vote escrowed HONEY (or veHONEY) represents governance in the Honey DAO.

veHONEY follows the veTOKEN model created by Michael Egorov (Curve), which allows governance in DAOs to be controlled by those with long term vested interests in the protocol.

Users can lock their $HONEY tokens for set periods of time and receive veHONEY as a function of two variables:

* How much $HONEY is locked
* How long $HONEY is locked for

{% hint style="info" %}
How much veHONEY is received for locking up 100 HONEY tokens, depending on time:\
\
**1 month**: 100 HONEY -> **2** veHONEY\
**3 months**: 100 HONEY -> **6.25** veHONEY\
**6 months**: 100 HONEY -> **12.5** veHONEY\
**1 year**: 100 HONEY -> **25** veHONEY\
**4 years**: 100 HONEY -> **100** veHONEY
{% endhint %}

## Votes

### Approving lending markets

Governance proposals are used to approve new lending markets into the protocol. This means projects wishing to be added for collateralisation must either vest HONEY to vote for themselves or incentivise current holders to approve their proposal through bribes.

Bribes are usually spl tokens distributed to voters of certain proposals. These tokens can be governance, farming rewards, USDC, whitelist tokens, NFTs, etc.

### Honey Improvement Proposals \[HIPs]

The protocol's tokenomics and changes to its programs / smart contracts must be approved by the community through governance.

## Boosted yields\*

Those who vest HONEY tokens into veHONEY can receive boosted APRs on the liquidity they supply in lending markets.

Vesting HONEY or locking NFTs allows lenders to boost their stable coin yield by 20%.

This is currently being developed.&#x20;

## Revenue sharing\*

The Honey Finance protocol generates fees which could be redistributed to veHONEY holders. This is not included in the design of the token to avoid regulatory issues, however nothing stops the DAO from routinely redistributing these fees to holders.

Such a proposal cannot come from the core team, and must be properly decentralised. Up to 75% generated fees are open for potential redistribution.



## Staking-as-a-Service

DAOs utilising Honey's staking-as-a-service (SaaS) can vest HONEY to be featured on the page's approved collections. Farms are ordered by the amount of veHONEY held by the pool creators.\
\
HONEY must also be vested in order to unlock certain features such as dual rewards, and gamified staking.

The cost of these additional features goes up linearly every week. When a DAO purchases HONEY and locks it for the farm, they lock in the price at which they vested it at for the duration of their vesting period.



## pHONEY vesting vs HONEY vesting

_pHONEY is a deprecated asset no longer supported by Honey DAO_

Both tokens can be locked to receive veHONEY.

When pHONEY is vested to receive veHONEY, it is automatically converted to HONEY and burned. The amount of HONEY received after the vesting is over depends on the vesting period. Converting pHONEY to HONEY using a vested pool means applying a multiplier to the pHONEY : HONEY ratio. This means pHONEY vested for 12 months has a 1:10 pHONEY : HONEY ratio.

When a pHONEY : HONEY conversion happens in the vested pool, the user receives veHONEY calculated from how much HONEY they will receive at the end of the lock.

HONEY tokens can also be vested for veHONEY. They have no multiplier and simply turn into time weighted governance. When the vesting period is over, the user can claim the same amount of tokens they locked up.

