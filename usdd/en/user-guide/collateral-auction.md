# Collateral Auction

When a Vault is liquidated, its collateral is moved into an auction process. Users can bid on the collateral at auction prices, potentially securing profits. The auction uses a Dutch auction model, where the price gradually decreases over time until a buyer places a bid or the auction ends.

#### Steps to Participate in an Auction

1.  **Navigate to the Auction Page**\
    Visit the Auction Page to explore ongoing auctions.

    <figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>
2. **View Auction Details**
   1. Access the details of the Vault undergoing auction.
   2. Review information about the collateral, debt, and current auction price.
3. **Stake USDD for Auction Participation**
   1. To bid, you must first stake USDD, which will be used for purchasing collateral in the auction.
   2. Staked USDD can be withdrawn anytime if not used for a bid.
4. **Place Your Bid**
   1. Enter the amount of USDD you wish to bid.
   2.  The platform will automatically calculate:

       1. Collateral Quantity: The amount of collateral you will receive, calculated as:\
          **Collateral Quantity = Input USDD Amount / Auction Price**
       2. Potential net Profit: The potential net profit you can earn if you sell the collateral at the current market price.

       Profit Calculation Formula:\
       **Potential Net Profit = Input USDD Amount \* Market Price - Input USDD Amount \* Auction Price - Transaction fee**

       <figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>
5. **Monitor Auction Prices**
   1. Since the auction follows the Dutch auction model, the price decreases over time.
   2. The page displays the current auction price and the time remaining before it decreases further.
6. **Complete the Purchase**
   1. If your bid is successful, you will acquire the collateral, which can be sold or used as desired. Any collateral obtained from auctions is stored in the liquidation auction account and can be withdrawn to the winning bidders’ wallet.
   2. The actual profit will depend on the market price when you decide to sell the collateral.

Participating in auctions is an excellent way to acquire assets at competitive prices and contribute to the USDD ecosystem.&#x20;

\
