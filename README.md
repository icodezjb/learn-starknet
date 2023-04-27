# learn-starknet

StarkWare
StarkNet 的母公司 StarkWare 成立于 2018 年,
总部位于以色列，两个主要产品为基于以太坊主网构建的扩容引擎 StarkEx 和 通用型 ZK-Rollup StarkNet。

Cario 是StarkNet上的智能合约开发语言。
StarkNet本身不支持EVM。
虽然 Cairo 是 Starknet 合约的母语，它完全优化了 Starknet 的扩展潜力，
但团队正在开发从 Solidity 和其他编程语言到 Cairo 的转译器。
这些转译器将允许在 Starknet 上快速部署。(Nethermind 的 Warp 团队正在开发一个 Solidity 到 Cairo 的转译器：Warp)

#### 1.《崛起社区：一文全解StarkNet 技术原理及生态现状》
https://baijiahao.baidu.com/s?id=1761583400626614572&wfr=spider&for=pc

#### 2. starkware 官网
https://starkware.co/

#### 3. starknet api
https://github.com/starkware-libs/starknet-specs/blob/master/starknet_vs_ethereum_node_apis.md

#### 4. starknet 官网
https://www.starknet.io/en

#### 5. startnet 浏览器
- https://voyager.online/
- https://starkscan.co/
- https://v2.viewblock.io/starknet

#### 6. starknet 文档
https://docs.starknet.io/documentation

#### 7. starkgate
- https://github.com/starknet-io/starkgate-contracts

- https://github.com/starknet-io/starkgate-contracts/blob/main/src/starkware/starknet/apps/starkgate/cairo/token_bridge.cairo#L122

initiate_withdraw
- https://goerli.voyager.online/contract/0x073314940630fd6dcda0d772d4c972c4e0a9946bef9dabf4ef84eda8ef542b82#writeContract


#### 8. cairo-lang
https://www.cairo-lang.org/

#### 9. Cairo Book (released 2023-04-13)
https://cairo-book.github.io/title-page.html

#### 10. Awesome StarkNet 中文
https://github.com/StarkNet-ZH/Awesome-StarkNet-Chinese

#### 11. cario 1.0 31字节短数组类型
https://medium.com/@0xasten/exploring-cairo-1-0-indexer-b9eb5ff93531

#### 12. Cairo 之旅 III：通过 Starkling 学习 Felt 和 String
https://mirror.xyz/starknet-zh.eth/zSGxb7N4D6a1qW6S3q7JrRSaYYIOG9KasKNIVDHOlzg

#### 13. cario没有字符串
- https://cairo-utils-web.vercel.app/
- https://github.com/starkware-libs/cairo/blob/main/examples/fib_array.cairo

#### 14. OpenZeppelin cairo
https://github.com/OpenZeppelin/cairo-contracts/pull/584/files

#### 15. Cairo开发流程示例
https://trapdoor-tech.github.io/zkstark-book/Cairo_example/frame.html

#### 16. Starknet 2023年目标和路线图
https://m.marsbit.co/newsdetail/20230426093410733453.html

#### 17. Starkware技术架构与生态应用梳理
https://m.odaily.news/post/5185240

#### 18. StarkNet messaging bridge
https://github.com/starknet-edu/starknet-messaging-bridge

#### 19. Starknet debugging
https://github.com/starknet-edu/starknet-debug

#### 20. Cairo/Starknet bytecode analyzer, disassembler and decompiler
https://github.com/FuzzingLabs/thoth

#### 21. Basic Sample Hardhat Project - with Starknet Plugin
https://github.com/0xSpaceShard/starknet-hardhat-example/tree/master/scripts

#### 22. 可视化组装cairo erc20合约
https://wizard.openzeppelin.com/cairo#erc20

#### 23. cairo序列化
https://starknetpy.readthedocs.io/en/latest/guide/serialization.html


```txt
从StarkNet 版本 0.10.1开始，在 StarkNet 上部署账户的历史方法，deploy交易，已经被删除。
它现在已被允许您部署帐户并从预注资地址支付费用的交易所取代deploy_account
（从而解决了如何在尚未部署帐户的情况下支付费用的问题）。

1. account
   为了在 StarkNet 上部署新帐户，您需要完成以下步骤：
   (1) 确定要部署的账户合约
   (2) 在链下计算你的潜在账户地址
   (3) 将资金发送到这个地址
   一旦地址有足够的资金来支付部署费用，您就可以发送deploy_account交易了。

new_account (链下生成,链下充值)
deploy_account(链上部署)

2. contract
   在 Starknet 上，部署合约分为两步：
   (1) 声明您的合约类别，或将您的合约代码发送到网络
   (2) 部署合约，或创建您之前声明的代码的实例

starknet-compile(链下编译)
declare(链上声明, Class声明)
deploy(链上部署, Contract实例化)
invoke(链下write链上)
call(链下read链上)
```




