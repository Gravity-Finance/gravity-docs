# Collateral

## Why would I use Gravita Protocol?

### 1. Capital efficency and Productive Collateral

Since less collateral is needed for the same loan, Gravita Protocl offers more capital efficiency than other decentralized lending platforms. Your LST continues to provide you with interest even when it is used as a collateral. This is also true for your DeFi positions that will be available to be used as a collateral in a future update.

Also, borrowers can increase their exposure to the LST of their choice by leveraging their position. 

For examble, the proceeds of loans issued in the form of GRAI can be used to purchase more collateral, that in return allows to mint more GRAI. 

__*This is not a recommendation on how to use Gravita Protocol, use leverage at your own risk!*__

### 2. Collateral LTV

You can find here the maximum amount of GRAI that you can borrow based on your LST collateral of choice. 
__*REMINDER: while Gravita Protocol is by design a multi-collateral lender, you can only borrow against a signle LST for each Vessel that you open. If you wish to borrow GRAI using different tokens, you will need to open a separate vessel each time*__
| Token       | Maximum LTV | 
| ----------- | ----------- | 
| WETH      | 90%       | 
| rETH   | 80%        | 
| wstETH   | 80%        |
| cbETH   | 70%        |

In addition mint caps are in place to ensure protocol stability. These numbers will be reviewed as the protocl grows and will be available [on the Gravita Protocl website.](https://www.gravitaprotocol.com/)  

WETH liquidations will always be total liquidations. That means that at an 80% LTV, the stability pool will capture those assets at a 20% discount. If the LTV reaches 70%, the discount becomes 30%, and so on.

### 3. Fixed 0% APR 
Many borrowing protocols like Compound and Aave offer a variable borrowing APR that is determined based on supply and demand. This can be quite inconvenient for users, since they need to constantly check their position to avoid liquidation. As shown recently, variable APR can increase quite drastically and suddenly, which can cause a sub-optimal user experience. 

With Gravita Protocol you can enjoy interest-free borrowing with a low maximum and fixed one time fee of 0.5% for positions longer than 6 months. Short term borrowers will be incentivized to use the protocol with a partial refund mechanism.

### 4. Fee refund for short term borrowers
When a user repays his debt before the expiry of six months (~182 days), the 0.5% fixed borrowing fee is refunded pro rata for the time elapsed, but at least one week worth of interest. 

The smart contract controls this decaying refund by immediately remitting the minimum fee (either to the Treasury or to a staking contract) and maintaining a record that includes the refund balance and the timestamp of the last change in the amount from the timestamp of the expiry date.

### 5. Peg Stability and Softer Redemptions
In order to reduce the volatility of GRAI, a Liquity-like redemption mechanism will be enabled after launch. [Redemptions are made](docs\2.HowDoesGravitaWork\RedemptionsAndLiquidations.md) at a rate of 0.97 to 1 (the redeemer pays a 3% fee to the borrower).

You can find more on the [Price Volatility and Peg](/docs/2.HowDoesGravitaWork/Price%20Volatilityand%20Peg.md) page.

### 6. Decentralization
Make a difference in the Ethereum ecosystem by supporting minority liquid staking tokens - especially those emphasizing decentralization.