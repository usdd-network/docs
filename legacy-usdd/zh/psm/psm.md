# PSM

## 背景

USDD 的核心使命是为区块链行业提供一种去中心化超抵押稳定币。作为 USDD 的初始托管人，波场联合储备（以下简称“TDR”）根据市场情况不仅采取了一系列货币政策来维持 USDD 的价格稳定，且一直致力于探索新的方式来提升 USDD 价格的稳定性，促进 USDD 生态系统的持续增长。

PSM 解决方案已经在行业中得到了广泛的测试和使用，因此也可以作为稳定 USDD 价格的货币政策，TDR 将为 USDD 引入全新的 Peg Stability Module（以下简称“PSM”） 模块，从而进一步的提升 USDD 价格的稳定性，为 USDD 生态提供更安全，价格更稳定的基础设施，共同推动 USDD 生态持续健康的发展。

## PSM 机制&#x20;

PSM 作为 USDD 固定汇率货币兑换模块，允许用户通过此功能以 1:1 固定汇率将 USDT/USDC/TUSD/USDJ 兑换为 USDD，同理，也允许用户以1:1 固定汇率将 USDD 兑换为 USDT/USDC/TUSD/USDJ。整个兑换过程中，用户无需承担任何债务和管理任务，更重要的是，PSM 将为用户提供零滑点、零手续费的卓越体验，帮助 USDD 价格稳定在 1 美元附近。

PSM 的实现机制完美的结合了 USDD 发行机制，为 USDD 引入了一种新的发行方式。现阶段 USDD 的发行过程主要有以下三步（更详细的发行流程介绍参看白皮书）。&#x20;

1. TDR 机构成员将 TRX 转入 TRX 销毁合约。
2. TDR 根据当时汇率计算等值美元，以多重签名的方式从授权合约转移等值 TRC-10 USDD 到流通账户。&#x20;
3. TDR 将流通账户中的 TRC-10 USDD 转换成 TRC-20 USDD 后，转账给机构成员完成 USDD 发行。

引入 PSM 之后，用户使用 PSM 兑换 USDD 的过程，也是以“固定比率抵押的方式发行 USDD” 的过程。借助 PSM 普通用户也能参与到 USDD 的发行。 详细过程如下：&#x20;

1. TDR 将授权合约中已授权未发行的 TRC-10 USDD 释放到 PSM 的 **safeVault** 合约。&#x20;
2. PSM 在执行 USDT/USDC/TUSD/USDJ → USDD 的兑换时，会将 **safeVault** 中的 TRC-10 USDD 转为 TRC-20 USDD 并释放给用户。反向兑换时，会将TRC-20 USDD 转换为 TRC-10 USDD 并转至 **safeVault** 合约；

注： safeVault 中的 TRC-10 USDD 并不会影响 USDD 的实际发行量，只有兑换完成的时候，发行量才会相应的变化。

* 增加发行量：当用户成功将 USDT/USDC/TUSD/USDJ 兑换成 USDD 的时候， USDD 的发行量会相应的增加。&#x20;
* 减少发行量：当用户成功将 USDD 兑换成 USDT/USDC/TUSD/USDJ 的时候， USDD 的发行量会相应的减少。

#### PSM合约地址&#x20;

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

TUSD Quota \*        [TSApGmpYaPqKrQahjzbs7yrMjobSfugpXT](https://tronscan.io/#/contract/TSApGmpYaPqKrQahjzbs7yrMjobSfugpXT)     &#x20;

USDJ GemJoin \*    [TKAovR61zwp1t9Rg1UE4UY5mXt7QTJdDXg](https://tronscan.io/#/contract/TKAovR61zwp1t9Rg1UE4UY5mXt7QTJdDXg)

USDJ PSM \*           [TVS3rVDUSd3ySeXV5moRH2J2t5B9reJfLR](https://tronscan.io/#/contract/TVS3rVDUSd3ySeXV5moRH2J2t5B9reJfLR)

USDJ Quota \*        [TMdUs66Y4GQjdsPLkDPu2bmDVze6ErZSFY ](https://tronscan.io/#/contract/TMdUs66Y4GQjdsPLkDPu2bmDVze6ErZSFY/code)

safeVault                [TMgSSHn8APyUVViqXxtveqFEB7mBBeGqNP](https://tronscan.org/#/contract/TMgSSHn8APyUVViqXxtveqFEB7mBBeGqNP)

&#x20;\*  此合约由多重签名控制，由 7 个不同机构成员共同管理，签名条件为 5/7。

## 为什么要使用 PSM？&#x20;

### 通过稳定的挂钩进一步稳定 USDD 的价格&#x20;

TDR 一直以来都将稳定 USDD 的价格（即确保 USDD 价格锚定在1美元附近）作为自己的首要目标。PSM 作为一个固定汇率货币兑换模块（允许用户在 USDT/USDC/TUSD/USDJ 和 USDD 之间以1:1的比例进行交换）为 USDD 引入了一个更稳定的挂钩，从而达到提升 USDD 价格的稳定性的目标。&#x20;

此外，即时的套利机制也将有助于 USDD 价格维持稳定，当 USDD 价格偏离 USD 价格时，市场就出现了套利机会。

* 当 USDD 的价格 < 1USD 时，例如 1USDD = 0.9USD 时，套利者在外部市场支付 0.9USD 购买 1USDD，然后在 PSM 中将1USDD换成1USD的稳定币，套利者花费 0.9USD 得到 1USD，可以获利 0.1USD的无风险利润。经过上述套利后，会抬高外部市场 USDD 的市场价格，当 USDD 价格接近 1USD 时，将失去套利空间，同时 USDD 价格实现了与 USD 挂钩。&#x20;
* 当 USDD 的价格 > 1USD 时，例如 1USDD = 1.1USD 时，套利者在PSM中将 1USD的稳定币兑换成 1USDD，然后在外部市场支付 1USDD 购买 1.1USD 的稳定币，套利者花费 1USD 得到 1.1USD，可以获利0.1USD 的无风险利润。经过上述套利后，会导致 USDD 的价格下降，当 USDD 价格接近 1USD 时，将失去套利空间，同时 USDD 价格实现了与 USD 挂钩。

与此同时，PSM 模块也将累积大量 USDT/USDC/TUSD/USDJ 作为抵押物来稳定 USDD 的价格，后续 PSM 支持更多稳定币后，稳定效果会随着币种的增多和抵押规模的增大而加强， 同时，大量的抵押物也为 USDD 生态提供了非常可观的流动性，为 USDD 的出售提供了可靠来源，稳定的挂钩，也将有助于发行更多的 USDD 。与此同时，借助 USDD ，不同的稳定币之间也可以实现互相兑换，从而帮助系统迅速恢复平衡。

### **新的应用场景**

PSM 在稳定价格的同时，也为不同稳定币之间提供了一个新的交易中心。后续 PSM 中引入多个稳定币后，每个稳定币都可以通过 USDD 作为中介进行 1:1 的低费用兑换，这也为 USDD 生态系统带来全新的应用场景。集成 PSM 可以轻松实现稳定币之间的兑换需求，最终也将有助于提升 DeFi 生态系统的整体流动性。

### **为 USDD 生态治理提供可靠的链上信号**

根据市场动态变化而调整 USDD 的利率也是 TDR 最重要的货币政策之一，以达到 USDD 市场的长期稳定增长的目标。由于市场动态的变化会立即反映在 PSM 中的USDT，USDC，TUSD，USDJ和 USDD 的余额上， PSM 模块也为利率调整提供了一个可靠的信号。借助 PSM 这一强大的概念，可为 USDD 生态治理提供更多可能性和方向。



## 治理

PSM 的治理主要是通过调整智能合约的参数的方式完成，极端市场情况下，PSM 可根据市场实时情况调整智能合约相应的参数以应对市场的极端变化，保障投资者和用户的资产安全，维护市场的稳定。总体来说，Swap Limit 是整个治理中最核心的参数， 可以用来控制系统最大可兑换的 USDD 的数量。 与此同时，支持多种稳定币也可以看作是风险管理的重要手段，它将风险分散在多个稳定币中而不是集中在一个稳定币中。

调整 PSM Fee 参数也可以是一种治理手段，该参数允许 PSM 对每笔交易收取少量费用，一方面可以更好的平衡市场，同时手续费也可帮助 PSM 实现更好的治理。

## 核心参数&#x20;

### Swap Limit (line)&#x20;

Swap Limit 是指 PSM 中可以兑换的最大 USDD 额度。

### Fee In (tin)&#x20;

将 USDT/USDC/TUSD/USDJ 兑换成 USDD 的费用。

### Fee Out (tout)&#x20;

将 USDD 兑换成 USDT/USDC/TUSD/USDJ 的费用。

## 交互&#x20;

用户可以从以下网站找到 PSM 入口：

* [usdd.io](https://usdd.io/#/)
* [tdr.org ](https://tdr.org/#/)
* [sun.io ](https://sun.io/?lang=en-US#/psm)

用户可以选择通过 PSM 入口完成 SWAP 功能， 也可以直接调用 PSM 合约完成兑换，对于 Defi 项目方来说，可轻松将 PSM 整合到 DEX 聚合器中完成交易。

## 注意事项&#x20;

PSM 能够提供的交易数量受到 Swap Limit 和流动性池中可用稳定币数量的限制。如果 PSM 已经达到兑换限额，它就不能提供 USDD 的兑换交易。同样，如果 PSM 内没有足够的 USDT/USDC/TUSD/USDJ，那么 PSM 也无法完成 USDD → USDT/USDC/TUSD/USDJ的兑换。
