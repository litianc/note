# Bootstrapping a Decentralized Autonomous Corporation, Part 3: Identity Corp

原文链接：https://bitcoinmagazine.com/articles/bootstrapping-a-decentralized-autonomous-corporation-part-3-identity-corp-1380073003/

## 1 探讨：DAC 的应用及其对社会的真实价值

1. 打破垄断：
    - 价格垄断：A decentralized corporation can theoretically be designed so that no one involved in the price-setting mechanism has any such incentive.
    - 企业腐化：Bitcoin itself is a perfect example of this.
2. 防止违法违规：
    - 去中心化网络的版权
    - 减少“丝绸之路”的使用
    - 去中心化网络能比中心化方式更高效地运行

## 2 打开加密货币、去中心化应用的大门

1. 加密货币的理想——Dapp
    - 与加密货币理想一致的设计，但远远不同于今天的加密货币。（这一设计现在被称为：Dapp）
2. Identity Corp
    - 定义
        > 中文：一个以创建密码学安全的给个人创建身份档案为唯一目的的公司，个人通过数字签名表达身份，并与物理身份相关联。
        >
        > 原文：a corporation whose sole purpose is to create cryptographically secure identity documents for individuals that they could sign messages with, and are linked to individuals’ physical identities.

    - 进入半匿名的比特币世界是为了逃避法币的枷锁和反洗钱的繁重的身份验证需求。
    - Identity Corp是要将身份验证带回到桌面上吗？
3. 身份的含义
    - 为什么Silk Road founder - Roberts 仍在维持自己的身份？答案很简单，他在经营数百万美元的生意，他需要告诉用户他们值得信赖。
    - 为了向世界展示,他们现在有一个额外的动力,诚实守信。有的生意人会故意让政府和不满的客户能轻易攻击他们。
    - 与Roberts公开的“身份”不同，这里谈的“身份”是指标准的密钥加密身份：提供两条消息是由同一实体创建/签名出来的。
4. 真名与假名
    - 现实世界，“Vitalik Buterin” 与 “djargon135″ （笔名）都是代表一个人
    - 在这里的“身份”框架内，每个实体只能有一个真实名字：“Vitalik Buterin” 与 “djargon135″ 代表的是两个人。
    - 小结：“假名”被用来证实两个消息是由同一实体创建 / 签名，“真名”被用来证明两个消息是由两个不同实体创建的。
    - 为什么要用真名？
        - 真名的应用都被简化为一个概念：免费样品——每人只有一份
        - 一个早先被用作“真名”的案例：公司拥有人需要公开他的详细信息，来消除他可能会被起诉的担心。类比免费样品，公司拥有者获得了一份社会的样品：声誉。
        - 在公钥的场景中，身份可以零成本创建，每个人的初始声誉为零，生意起步就很难。
        - 真名系统中，每个人的初始身份是被创建的，无法获得多个。也因此就有一个免费的初始声誉。

## 3 如何实现？

1.  完全通过互联网机制很难实现
2.  线下机制
    - 如生物识别（DNA 指纹 面部等）。
    - 实际政府并没有用到太多这些信息，而是用血缘关系：父子模型，基于出生证明和面部识别。
3.  去中心化系统可以使用上面两种机制。
4.  去中心化的做法：答案是自然垄断的论点适用。即使系统可能有多个身份提供者,他们彼此都需要反复核对信息,以防止多个用户,以及由此产生的系统一定是唯一的。
5.  谁来运营 DAC ？
    - 如果企业运行这套系统，且被广泛接受，就可以收取一定费用。
    - 如果政府运行这套系统，可以绑定到已有的“真名”系统，并删除隐私信息。政府还可以撤销身份作为惩罚，如果大部分的互联网(社会)开始依赖这些机制将成为逃犯或持不同政见者更难生存。
    - 哪种政府会执行这样的系统？全球机构如联合国不是普遍信任,往往正是因为他们是如此完美的目标,任何试图获得任何形式的腐败现象在世界范围内控制。
    - 为了避免公司颠覆系统利润和政府颠覆系统为了自己的政治目的,将权力的一个分散的网络,如果可能的话,可以说是最好的选择。
    - 结论：要避免公司和政府来运行这套系统，交由去中心化的网络来处理。
6. Identity Corp 绕过的问题：
    - 无止境地收录用户信息。
        - 由Human代理，组群代理来完成。
        - 但是，代理人可以为假的个体创建许多身份，来欺骗系统。
        - 解决ii的问题的唯一办法就是 去中心化和冗余性：
        > have many different agents collecting the same information, and require individuals looking to get an identity to confirm it with several different agents, ideally randomly (or otherwise) selected by the system itself.
        >
        > decentralized “court”

    - 这些代理都应该是谁？
        - 应该避免 [Sybil attacks](https://en.wikipedia.org/wiki/Sybil_attack)
        - 因为我们不希望一个人的生物信息被全世界51%以上的人都得到，所以POW/POS是不够的。BTW，大规模部署时，只需要 5%~10% 就能进行欺骗。
        - 一个纯粹去中心化的公司来实现这个任务是不可能的。
        - 我们希望的是一个混合的系统，通过大量的人力支持来促使系统与现实趋近一致。

## 4 SocialCoin and the One World “Government”
1. SocialCoin 给每个公民 1000币/月
2. Devcoin-like system 允许人们来投票钱将花在哪里
    - 建立必要的“world government" 通过铸币税来筹备基金。
    - 那税率如何计算？
        - 人口死亡永久带走的币 + 通货膨胀。
        - 结论是每年2%
3. Will it happen? Well, either wait and see to find out, or start implementing it yourself.
