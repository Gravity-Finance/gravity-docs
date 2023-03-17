# Overview

Gravita Protocol is a decentralised borrowing protocol built on Ethereum that provides users with interest-free loans secured by both Liquid Staking Tokens (LST) and a Stability Pool (SP). <br/>
<br/>
Loans are issued in the form of minting **GRAI**, a token with similar volatility dampening mechanism as LUSD, and can be *up to 90%* of the value of a user's collateral.  You can find more information on the maximum LTV ratio of the supported assets in our [Collateral page](docs\2.HowDoesGravitaWork\Collateral.md). <br/>
<br/>
Gravita Protocol builds off [Liquity's economic model](https://github.com/liquity/dev) to ensure efficient borrowing and timely liquidations. A standard 0,5% borrowing fee is charged upfront on each new debt (or debt increase). In order to incentivize short-term borrowing, the fee is refunded if the user repays his debt before the expiry of six months (~182 days), pro rata for the time elapsed, but the minimum fee corresponds to one week worth of interest. You will find more informations on the [Fee Model page](/docs/2.HowDoesGravitaWork/Fee%20Model.md). <br/>
<br/>
Gravita has an unique multi-collateral design in which each position has a single collateral type, but they are all linked to the same stability pool:
 ![Gravita Multi-collateral type](/assets\multi-collateral.png)<br/>
<br/>
Borrowers mint GRAI against the value of their collateral. It can then be used in various ways - swapping for other assets, or earning income by providing liquidity or participating in the stability pool.<br/>
<br/>
In order to reduce the volatility of GRAI, a Liquity-like redemption mechanism will be enabled after launch. [Redemptions are made](docs\2.HowDoesGravitaWork\RedemptionsAndLiquidations.md) at a rate of 0.97 to 1 (the redeemer pays a 3% fee to the borrower).
<br/>
<br/>
Gravita Protocol is non-custodial and governance-minimised, with the goal of becoming immmutable.
