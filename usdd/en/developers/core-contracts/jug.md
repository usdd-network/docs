# Jug

### **Purpose**

Calculates and accrues stability fees on minted USDD. These fees ensure protocol sustainability and discourage excessive borrowing.

### Key Responsibilities

* Accumulate stability fees for particular collateral types .
* Adjusts debt levels to reflect accrued interest.

### Key Methods

*   d`rip(ilk)`\
    Performs stability fee collection for a specific collateral type when it is called. Calls `Vat.fold` to update the collateral's rate, total tracked debt, and Vow surplus;

    duty: Annualized stability fee rate.
* `file(what, data) / file(what, ilk, data)`\
  Configures global and per-collateral stability fee rates.
  * Example Parameters:
    * `duty`: Annualized stability fee rate.
