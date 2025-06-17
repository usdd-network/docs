# The PSM

## Motivation

USDD’s core mission is to provide the blockchain world with an Over-Collateralized Decentralized Stablecoin. As the custodian of the USDD, The TRON DAO RESERVE(TDR) has adopted a series of monetary policies to maintain the USDD’s price stability and spur growth in the TRON ecosystem based on the market conditions, and the TDR has always been intensively working on how to further ensure the USDD’s price stability, and drive the continued growth of the USDD ecosystem.

The PSM solution has already been tested and used extensively in the industry, Thus, it can be one of the monetary policies to maintain the stability of USDD’s price. The TDR will introduce the new Peg Stability Module(PSM) for the USDD ecosystem, which actually goes a step further on the stability improvement of the USDD price. At the same time, providing safer and more stable infrastructure for the USDD ecosystem, and jointly promotes the sustainable and healthy development of the USDD ecosystem.

## **PSM Mechanism**&#x20;

As a USDD fixed ratio SWAP module, PSM allows users to exchange USDT/USDC/TUSD/USDJ  to USDD at a fixed ratio of 1:1. Similarly, it also allows users to exchange USDD to USDT/USDC/TUSD/USDJ  at a fixed ratio of 1:1. During the entire exchange process, users do not need to undertake any debt and management tasks. More importantly, PSM has an excellent experience of 0 slippage and 0 handling fee, which helps the USDD price to stabilize at around 1 USD.

The PSM mechanism perfectly combines the USDD issuance mechanism and introduces a new issuance method for USDD. the current USDD issuance process mainly consists of the following three steps (Please refer to the white paper for a detailed description of the issuance process).

1. TDR members deposit TRX to the **TRX Burning Contract**.&#x20;
2. TDR will calculate the equivalent US dollars according to the current exchange ratio, and transfer the equivalent TRC-10 USDD from the **Authorized Contract** to the circulation account via multi-signature.&#x20;
3. The TDR converts TRC-10 USDD in the circulation account into TRC-20 USDD and then transfers the USDD to TDR members.

With the newly introduced PSM,  the process of USDD SWAP is actually the process of USDD issuing via the fixed ratio collateralizing. All PSM users actually participate in the issuance of USDD. The detailed process is as follows:&#x20;

1. TDR releases the authorized and unissued TRC-10 USDD from the authorization contract to the **safeVault** contract of PSM.&#x20;
2. When PSM executed the USDT/USDC/TUSD/USDJ → USDD SWAP, it will convert TRC-10 USDD in **safeVault** to TRC-20 USDD and release it to users. In reverse conversion, TRC-20 USDD will be converted into TRC-10 USDD and transferred to the **safeVault** contract.

Note: The TRC-10 USDD in **safeVault** will not affect the total supply of USDD. Only when the exchange is completed, the total supply will change accordingly.&#x20;

* Increase the total supply: When users successfully convert USDT/USDC/TUSD/USDJ into USDD, the total supply of USDD will increase accordingly.&#x20;
* Reduced the total supply: When users successfully convert USDD into USDT/USDC/TUSD/USDJ, the total supply of USDD will be reduced accordingly.

#### PSM Contracts

VAT \*                       [ TBbYhvifBJVQ5ytThJ5ZfHfX8mK133ccqv](https://tronscan.org/#/contract/TBbYhvifBJVQ5ytThJ5ZfHfX8mK133ccqv)

USDDJoin \* [         TUhQDzXJ3QsT6F2KiK5gZ3H673TV1516E9](https://tronscan.org/#/contract/TUhQDzXJ3QsT6F2KiK5gZ3H673TV1516E9)

GemJoin \*      [      TMn5WeW8a8KH9o8rBQux4RCgckD2SuMZmS](https://tronscan.org/#/contract/TMn5WeW8a8KH9o8rBQux4RCgckD2SuMZmS)

USDT PSM \*     [    TM9gWuCdFGNMiT1qTq1bgw4tNhJbsESfjA](https://tronscan.org/#/contract/TM9gWuCdFGNMiT1qTq1bgw4tNhJbsESfjA)

USDT Quota \*  [     TEVuAK3cXeG93wJLE2Hv4U2sx69hFovnjU](https://tronscan.org/#/contract/TEVuAK3cXeG93wJLE2Hv4U2sx69hFovnjU)

USDC GemJoin \*  [TRGTuMiDYAbztetdndYyMzYvtaRmucjz5q](https://tronscan.org/#/contract/TRGTuMiDYAbztetdndYyMzYvtaRmucjz5q)

USDC PSM \*         [TUcj1rpMgJCcFZULyq7uLbkmfh9xMnYTmA](https://tronscan.org/#/contract/TUcj1rpMgJCcFZULyq7uLbkmfh9xMnYTmA)

USDC Quota \*       [TQnAGXspTiqJVvdNqUk8giSBFW4Ykt2Gxm](https://tronscan.org/#/contract/TQnAGXspTiqJVvdNqUk8giSBFW4Ykt2Gxm)

TUSD GemJoin \*   [TPxcmB9dQC3LHswCNEc4rJs1HFGb8McYjT](https://tronscan.io/#/contract/TPxcmB9dQC3LHswCNEc4rJs1HFGb8McYjT)

TUSD PSM \*          [TY2op6AKcEkFhv8hxNJj3FBUfjManxYLSe](https://tronscan.io/#/contract/TY2op6AKcEkFhv8hxNJj3FBUfjManxYLSe)

TUSD Quota \*        [TSApGmpYaPqKrQahjzbs7yrMjobSfugpXT](https://tronscan.io/#/contract/TSApGmpYaPqKrQahjzbs7yrMjobSfugpXT)  &#x20;

USDJ GemJoin \*    [TKAovR61zwp1t9Rg1UE4UY5mXt7QTJdDXg](https://tronscan.io/#/contract/TKAovR61zwp1t9Rg1UE4UY5mXt7QTJdDXg)

USDJ PSM \*           [TVS3rVDUSd3ySeXV5moRH2J2t5B9reJfLR](https://tronscan.io/#/contract/TVS3rVDUSd3ySeXV5moRH2J2t5B9reJfLR)

USDJ Quota \*        [TMdUs66Y4GQjdsPLkDPu2bmDVze6ErZSFY ](https://tronscan.io/#/contract/TMdUs66Y4GQjdsPLkDPu2bmDVze6ErZSFY/code)&#x20;

safeVault                [TMgSSHn8APyUVViqXxtveqFEB7mBBeGqNP](https://tronscan.org/#/contract/TMgSSHn8APyUVViqXxtveqFEB7mBBeGqNP)

&#x20;\* This contract is controlled by multiple signatures, managed by 7 different TDR members, and the transaction is valid when 5 of them have signed.

## Why PSM&#x20;

### Improve the price stability of USDD through a stable peg&#x20;

The number one objective of the TDR is to maintain the price stability of USDD and secure the USDD peg close to $1 U.S. dollar. PSM as a fixed exchange ratio swap module (allowing users to exchange between USDT/USDC/TUSD/USDJ and USDD at a ratio of 1:1) is an important step in achieving this goal, introducing a more stable Peg for USDD, increasing the stability of USDD pice.

The arbitrage mechanism will also help to maintain price stability. When the USDD price deviates from the USD price, there is an arbitrage opportunity in the market.

* When USDD's price < 1 USD, for example 1 USDD = 0.9 USD, an arbitrageur can buy 1 USDD with 0.9 USD in the external market and then swap 1 USDD for 1 USD stablecoin in the PSM. In this way, the arbitrageur spends 0.9 USD to get 1 USD and earns 0.1 USD without taking any risks. As a result of the above arbitrage, USDD's price will increase, to the point where there is no room for arbitrage and 1 USDD re-equates to 1 USD.&#x20;
* When USDD's price > 1 USD, for example 1 USDD = 1.1 USD, an arbitrageur can pay 1 USD stablecoin for 1 USDD in the PSM. After that, the arbitrageur can sell 1 USDD in the external market at 1.1 USD. The arbitrageur spends 1 USD to get 1.1 USD and earns 0.1 USD without taking any risks. As a result of the above arbitrage, USDD's price will go down, to the point where there is no room for arbitrage and 1 USDD re-equates to 1 USD.

At the same time, the PSM module will also accumulate a large amount of USDT/USDC/TUSD/USDJ as collateral to stabilize the price of USDD. After PSM supports more stablecoins in the future, the stabilization effect will be strengthened with the increase of the number of stablecoins and the increase of the collateral scale. The collateral also provides very considerable liquidity for the USDD ecosystem, providing a reliable source for the sale of USDD, and its stable peg will also help to mint more USDD. At the same time, different stablecoins can also be exchanged with each other via the USDD, thus helping the system to quickly restore balance.

### **New Application Scenarios**

While stabilizing the USDD price, PSM also provides a new trading hub between different stablecoins. After the introduction of multiple stablecoins in PSM, each stablecoin can be exchanged at a low cost of a 1:1 ratio through USDD as an intermediary, which also brings a new application scenario to the USDD ecosystem. The integration of PSM can easily realize a stablecoins swap, which will ultimately help to improve the overall liquidity of the DeFi ecosystem.



### **A reliable signal for USDD ecological governance**&#x20;

Adjusting the USDD interest ratio according to market dynamics is also one of the most important monetary policies of TDR, to achieve the goal of long-term stable growth of the USDD market. Since changes in market dynamics are immediately reflected in the balance of USDT/USDC/TUSD/USDJ and USDD in PSM, the PSM module also provides a reliable signal for interest ratio adjustments. With the powerful concept of PSM, it can provide more possibilities and directions for the USDD ecosystem governance.

## Governance&#x20;

The governance of PSM is mainly accomplished by adjusting the parameters of the smart contract. In extreme market conditions, PSM can adjust the corresponding parameters of the smart contract according to the real-time market conditions to deal with the extreme challenge from the market, protect the asset safety of investors and users, and maintain the market stability. In general, the most core parameter in the entire governance is Swap Limit. It can be used to control the maximum amount of USDD that can be exchanged in the system.&#x20;

At the same time, supporting multiple stablecoins can also be seen as an important means of risk management, spreading risks among multiple stablecoins rather than concentrating them in one stablecoin.&#x20;

The PSM Fee parameter can also be a governance method. This parameter allows PSM to charge a small fee for each transaction. On the one hand, it can better balance the market, and at the same time, the fee can also help PSM achieve better governance.



## Key Parameters&#x20;

### Swap Limit (line)&#x20;

The Swap Limit refers to the maximum USDD limit that can be exchanged globally in PSM.

### Fee In (tin)&#x20;

The percentage fee is applied when trading the USDT/USDC/TUSD/USDJ into the PSM in exchange for USDD.&#x20;

### Fee Out (tout)&#x20;

The percentage fee is applied when trading USDD into the PSM in exchange for the USDT/USDC/TUSD/USDJ.&#x20;

## User Interaction&#x20;

Users can find the PSM portal from:&#x20;

* [usdd.io](https://usdd.io/#/psm)
* [tdr.org ](https://tdr.org/#/)
* [sun.io ](https://sun.io/?lang=en-US#/psm)

Users can choose to complete the SWAP through the PSM portal, or directly call the PSM contract to complete the exchange. For the Defi projects, it is super easy to integrate PSM into the DEX aggregator to complete the transaction.

## Considerations&#x20;

The number of transactions that a PSM can offer is limited by the Swap Limit and the number of stablecoins available in the liquidity pool. If PSM has reached the exchange limit, it cannot offer USDT/USDC/TUSD/USDJ → USDD exchange transactions. Likewise, if there is not enough USDT/USDC/TUSD/USDJ in the PSM, then the PSM cannot complete the USDD → USDT/USDC/TUSD/USDJ exchange.
