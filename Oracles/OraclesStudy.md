# **Oracle Server Study**

*lixiaoyu 2017.2.17 -*

## 学习路径
1. Vitalik Buterin, [SchellingCoin: A Minimal-Trust Universal Data Feed](https://blog.ethereum.org/2014/07/22/ethereum-and-oracles/), 2014
2. Vitalik Buterin, [Ethereum and Oracles](https://blog.ethereum.org/2014/07/22/ethereum-and-oracles/)，2014
3. 第三方服务网站[Oraclize.it](www.oraclize.it)

## Oracles定义

>`An oracle, in the blockchain sense, is a third party which is sending to your on-chain smart contract some data your smart contract code cannot fetch by itself.`

看上去等同于Data Feed。高大上的说法是:
A reliable bridge between Ethereum smart contracts and the Internet.([TLSNotary](https://tlsnotary.org/) proof Oraclize could.)


## SchellingCoin
SchellingCoin出现的背景是解决以太坊智能合约与金融衍生品的应用遇到的问题。“对冲”，一种金融衍生品，是外贸交易中常用的金融工具，可以有效地减少汇率波动引起的损失。虚拟货币的价格波动非常大，用户使用虚拟货币进行交易也会面临价格波动引起损失的风险。使用“对冲”合约可以避免这样的损失，但区块链完整节点本身并不能读取链下的“价格”（如：ETH/USD）。因此，提出各种方法来解决链下数据上链的方法，SchellingCoin就是其中的一种去中心化的方法。

### Scheling Point 谢林点
http://baike.baidu.com/link?url=iolZwFMTrsJF8WNyL9L9jPjmB5y2wmNvI1fmrk90xd3Y5B6Xd0RlwXFP59Hvn0tB3Mk43D7a6U9jm-rfCwZS20-561t27hX4XI0u3DCCcg2hiTcpn2ZiRwyXQabQHFBq

“人们在没有沟通的情况下的选择倾向，做出这一选择可能因为它看起来自然、特别、或者与选择者有关。”

举例：假设你和另一个囚犯被关在单独的房间里,和保安给你两个相同的纸和几个数字。如果你选择相同数字的,那么你们将被释放;否则,将在狱中度过余生。这些数字是：

14237 59049 76241 81259 90215 100000 132156 157604

由于数字“100000”在几个数字中最特殊，绝大多数人都会选择它。根据人类的这一趋利避害的天性设计了SchellingCoin大致原理如下：
1. 每偶数个区块，所有用户都能用各自的地址提交ETH/USD的价格的Hash值。
2. 在下一个区块，用户能提交上次提交的ETH/USD的价格的实际值。
3. 当实际值N+用户地址做hash，即H(N+ADDR)前后一致，且交易签名方是系统合法的，数字签名也正确时，我们就称之为“正确的提交值”。
4. 将正确的提交值进行排序。
5. 每个提交正确且提交值处于所有值25%~75%用户，将获得SchellingCoin奖励。
6. *假设使用PoW或PoS，可以避免女巫攻击。*

### 问题和限制
1. 共谋攻击，类似51%攻击。
2. micro-cheating，对问题的理解有歧义或不够具体。解决方法：一、清晰定义问题。二、改善系统，减少出错几率。

### 总结：
Vitalik提出了POC设计，将SchellingCoin作为激励，让更多用户透过智能合约参与投票，选取符合中间值（25%~75%）的参与者进行奖励。除了引入汇率，SchellingCoin还可以被用来作为分布式的AWS。

### 思考：
**Vitalik在[SchellingCoin](https://blog.ethereum.org/2014/07/22/ethereum-and-oracles/)一文中指出：**
>`In fact Bitcoin’s mining algorithm basically is a SchellingCoin on the order of transactions.`

意味着比特币挖矿算法（记录账本的规则，并非共识演算法）就是一种交易排序的SchellingCoin。进一步思考，把挖矿算法换成EVM就是以太坊，把挖矿算法换成Oracles就是更有意思的组合。
