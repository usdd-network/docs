# Key Features of Liquidation

**Trigger Mechanism**

* The protocol continuously monitors CDPs to assess their collateralization ratio.
* If the ratio falls below the minimum collateralization threshold, the liquidation process is initiated automatically.

**Auction Process**

* Liquidated collateral is put up for auction to a valid bidder.
* Bidders, often known as Keepers, compete to purchase the collateral, ensuring market-driven pricing.

**Liquidation Fee**

* A liquidation fee is imposed on the user whose position is liquidated.
* This liquidation fee is designed to discourage risky behavior and compensate the protocol for the added system risk.

**Keeper Rewards**

* Keepers are incentivized with rewards for participating in the liquidation process.
* Rewards typically include a portion of the liquidation fee and opportunities to acquire discounted collateral.

**Debt Repayment**

* The proceeds from the auction are used to repay the outstanding USDD debt.
* Any remaining collateral after repaying the debt and penalties is returned to the user.

**Peg Stability Impact**

* Liquidation ensures that excessive debt does not destabilize the peg of USDD.
* By swiftly resolving undercollateralized positions, the protocol maintains its financial health.
