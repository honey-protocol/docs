---
description: Calculating interest rates and risk
---

# Protocol maths

## Interest Rates

Interest rates on loans, also referred to as borrow APR, is calculated to reflect supply and demand for capital in lending markets. Supply is represented by lenders supplying liquidity or capital, and demand is represented by borrowers who seek capital in exchange for depositing collateral.

If there is an abundance of capital allocated to a market, more than is necessary, interest rates will be low. If however there is a shortage of capital in another market, which means strong demand with low supply, then interest will be higher.&#x20;

This incentivises capital to be allocated where it is most needed. Interest rates become a signal for lenders to indicate where money is most needed, and where in turn they can get the highest return on their capital.

This supply and demand for liquidity is measured with the **utilisation rate**, in other words, how much of the supplied liquidity is being borrowed (utilised) by borrowers. The higher the utilisation rate, the higher the interest rate in a lending market.

{% hint style="info" %}
_Ut_ = utilisation rate at time _t_\
_Uoptimal_ = optimal utilisation rate\
\
_Rv_ = variable borrow rate\
_Rv0_ = base variable borrow rate (interest when utilisation = 0%)\
_Rslope1_ = constant which determines the progression of the interest rate **until** Uoptimal\
_Rslope2_ = constant which determines the progression of the interest rate **after** Uoptimal
{% endhint %}

The protocol has built in incentives in the interest rate model. To be capitally efficient, it sets an _optimal utilisation rate._ Below this rate, the protocol will incentivise utilisation, above this rate and it will disincentivise utilisation.

Two different slopes are used to measure interest rates, one for when utilisation is below optimal, and one for when it is above the optimal rate.



When not enough borrowers are borrowing available liquidity, the interest rate will be calculated as such:

$$
R_v =R_{v0} + (U_t \div U_{optimal}) \times R_{slope1}
$$

When too many borrowers are borrowing available liquidity, the interest rate will be calculated as such:

$$
R_v = R_{v0} + R_{slope1}+(U_t - U_{optimal})\div(1-U_{optimal})\times R_{slope2}
$$



## Protocol parameters

Honey Finance lending markets use the following parameters as default:

{% hint style="info" %}
**Optimal utilisation**: `80%`\
**Borrow APR at Uoptimal**: `40%`\
**Base borrow APR**: `10%`\
\
**Rslope1 constant**: `0.3`\
**Rslope2 constant**: `1`
{% endhint %}

You can try these parameters out for yourself and test models [here](https://share.streamlit.io/simeongk/interest-rates/main.py).
