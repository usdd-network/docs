# Oracle

An oracle module is deployed for each collateral type, feeding it the price data for a corresponding collateral type to the `Vat`. Every oracle module contains three main contracts: `Median, OSM, Spot`.

### Procedure

1. Median computes a price from a list of supported price feeds.
2. OSM updates the current price and the next price according to the price from Median.
3. Spot reads the current price from OSM and updates `ilk.spot` in `vat`.

_USDD use Chainlink and WinkLink Data Feeds as its primary Oracles._
