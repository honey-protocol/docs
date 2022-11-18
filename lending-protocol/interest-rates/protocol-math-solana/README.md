# Protocol math (Solana)

Solana's programs use linear functions to derive interest rates. Thus, all of the interest rates on the Solana lending programs can be expressed as:

**`y = ax + b`**

Where **`y`** is the interest rate for a given utilisation rate **`x`**.

{% hint style="info" %}
Variable **`a`** is the slope of the curve, determining how fast or slow interest accrues given a change in utilisation.
{% endhint %}

```typescript
// Example of interest calculation when current utilisation is below 1st optimal rate 

interestRate = ((BORROW_RATE_ONE - BASE_BORROW_RATE) / ( OPTIMAL_RATIO_ONE - 0 )) * utilizationRate + (-1*((BORROW_RATE_ONE - BASE_BORROW_RATE) / ( OPTIMAL_RATIO_ONE - 0  )) * 0 + BASE_BORROW_RATE )

/* y = interestRate
 * a = (x2 - x1) / (y2-y1)
 * x = utilizationRate
 * b = -ax + y
 *
 * Meaning that:
 *
 * y = interestRate
 * a = ((BORROW_RATE_ONE - BASE_BORROW_RATE) / ( OPTIMAL_RATIO_ONE - 0 ))
 * x = utilizationRate
 * b = (-1*((BORROW_RATE_ONE - BASE_BORROW_RATE) / ( OPTIMAL_RATIO_ONE - 0  )) * 0 + BASE_BORROW_RATE )
*/ 
```

Varying risk parameters and collaterals will result in different values for `ax + b`&#x20;

```
// InterestRate.ts
// Parameters used in the default risk model

export const OPTIMAL_RATIO_ONE = 0.4;
export const OPTIMAL_RATIO_TWO = 0.8;
export const BASE_BORROW_RATE = 0.1;
export const BORROW_RATE_ONE = 0.25;
export const BORROW_RATE_TWO = 0.4;
export const BORROW_RATE_THREE = 1.4;
```
