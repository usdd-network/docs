# PSM

### **Purpose**

Maintains USDD’s price peg by facilitating 1:1 swaps with other stablecoins (e.g., USDT).

### Key Responsibilities

* Reduces volatility during market imbalances.
* Offers zero-slippage swaps with no fees.

### Key Methods

* `sellGem(usr, wad)`\
  Allows users to exchange a stablecoin (`gem`) for USDD.
* `buyGem(usr, wad)`\
  Enables users to swap USDD for another stablecoin.
* `file(what, data)`\
  Sets PSM parameters such as swap limits or supported stablecoins.
