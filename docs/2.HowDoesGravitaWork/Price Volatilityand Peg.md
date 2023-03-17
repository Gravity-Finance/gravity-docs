# Price Volatility and Peg

## How does GRAI closely follow the price of USD?

Because of it's design, it is likely that GRAI will follow USD price in a -3%/+10% range. It has been defined as a *volatility dampened token*. This happens through a combination of mechanisms defined below:

### Hard peg
The ability to redeem GRAI for collateral at 0.97 (i.e. 1 GRAI for $0.97 worth of collateral) and to mint GRAI at a 110% against WETH creates a price floor and price ceiling respectively through arbitrage opportunities. We call these "hard peg mechanisms" since they are based on direct processes. This offers to the user a more forgiving margin of error to avoid liquidation. More importantly, it allows GRAI to not regularly be over peg, which can over time make the implementation of GRAI as a stable-coin less desirable.

### Soft peg
GRAI also benefits from less direct mechanisms for USD parity — called "soft peg mechanisms".  As the price of GRAI fluctuates below and above 1 USD, opportunnities arise for both borrowers and depositors. Redemptions happen at an increasing rate depending on the price of GRAI. 

Another of these mechanisms is parity as a Schelling point. Since Gravita Protocol treats 1 GRAI as being equal to 1 USD, parity between the two is an implied equilibrium state of the protocol. 
