---
layout: post
title: "November2024 - $MSTR | Leveraged ETFs via MSTR Volatility (MSTU & MSTX)"
date: 2024-11-21 23:59:59 -0000
categories: mstr degen mstu mstx
author: "Sagun Garg"
tags: mstr degen mstu mstx
---

## Leveraged ETFs: MSTU, MSTX

Over multiple days, the effects of daily leverage can compound in unexpected ways, especially in volatile markets, potentially leading to results that do not align perfectly with the leveraged multiple of the underlying asset's performance over longer periods due to volatility decay.

Leveraged ETFs like MSTU (2X Long MSTR Daily Target ETF) and MSTX (which initially offered 1.75X but now also 2X leverage) aim to deliver a multiple of the daily performance of MicroStrategy's (MSTR) stock. Below is a simple example to demonstrate how the effects of daily leverage can compound over time, leading to volatility decay:

| Day | MSTR Movement | MSTU Movement (2X) | MSTX Movement (2X) | MSTR Price | MSTU Price | MSTX Price |
|-----|---------------|--------------------|--------------------|------------|------------|------------|
| 1   | +5%           | +10%               | +10%               | 100        | 110        | 110        |
| 2   | -5%           | -10%               | -10%               | 95         | 99         | 99         |
| 3   | +5%           | +10%               | +10%               | 99.75      | 108.90     | 108.90     |
| 4   | -5%           | -10%               | -10%               | 94.76      | 98.01      | 98.01      |
| 5   | +5%           | +10%               | +10%               | 99.50      | 107.81     | 107.81     |

**Note:** The values are simplified and do not account for fees, daily rebalancing costs, or other market factors.

### Explanation:

- **Day 1:** MSTR goes up 5%, so MSTU and MSTX, both providing 2X leverage, go up 10%. MSTR ends at $100, while MSTU and MSTX end at $110.

- **Day 2:** MSTR drops by 5%. MSTU and MSTX drop by 10%. Now, MSTR is at $95, but MSTU and MSTX are at $99 because they are leveraged.

- **Day 3:** Another 5% increase. MSTR goes back to $99.75, but due to the compounding effect, MSTU and MSTX only reach about $108.90, not back to their original $110 because of the previous drop affecting the base for the next calculation.

- **Day 4:** A 5% decrease again. MSTR drops to approximately $94.76, while MSTU and MSTX fall further due to leverage, to about $98.01.

- **Day 5:** MSTR increases by 5%, reaching $99.50. However, MSTU and MSTX, because of the cumulative effect of volatility, are now at $107.81, showing they haven't kept pace with MSTR's overall performance due to the volatility decay.

### Volatility Decay Explained:

- **Volatility Decay:** This occurs because leveraged ETFs reset their leverage daily. If an asset like MSTR moves significantly up and down each day, even if it returns to its starting price over a period, the leveraged ETFs might not. This is due to the multiplicative effect of daily gains and losses which aren't linear over time.

- **Impact Over Time:** Over several days or longer, this daily rebalancing can lead to a performance divergence where the leveraged ETF might underperform or outperform the underlying asset in ways not directly proportional to their leverage factor, especially in volatile markets.

This table simplifies the concept but clearly shows how, over time, the performance of leveraged ETFs can deviate from the expected outcome based on the daily leverage ratio due to the inherent nature of compounding returns.

### So when I buy MSTX and MSTU, do I have to sell my position daily

No, you do not have to sell your positions in MSTX and MSTU daily when trading through Saxo in Singapore. Here are a few points to consider regarding these leveraged ETFs:

#### Leveraged ETFs: 
Both MSTX and MSTU are leveraged ETFs, meaning they aim to deliver multiples of the daily performance of MicroStrategy's stock. They are designed for short-term trading or speculation due to their daily reset mechanism. 
#### Daily Reset: 
Leveraged ETFs like MSTX and MSTU reset their leverage daily. This means they aim to achieve their stated leverage (e.g., 2x for MSTU) on a daily basis. However, this does not mean you must sell your position daily. You can hold your investment for longer periods, but be aware:
#### Over Time Effects: 
Over multiple days, the effects of daily leverage can compound in unexpected ways, especially in volatile markets, potentially leading to results that do not align perfectly with the leveraged multiple of the underlying asset's performance over longer periods due to volatility decay.
#### Holding Period: 
While you can hold these ETFs longer than a day, holding leveraged ETFs over an extended period can be risky due to the compounding effects of daily rebalancing. This is particularly relevant for products aiming to deliver daily performance multiples.
#### Trading Strategy: 
If you're using these for short-term speculation or aiming to capture daily movements in MicroStrategy's stock, you might engage in daily trading. However, for those looking at holding for a longer term, it's crucial to understand:
####  Risk Management: 
These products are not typically recommended for long-term holding due to the potential for significant deviations from the expected long-term performance of the underlying asset.

In summary, while there's no requirement to sell MSTX or MSTU daily, the nature of leveraged ETFs suggests they are best used for short-term trading strategies due to how they function with daily rebalancing. If you're considering holding these ETFs for longer periods, it's essential to fully understand the implications of leverage compounding over time.