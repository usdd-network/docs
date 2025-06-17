# 发行机制

## 背景

如白皮书介绍，USDD目前处于USDD 1.0阶段，在此阶段，TDR 在波场网络预发行9999亿TRC-10版本USDD，其中10亿转入授权合约，剩余9989亿转入发行合约。当授权合约储备不足时，TDR将以多重签名的方式从发行合约释放TRC-10 USDD 到授权合约 。USDD 发行过程就是将授权合约中的 TRC-10 版本的 USDD 转换成 TRC-20 的 USDD 版本并释放给用户的过程。&#x20;

在USDD 1.0初始阶段，TDR及机构成员可通过质押 TRX 铸造发行 USDD。随着 USDD 生态的蓬勃发展，TDR为 USDD 生态引入了一个全新的模块 PSM，让所有 USDD 用户都可以参与到 USDD 的发行中。 伴随着 PSM 的上线，USDD 的发行方式也扩展为两种：

1. TDR 及机构成员通过质押 TRX 铸造发行 USDD。
2. 通过 PSM 发行 USDD。

详细发行流程如下图所示，图上部分为通过TDR 及机构成员通过质押 TRX 铸造发行 USDD，图下部分为通过 PSM 发行 USDD，两种方式都必须通过授权合约释放 USDD。

<figure><img src="../.gitbook/assets/web - 中文.png" alt=""><figcaption></figcaption></figure>

## **发行流程**

### **TDR 及机构成员通过质押 TRX 铸造发行 USDD**

在引入 PSM 之前， TDR机构成员通过质押 TRX 来铸造发行 USDD。 截止2022年8月16日， TDR 及机构成员通过该机制共发行了约 725 Million 的USDD， 目前这些 USDD 已经在多条主流区块链和多个主流市场上流通，铸造发行的详细流程如下：

1. TDR及机构成员将 TRX 转入TRX 销毁合约 \*。
2. 根据当时汇率计算等值美元，以多重签名的方式从 授权合约 \* 转移等值 TRC-10 USDD 到流通账户。
3. 将流通账户中的 TRC-10 USDD 转换成 TRC-20 USDD 后，转账给机构成员完成 USDD 发&#x884C;**。**

#### 主要合约和 Token 信息

TRC-10 USDD  ID: 1004777&#x20;

TRC-20 USDD  TPYmHEhy5n8TCEfYGqW2rPxsghSfzghPDn&#x20;

TRX 销毁合约\*  TNMcQVGPzqH9ZfMCSY4PNrukevtDgp24dK&#x20;

发行合约 \*         TRFGnuUqED3NDpMYgqZY1X3gAeVHNw1SDq&#x20;

授权合约 \*         TTsASxQhMk4t3S5vZMVVJ7nR2GQjDXNRnq

&#x20;\* 授权合约和发行合约均是由 7 个不同的机构成员通过 5/7 多重签名控制。

### **通过 PSM 发行 USDD**

PSM 作为 USDD 固定汇率货币兑换模块，允许用户通过此功能以 1:1 固定汇率将指定稳定币（目前支持USDT/USDC/TUSD ） 兑换为 USDD，同理也允许用户以 1:1 固定汇率将 USDD 兑换为 USDT/USDC/TUSD  。

PSM 的实现机制完美的扩展和丰富了 USDD 的发行机制，为 USDD 引入了一种新的发行方式。用户通过 PSM 完成 USDT/USDC/TUSD  --> USDD 的兑换也就完成了 USDD 的发行。 详细如下：（更详细的发行流程介绍参看 PSM页 和 白皮书）

1. TDR 将授权合约中已授权未发行的 TRC-10 USDD 释放到 PSM 的 safeVault 合约。&#x20;
2. PSM 在执行 USDT/USDC /TUSD → USDD 的兑换时，会将 safeVault 中的 TRC-10 USDD 转为 TRC-20 USDD 并释放给用户。反向兑换时，会将TRC-20 USDD 转换为 TRC-10 USDD 并转至 safeVault 合约；&#x20;

注： safeVault 中的 TRC-10 USDD 并不会影响 USDD 的实际发行量，只有兑换完成的时候，发行量才会相应的变化。&#x20;

* 增加发行量：当用户成功将 USDT/USDC/TUSD 兑换成 USDD 的时候， USDD 的发行量会相应的增加。&#x20;
* 减少发行量：当用户成功将 USDD 兑换成 USDT/USDC/TUSD  的时候， USDD 的发行量会相应的减少。

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

TUSD Quota \*        [TSApGmpYaPqKrQahjzbs7yrMjobSfugpXT](https://tronscan.io/#/contract/TSApGmpYaPqKrQahjzbs7yrMjobSfugpXT)    &#x20;

USDJ GemJoin \*    [TKAovR61zwp1t9Rg1UE4UY5mXt7QTJdDXg](https://tronscan.io/#/contract/TKAovR61zwp1t9Rg1UE4UY5mXt7QTJdDXg)

USDJ PSM \*           [TVS3rVDUSd3ySeXV5moRH2J2t5B9reJfLR](https://tronscan.io/#/contract/TVS3rVDUSd3ySeXV5moRH2J2t5B9reJfLR)

USDJ Quota \*        [TMdUs66Y4GQjdsPLkDPu2bmDVze6ErZSFY ](https://tronscan.io/#/contract/TMdUs66Y4GQjdsPLkDPu2bmDVze6ErZSFY/code)

safeVault                [TMgSSHn8APyUVViqXxtveqFEB7mBBeGqNP](https://tronscan.org/#/contract/TMgSSHn8APyUVViqXxtveqFEB7mBBeGqNP)

&#x20;\*  此合约由多重签名控制，由 7 个不同机构成员共同管理，签名条件为 5/7。

## 增加授权合约的 USDD 储备

当授权合约储备的 USDD 不足 5 亿时，将自动 增加授权合约的 USDD 储备，该过程通过多重签名的方式从发行合约释放 TRC-10 USDD 到授权合约。 5/7 签名条件达到之后 ，USDD 将处于锁定状态且至少锁定 10 天。

截止2022年8月16日， 由发行合约解锁至授权合约的 USDD 总储备量是 20 亿， 已授权未发行的 USDD 数量为 1,274,667,957。



###
