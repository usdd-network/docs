# USDD Issuance

## Introduction

As introduced in the whitepaper, [#9-usdd-issuance-in-1.0-space](../usdd-whitepaper.md#9-usdd-issuance-in-1.0-space "mention"), USDD is now in USDD 1.0 phase. At this phase, the TRON DAO Reserve pre-issues 999 billion TRC-10 USDD and transfers 1 billion of them to the Authorized Contract, the remaining 998 billion USDD will be transferred and locked in the Issuance Contract. Once the USDD amount in the authorized contract falls below 500 million, the TDR will release [TRC-10 USDD](https://tronscan.org/#/token/1004777) from [Issuance Contract \*](https://tronscan.org/#/contract/TRFGnuUqED3NDpMYgqZY1X3gAeVHNw1SDq) to [Authorized Contract \*](https://tronscan.org/#/contract/TTsASxQhMk4t3S5vZMVVJ7nR2GQjDXNRnq) via multi-signature. The USDD Issuance process is actually the process of converting the TRC-10  USDD to the TRC-20 USDD and releasing the TRC-20 USDD to the users from the Authorized Contract.

At the beginning of the USDD 1.0 phase, the TRON DAO Reserve and its members (whitelisted institutions) issue the USDD by staking TRX. With the thriving of the USDD ecosystem, TDR introduced a new Peg Stability Module(PSM) for the USDD ecosystem, which allows all PSM users can participate in the USDD issuance. Now, the USDD can be issued with the following two ways:

1. TDR and its members issue the USDD via staking TRX.
2. Issue the USDD via PSM.

The detailed issuance process is shown in the figure below. The upper part of the figure shows TDR and its members issue the USDD via staking TRX, and the lower part shows issue USDD through PSM. In both ways, USDD must be released by Authorized Contract.

<figure><img src="../.gitbook/assets/web - 英文.png" alt=""><figcaption></figcaption></figure>

## Issuance Process

### Issue the USDD by staking TRX

Before the PSM, TDR and its members issued the USDD by staking the TRX. Until August 16, 2022, the TDR and its members have cumulatively issued approximately 725 Million USDDs, These USDDs circulate in multiple mainstream blockchains and are available on multiple mainstream markets, below is the Issuance process:

1\. TDR and its Members deposit TRX into [TRX Burning Contract \*](https://tronscan.org/#/address/TNMcQVGPzqH9ZfMCSY4PNrukevtDgp24dK).

2\. The TDR calculates the dollar value of the TRX based on the prevailing exchange ratio and transfers an equivalent dollar value of [TRC-10 USDD](https://tronscan.org/#/token/1004777) from [Authorized Contract \*](https://tronscan.org/#/address/TTsASxQhMk4t3S5vZMVVJ7nR2GQjDXNRnq) to the circulation account via multi-signature.

3\. The TDR converts [TRC-10 USDD](https://tronscan.org/#/token/1004777) in the circulation account into [TRC-20 USDD](https://tronscan.org/#/token20/TPYmHEhy5n8TCEfYGqW2rPxsghSfzghPDn) and then transfers the USDD to the TDR members.

#### Contracts & USDD Token Addresses are as follows.

TRC-10 USDD                     [ID: 1004777](https://tronscan.org/#/token/1004777)

TRC-20 USDD                    [TPYmHEhy5n8TCEfYGqW2rPxsghSfzghPDn](https://tronscan.org/#/token20/TPYmHEhy5n8TCEfYGqW2rPxsghSfzghPDn)

TRX Burning Contract      \*[TNMcQVGPzqH9ZfMCSY4PNrukevtDgp24dK](https://tronscan.org/#/address/TNMcQVGPzqH9ZfMCSY4PNrukevtDgp24dK)

Issuance Contract            \*[TRFGnuUqED3NDpMYgqZY1X3gAeVHNw1SDq](https://tronscan.org/#/address/TRFGnuUqED3NDpMYgqZY1X3gAeVHNw1SDq)

Authorized Contract         \*[TTsASxQhMk4t3S5vZMVVJ7nR2GQjDXNRnq](https://tronscan.org/#/address/TTsASxQhMk4t3S5vZMVVJ7nR2GQjDXNRnq)

\* This contract is controlled by multiple signatures, managed by 7 different TDR members, and the transaction is valid when 5 of them have signed.

### Issue the USDD via PSM

As a USDD fixed ratio SWAP module, PSM allows users to exchange USDT/USDC/TUSD to USDD at a fixed ratio of 1:1. Similarly, it also allows users to exchange USDD to USDT/USDC/TUSD at a fixed ratio of 1:1.&#x20;

The PSM mechanism perfectly combines the USDD issuance mechanism and introduces a new issuance method for USDD.  The PSM USDD issuance process mainly consists of the following two steps (Please refer to the white paper for a detailed description of the issuance process).

1. TDR releases the authorized and unissued TRC-10 USDD from the **Authorization Contract** to the **safeVault** contract of PSM.&#x20;
2. When PSM executed the USDT/USDC/TUSD → USDD SWAP, it will convert TRC-10 USDD in **safeVault** to TRC-20 USDD and release it to users. In the reverse conversion, TRC-20 USDD will be converted into TRC-10 USDD and transferred to the **safeVault** contract.

Note: The TRC-10 USDD in **safeVault** will not affect the total supply of USDD. Only when the exchange is completed, the total supply will change accordingly.&#x20;

* Increase the total supply: When users successfully convert USDT/USDC/TUSD into USDD, the total supply of USDD will increase accordingly.&#x20;
* Reduced the total supply: When users successfully convert USDD into USDT/USDC/TUSD, the total supply of USDD will be reduced accordingly.

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

USDJ Quota \*        [TMdUs66Y4GQjdsPLkDPu2bmDVze6ErZSFY ](https://tronscan.io/#/contract/TMdUs66Y4GQjdsPLkDPu2bmDVze6ErZSFY/code)

safeVault                [TMgSSHn8APyUVViqXxtveqFEB7mBBeGqNP](https://tronscan.org/#/contract/TMgSSHn8APyUVViqXxtveqFEB7mBBeGqNP)

&#x20;\* This contract is controlled by multiple signatures, managed by 7 different TDR members, and the transaction is valid when 5 of them have signed.

## Replenish Reserves of Authorized Contract

Once the amount of USDD reserved in the **Authorized Contract** falls below 500 million, the TDR will automatically replenish the reserves. The TDR will release[ TRC-10 USDD](https://tronscan.org/#/token/1004777) from[ Issuance Contract \*](https://tronscan.org/#/contract/TRFGnuUqED3NDpMYgqZY1X3gAeVHNw1SDq) to[ Authorized Contract \*](https://tronscan.org/#/contract/TTsASxQhMk4t3S5vZMVVJ7nR2GQjDXNRnq) via multi-signature. After the transaction receives five out of seven signatures, USDD will be locked for a minimum of 10 days.

Until August 16, 2022, the total amount of USDD released from [Issuance Contract \*](https://tronscan.org/#/contract/TRFGnuUqED3NDpMYgqZY1X3gAeVHNw1SDq) to [Authorized Contract \*](https://tronscan.org/#/contract/TTsASxQhMk4t3S5vZMVVJ7nR2GQjDXNRnq) is 2 billion, with 1,274,667,957 of these USDD authorized but not issued.



