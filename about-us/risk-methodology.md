# Risk Methodology

The Honey protocol is built around 4 core principals:

* Decentralised pricing is the manifestation of risk in a market
* Risk must be compartmentalised
* In truly free markets, bad debt is the responsibility of market participants
* Fixed losses are more desirable than floating losses

Many design decisions stem from these principals, the sum of which has outlined a methodology for how risk is handled in Honey's various markets.

### Decentralised pricing

Interest rates on Honey are a function of supply and demand for liquidity inside of lending pools. Thus, a shortage or surplus in the supply of liquidity should be considered a signal from the market, as to the underlying risk contained within it.

This is especially important in permissionless markets, where the range of risk can be incredibly wide, and where curation is impossible.

The sum of borrowers and lenders interacting in free markets express a collective sentiment around collections regarding their underlying risk, a sentiment which is aggregated in a single figure, the interest rate.

### Risk Compartmentalisation

Honey uses Isolated Risk Markets (IRMs), meaning that debt and liquidity in a market is contained, and not spread throughout the protocol.

This isolation of risk safeguards the protocol from bad actors, and limits contagion during liquidation events. It allows lenders and borrowers the opportunity to tailor their actions according to their own risk profiles.

### Double-edged sword of responsibility&#x20;

If markets and their rates are independent, then collections with higher risk should attract less lenders, resulting in higher interest rates in riskier markets. Lenders participating in these markets carry this risk but also stand to benefit from the increased potential upside. As long as they equally participate in both the potential upside _and_ downside of respective markets, then the subsequent result of their speculation is their own doing, and DAOs, admins, and communities should not be called to intervene.

### Realisation of losses

The protocol's liquidation engine is built to liquidate by any means necessary, even if this constitutes a loss. The idea being that fixed losses can be managed in time as risk adjusts in a market. Fixed losses also become the responsibility of the market participants, instead of the liquidators, once again aligning incentives between potential upside and downside.

The protocol and DAO do not hold on to risk in the hopes of rising floor prices, but instead ensure the smooth and predictable operation of markets in volatile times, that is their primary task.

