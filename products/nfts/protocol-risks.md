---
description: >-
  Below is a non-exhaustive overview of the risks associated to using Honey
  Finance
---

# Protocol risks

## Isolation of risk

Lending and borrowing markets on Honey are what's known as Isolated Risk Markets (IRMs).

IRMs are not funded by the Honey DAO, even for our own collection Honey Genesis Bees. Instead, all of the liquidity in the market is provided by independent lenders which can withdraw their capital at any time.

This means lenders take on the risk of bad debt, instead of the protocol. If collateral cannot be liquidated, lenders will lose parts of their deposited assets and in exchange hold on to fractionalised shares of the collateral.&#x20;

At a protocol level, Honey connects lenders and borrowers, and at no moment does the unsold or unliquidated collateral go back to the Honey DAO. The Honey DAO develops the protocol, and maintains these free and isolated markets on its platform, but does not have a responsibility to intervene in them.&#x20;

Lenders implicitly choose varying levels of risk when providing liquidity to isolated risk markets, as the risk of markets defaulting can be expected to correlate to higher interest rates as a function of supply and demand.&#x20;

**The result of this approach is that one market defaulting does not affect any other market on the protocol**, as risk is isolated. This also allows Honey to add any collections to its markets, as it does not have to worry about the collection's risk and solvency contaminating the protocol, leaving lenders and borrowers to assess the risk for themselves.

## Liquidations & Grace Periods

Unlike most NFT lending protocols, Honey performs auctions _before_ NFTs are marked for liquidation. This is to eliminates the risk of the protocol holding on to bad debt, and makes liquidations predictable and transparent.

When collateral needs to be liquidated, the protocol checks to find the highest bids for the associated collection. If bids are not high enough to cover the full amount of the debt owed to borrowers, then the protocol seeks to liquidate on the various NFT AMMs it integrates with, to obtain instant liquidity.

Liquidations should happen in the best available AMMs and pools, however if slippage is too high, and the value obtained from the AMM is inferior to the debt, then the liquidation will happen anyways. Collateral must be liquidated, and cannot be held as bad debt, meaning the liquidation engine favours losses over a floating and unrealised loss in the market which could get worse with time.

This bad debt accrues in the isolated risk market, it does not necessarily affect a lenders ability to withdraw assets, however it will take time for interest accrued by lenders to pay off the bad debt in the IRM.

To learn more about Honey's liquidation engine, read [here](../../learn/liquidations.md).

Preparing liquidations as loans approach their maximum risk thresholds also means that there are no grace periods, again, minimising bad debt in the protocol. A grace period would result in somebody holding on to the bad debt while waiting for borrowers to potentially pay back their loans. Unless lenders create a market where they accept to temporarily hold on to this bad debt, there is no grace period mechanism by which the DAO or the protocol would hold on to bad debt on behalf of borrowers.

## Bank runs

A bank run in a lending protocol happens when lenders rush to withdraw their money faster than borrowers can repay their loans, and faster than the protocol can liquidate collateral.

Because Honey does not use post-liquidation auctions for liquidating collateral, there is no window of time where lenders have to wait for NFTs to be sold.

As lenders withdraw their capital, the utilisation rate will increase, since a larger share of the remaining capital is being borrowed. Utilisation rates are designed to provide a margin of safety for lenders wishing to withdraw collateral, but if more lenders than the model predicts start to withdraw funds, interest rates will begin to rise exponentially for borrowers.

Rising interest rates will trigger liquidations, however if the majority of lenders decide to withdraw their funds at the same time or in a very short window of time, they will have to wait for increased interest rates to accrue on borrowers. This period of time where funds are unavailable to lenders is the result of a bank run.

To minimise the risk of being caught in a bank run, lenders should always check the utilisation rate of the markets in which they lend. At 100% utilisation, they will need borrowers to either pay back their loan, or be liquidated before withdrawing funds. To learn more about utilisation rates, read [here](../../faq/faq/lending-and-borrowing-faq.md).

## Oracle risks

One of the hardest aspects of issuing loans on NFTs is in valuing the collateral. This is done by oracles who estimate collateral value based on the floor price of a collection over a given amount of time.

Honey protocol's approach is the same with oracles as it is for isolated risk markets. Oracles are chosen by market admins, and it is up to lenders and borrowers to trust the oracle of their particular isolated risk market.

Honey integrates with [Switchboard](https://switchboard.xyz/), a permissionless oracle, allowing anybody to provide their own data feed to value NFT assets. Different markets can be created around different data feeds, and lenders must decide which one they feel has the appropriate levels of risk in return for the interest rate of the associated market.

Oracles and floor prices could be manipulated by bad actors, if there is not sufficient modelling against price manipulation. Before participating in a market, lenders and borrowers should research how their oracle is configured, to properly evaluate risk.

## Unforeseen risk

Despite being regularly audited and reviewed open source, it's possible for Honey's programs to contain bugs and vulnerabilities, which could result in the loss of user funds.

Other risks associated with using DeFi protocols may not be known yet, and users should always act with extreme caution when participating in debt or DeFi protocols emulating debt instruments.
