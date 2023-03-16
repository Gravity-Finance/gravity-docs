# Overview

###### Please review our Disclaimer and Terms of Service before using the Gravita Protocol or interacting with GRAI. Gravita Protocol and GRAI are not available in the U.S.
Gravita Protocol is a decentralised borrowing protocol built on Ethereum that provides users with interest-free loans secured by both liquid staking derivatives (LST) and a Stability Pool (SP). <br/>
<br/>
Loans are issued in the form of a USD-pegged stablecoin, **GRAI**, and can be *up to 90%* of the value of a user's collateral.  You can find more informations on the maximum LTV ratio of the supported assets in our Collateral page. <br/>
<br/>
Gravita Protocol builds off [Liquity's economic model](https://github.com/liquity/dev) to ensure peg stability and efficient liquidations. A standard 0,5% borrowing fee is charged upfront on each new debt (or debt increase). In order to incentivize short-term borrowing, the fee is refunded if the user repays his debt before the expiry of six months (~182 days), pro rata for the time elapsed, but the minimum fee corresponds to one week of interest. You will find more informations on the Fee Model page.<br/>
<br/>
Gravita has an unique multi-collateral design in which each position has a single collateral type, but they are all linked to the same stability pool:
 ![Gravita Multi-collateral type](/assets/multi-collateral.png)<br/>
<br/>
Borrowers receive GRAI at a minimum ratio of 1 GRAI to 1 USD in collateral. Users will then be able to use the GRAI to purchase additional assets, hedge their position, or provide liquidity for additional rewards.<br/>
<br/>
In order to prevent GRAI from being over-peg and to incentivize stability through borrowers, redemptions are made at a rate of 0.97 to 1 (the redeemer pays a 3% fee to the borrower).<br/>
<br/>
Gravity Protocol is non-custodial, immutable and governance-minimised.
