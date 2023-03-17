# Stability Pool

## What is the Stability Pool?

The Stability Pool is the first line of defense in maintaining system solvency. It achieves that by acting as the source of liquidity to repay debt from liquidated Vessels—ensuring that the total GRAI supply always remains backed.

When any Vessel is liquidated, an amount of GRAI corresponding to the remaining debt of the Vessel is burned from the Stability Pool’s balance to repay its debt. In exchange, the entire collateral from the Vessel is transferred to the Stability Pool. 

The Stability Pool is funded by users transferring GRAI into it (called Stability Providers).

This allows for an interesting mechanic to play out: over time Stability Providers lose a pro-rata share of their GRAI deposits, while gaining a pro-rata share of the liquidated collateral. 

In the example of WETH Vessels, because those are likely to be liquidated at just below 110% collateral ratios, it is expected that Stability Providers will receive a greater dollar-value of collateral relative to the debt they pay off.

For more informations on the Collaterals that you can use with Graivta Protocol consult [this page](docs\2.HowDoesGravitaWork\Collateral.md)

## Why should I deposit GRAI to the Stability Pool?

Stability Providers will make liquidation gains. In the future, they will also receive GRVT tokens.

## What are liquidations?
To ensure that the entire stablecoin supply remains fully backed by collateral, Vessels that fall under the [minimum collateral ratio](docs\2.HowDoesGravitaWork\Collateral.md) will be closed (liquidated).

The debt of the Vessel is canceled and absorbed by the Stability Pool and its collateral distributed among Stability Providers.

The owner of the Vessel still keeps the full amount of GRAI borrowed but loses value overall hence it is critical to always keep the ratio above the protocol set amount.

## Who can liquidate Troves? 
Anybody can liquidate a Trove as soon as it drops below the Minimum Collateral Ratio of 110%. The initiator receives a gas compensation (200 GRAI + 0.5% of the Vessel's collateral) as reward for this service. This mechanism is in place to avoid excessive exposure of the liquidator to the gas costs that are incurred by performing this on-chain operation. 

Our UI currently does not offer the possibility to liquidate Troves. Please check our [Contract Adresses](docs\3.AboutGravitaProtocol\ContractAdresses.md) if you wish to implement a service for liquidating troves. 

The 200 GRAI is funded by a Liquidation Reserve while the variable 0.5% part comes from the liquidated collateral, slightly reducing the liquidation gain for Stability Providers.

## How do I benefit as a Stability Provider from liquidations?

As liquidations happen just below a [predefined collateral ratio](docs\2.HowDoesGravitaWork\Collateral.md), you will most likely experience a net gain whenever a Vessel is liquidated. 

Let’s say there is a total of `1,000,000 GRAI` in the Stability Pool and your deposit is `100,000 GRAI`. 
Now, a Vessel with debt of `200,000 GRAI` and collateral of `400 WETH` is liquidated at an Ether price of `$545`, and thus at a collateral ratio of `109% (= 100% * (400 * 545) / 200,000)`. Given that your pool share is `10%`, your deposit will go down by `10%` of the liquidated debt (20,000 GRAI), i.e. from `100,000` to `80,000 GRAI`. In return, you will gain `10%` of the liquidated collateral, i.e. `40 WETH`, which is currently worth `$21,800`. Your net gain from the liquidation is `$1,800`. 

## Can I withdraw my deposit whenever I want?
As a general rule, you can withdraw the deposit made to the Stability Pool at any time. There is no minimum lockup duration. However, withdrawals are temporarily suspended whenever there are liquidatable Vessels with a collateral ratio below the amount set by the protocol that have not been liquidated yet.

## What oracle are you using to determine the price of ETH?

TBD: chainlink?

## Can I lose money by depositing funds to the Stability Pool?

While liquidations will occur at a collateral ratio well above 100% most of the time, it is theoretically possible that a Vessel gets liquidated below 100% in a flash crash or due to an oracle failure. In such a case, you may experience a loss since the collateral gain will be smaller than the reduction of your deposit. 

If GRAI is trading above $1, liquidations may become unprofitable for Stability Providers even at collateral ratios higher than 100%. However, this loss is hypothetical since GRAI is expected to return to the peg, so the “loss” only materializes if you had withdrawn your deposit and sold the GRAI at a price below $1.

Please note that although the system is diligently audited, a hack or a bug that results in losses for the users can never be fully excluded.

## What happens if the Stability Pool is empty when liquidations occur? 

If the Stability Pool is empty, the system uses a secondary liquidation mechanism called redistribution. In such a case, the system redistributes the debt and collateral from liquidated Troves to all other existing Vessels. The redistribution of debt and collateral is done in proportion to the recipient Vessel's collateral amount. 