
[欢迎来到BitShares文档](https://docs.bitshares.org/)

欢迎访问BitShares Blockchain的文档门户。 此页面上的内容由BitShares社区管理，并不断在完善。

本网站的目的是提供有关BitShares区块链的深入文档，使用户和开发人员可以更轻松地利用BitShares区块链的全部功能。

* [白皮书](https://github.com/bitshares-foundation/bitshares.foundation/blob/master/download/articles/BitSharesBlockchain.pdf)
* [基金会公告](http://www.bitshares.foundation/)


# 技术


# BTS 持有者

## 1. Things you should know  

### 1.1. For the Starter
* Security and Control over accounts and funds: No one can access your funds unless you let them, intentionally, or unintentionally. With the power to be independent from 3rd parties, comes the responsibility to protect what belongs to you.
* Can interact with people directly: With BitShares it becomes possible to interact with people directly without needing to go through a middleman. Hence, BitShares is a platform of free speech that implements a payment platform and exchange for digital goods.
* Fast: Transactions in BitShares are verified and irrevocable in only a few seconds time.
* Decentralized Committee: Decisions that can effect the BitShares ecosystem are made using a on-chain committee voted upon by shareholders. Hence, no single entity can change the deal retroactively.
* Flexible: Protocol upgrades (formerly known as hard forks) can be implemented and executed to improve the BitShares business over time and allow to react on.

### 1.2. For the Investor
* Become BTS Holder: If you buy BTS either from a partner exchange or from the DEX, you become a BTS Holder of the BitShares decentralized business and as such can take a cut of its profits and participate in votes for future directions.
* Expenses: Vote for expenses of the business and hire workers to do important tasks for BitShares.
* Leaders: Participate in political decisions by voting for committee members that represent your views!
* Protocol upgrades: Improve the technology, integrate new features and adept legal and regulative changes by voting for upgrades.
* Decision making for a profit: Take part in decision finding about fair pricing models for transaction fees to a) increase growth and b) make BitShares profitable for its shareholders

## 2. 代币资产(Assets Tokens)  

### 2.1 用户可以发行的资产(UIAs)
BitShares 允许个人或公司去创建和发行他们自己的tokens。这种用户发行的资产(UIA)的场景是数不尽的。一方面，UIA可用作存放在客户手机上的简单活动门票，以通过音乐会的入口。 另一方面，它们可用于人群募资，所有权跟踪甚至以股票形式出售公司股权。  

所有你需要做的只是点击几下鼠标去创建一种新的UIA，定义你的coin的主要参数，如supply，precision，symbol，description，在几秒钟后那你就能看到你的coin被创建出来。从现在开始，你可以发行你的coin给你想给的人，出售代币资产，以及和BitShares上已经存在的coin进行交易。  

除非你自己想要一些限制。作为发行人，你拥有对你的coin的某些特权，例如，你可以仅允许在某些市场对中进行交易，并通过使用白名单和黑名单来定义实际上允许谁持有你的coin。当然，发行人可以为了信任和声誉而无限期地选择退出他的特权。  

作为该coin的所有者，你无需关注区块链技术的所有技术细节，例如分布式共识算法，区块链开发或集成。 甚至不需要运行任何挖矿设备或服务器等等。  

那么，缺点是什么？  

在这种情况下存在缺点，即集中发行新token。在某种程度上，这可以通过分层多签名发行者账户来管理，该账户防止任何单个实体发行新token，而是要求任意一组人之间达成共识以同意对coin的任何改变。

显然，适用于每一种token的法规的范围太大，并且，在不同的司法管辖区法规也存在差别。因此，BitShares提供的工具允许发行人在发行资产时遵守所有适用法规，前提是监管机构允许此类资产。

### 2.1.1. Use Cases
* Reward Points
* Fan Credits
* Flight Miles
* Event Tickets
* Digital Property
* Crowd-Funding
* Company Shares
  
### 2.1.2. How to create a new UIA by using GUI
[How can I create a new UIA by using GUI?](https://docs.bitshares.org/en/master/bts_holders/tutorials/uia-create-gui.html#creating-new-uia-gui)


### 2.2 市场挂钩资产(MPAs)

具有比特币的特性和优点的加密货币能够与全球采用的货币（例如美元）保持价格稳定，具有方便和审查抵制商业的高效用。 这可以通过BitShares的市场挂钩资产（MPA）来实现，MPA是一种新型的自由交易数字资产，其价值旨在通过差价合约（CFD）跟踪传统标的资产的价值。  

我们还可以创建市场挂钩资产（MPA）并让市场处理需求和供应，而不是建立一个完全控制供应的UIA。 我们所需要的只是一个公平的价格和另一种可以作为抵押品的资产。  

我们为什么需要抵押品？ 由于MPA的发行人无法控制供应，因此区块链协议涉及增加和减少供应。 为了让用户获得一些新的coins，他需要将抵押品放入智能合约中（从技术上讲，这份合约是差价合约）。  

> 一个简单的例子是由美元支持的MPA（BitShares中的稳定加密token），需要200％的附加比率。然后，为了获得新coins，我们可以通过支付200美元借入价值100美元的新coins。

这样，你的coins供应量就增加了100，但是怎么去减少呢？美元被锁定在智能合约中，只有在退还债务（此处为100个coins）时才能收回。退回它们将导致coins从供应中移除，因为它们不再受任何抵押品的支持。  

那么我们需要一个合理的价格呢？请记住，我们选择了200％的抵押比率？这个数字告诉我们你的coins在抵押品上的支撑程度。但是，如果你的coin价值落到月球上会发生什么？那么你的抵押比率将减少到150％。在一定比例下，区块链将自动触发所谓的追加保证金。  

> 1.Take your collateral (here, USD)  
> 2.Sell it in the market to buy back the coin you owe  
> 3.Close the contract  
> 4.Pay your the residual USD  

因此，公平的价格告诉市场你的coin的价值（例如，在外部交易所交易）并在必要时触发追加保证金。

但还有更多！在BitShares中持有您的（MPA）coin的每个人都可以以合理的价格将coin转换为支持资产。此程序称为“结算”，确保您的MPA始终至少价值合理。

在用户界面中，MPA很容易与资产浏览器中的UIA区分开来。

#### 2.2.1. SmartCoins
BitAssets可以由网络上的任何人创建和拥有。 但是，BitShares委员会拥有的那些被称为 SmartCoins。 其中包括：
* (Bit)USD
* (Bit)CNY
* (Bit)EUR
* (Bit)GOLD
* (Bit)Silver  

这些资产中的余额标有USD、CNY等的标签，因为它们与其底层具有相同的价值。

#### 2.2.2. Collateralized Tokens 抵押tokens

SmartCoin（MPA的同义词）是一种加密货币，其总价值的100％或更多由BitShares核心货币（BTS）支持，它们可以随时转换为CFD中的抵押品。  

MPA的独特之处在于它们没有交易对手风险，即使它们类似于抵押品支持的差价合约。 这可以通过让网络本身（作为软件协议实现）负责保护抵押品并执行结算来实现，这将在下面更详细地描述。  

#### 2.2.3. Market Mechanics 市场机制

每种BitAsset会有一个被witnesses提供的feed，表明该资产的公平价格。这种被叫做Settlement Price或Feed Price的，被用来保证借入BitAssets的看涨，不再维持最小抵押比率(维持抵押比率)。这些持仓的抵押会自动地去回购债务，也即头寸被强制平仓。根据这些规则，网络强制交易参与者始终保持高于最低要求的抵押品。目前，所需要的最低抵押比率为175%，可以通过见证人修改。

在交易前阅读更多关于保证金要求的机制。

### 2.3 Exchange Backed Assets(EBA)

交易所支持资产代表由集中实体（如交易所，银行或其他机构）发行的存款收据。 这些可以解释为我欠你（欠条）或在该机构存款的证书。

从区块链的角度来看，EBA相当于用户发行的资产（UIA），只是创建和发行方变成了交易所，银行或金融机构。因此，他们有责任在存款上使用相应的区块链token（EBA）。  
> From the blockchain perspective, EBA are equivalent to a User Issued Assets (UIAs) that is created and issued by an exchange, bank or financial institute. Hence, it is their responsibility to credit you with the corresponding blockchain token (the EBA) on deposits.

#### 2.3.1. Use Case

最常见的例子是中心化交易所，这些交易所支持用户通过钱包去充值加密货币。这些充值通常是存储在他们自己的数据库中，和用户的内部账户的资产相一致。这些数据库余额用作存款收据，但显然需要一些信任，即数据库可以抵御任何类型的攻击。

不是增加用户的内部账户余额，一种EBA的新的份额可以以充值的形式被发行给用户。由于EBA是区块链代币，因此它们可以在分散交易所交易，类似于任何其他交易所。

为了在他们的原生区块链中回收他的加密token，用户将EBA发回给institute，然后销毁EBA并将相应的资产转回其合法的所有者。

[由于EBA是作为UIA实现的，因此您可以在相应的页面上阅读有关底层技术的更多信息 -  UIA。](https://docs.bitshares.org/en/master/bts_holders/tokens/uia.html#uia)

### 2.4 Privatized BitAssets 私有化的

除了像bitUSD这样的常规MPA之外，BitShares还为 entrepreneurs 提供了一个机会，可以使用自定义参数和一组独特的价格Feed生成器创建自己的SmartCoins。  

私有化的SmartCoin经理可以尝试不同的参数，如抵押要求，价格反馈，强制结算延迟和强制结算费用。 他们还从已发行资产所涉及的交易中获得交易费用，因此具有在网络上营销和推广它的财务激励。 能够发现和推广最佳参数集的entrepreneurs可以获得巨大的利润。 entrepreneurs可以调整的参数集足够广泛，SmartCoins可用于实现功能完善的预测市场，并以合理的价格保证全球结算，并且在交割日期之前不会强制结算。

一些entrepreneurs 可能想要尝试SmartCoins，它总是以1.00美元的价格交易，而不是严格超过1.00美元。 他们可以通过持续操纵强制结算费来做到这一点，使平均交易价格保持在1.00美元左右。 默认情况下，BitShares更喜欢市场设定的费用，因此选择让价格浮动到1.00美元以上，而不是通过直接操纵强制结算费来固定价格。

### 2.5 Fee Backed Asset

BitShares协议的现有核心功能是市场挂钩资产（MPA）和发行方支持的用户已发布资产（UIA）。 在此提案中，我们引入了另一种资产：费用支持资产（FBA）。  

Feed backed assets allow to propose and fund market based innovation by sharing a cut of future profits generated by this particular innovation with the people that helped fund it. Think of it as a Kickstarter for features. Hence, if people can profit from successful features in the form of fees then it can help the BitShares ecosystem to become more adaptable over time as it promotes innovation and can pay for its development.  

如果你有任何需要在区块链上进行新类型交易的功能的想法，你可以编写该功能，FBA会提供资金支持。  

### 2.6 预测市场  
预测市场有一种专门的BitAsset，总负债和总抵押总是会达到一种相等的平衡(尽管他们的资产类型不同)。无保证金和强制结算是预测市场资产的特征。在预测事件完成后，预测市场资产被资产的发行者全局结算(global_settle_asset)。因此，预测市场资产必须总是要有glbal_settle的权限。一种预测市场资产的global结算或卖空行为的最大价格是1或-1(也即价格介于-1和1之间)。

----
**目录：**
* [创建](#2.6.1创建)
* [下注](#2.6.2下注)
  * [看涨](#2.6.2.1看涨)
  * [看跌](#2.6.2.2看跌)
* [表决](#2.6.3表决)

----

注意：  
    在下文中，预测市场看涨，resolve=true，喂价为1；看跌，resolve=false，喂价为0。  

If the bet resolves to true (i.e. a price feed of 1), then the PM-asset can be settled release the collateral to the holder of the asset.  

If, instead, the bet resolves to false (i.e. a price feed of 0), then those that sold the PM-asset on the market and went short, made a profit since it PM-asset became worthless.  


### 2.6.1创建  
预测市场的是能够自由交易的资产，可以与支持的资产(可能是任何其他资产，包括BTS，USD，GOLD)按照1:1的比率从市场借入。  

### 2.6.2下注  
用户可以自由地看涨或看跌。我们在这里会展示如何生效的。

#### 2.6.2.1看涨
如果你确信看涨将会发生，通过1:1的比例提供对应的抵押资产，你可以拥有特定的PM资产。  
为了拥有这些代币，你可以设置价格在0~1的买单，然后等待订单成交；或者市价下单。通过这种方式，用户可以预先设定要购买的份额。

For instance, if you think that the bet resolves positively at a probability of 80%, you can put your buy order at a price of 0.8. If the bet resolves positively (price feed of 1), then you can settle your shares at 1 and make a 20% profit.

If you can buy tokens at a price of 0.2 (i.e. market participants think it is unlikely to resolve positively), then you could make 80% profits at a risk of loosing with 80% probability.

在结束投注后，用户可以通过结算其借入头寸并取出抵押品来获得利润：

* Settlement in the CLI wallet:  
``` shell
    >>> settle_asset <account> <amount> <symbol> True  
```
* Borrowing in the GUI wallet:  
    A settlement button is available when hovering the asset in your account’s overview.


#### 2.6.2.2看跌
为了看涨(bet resolvers = false, feed price = 0)，你需要卖出tokens。为了得到这些代币，虽然你不能在市场上买入，但是可以通过支付1:1比例的抵押物去borrow这些tokens。

例如，在PM.PRESIDENT2016中，如果您想以100k BTS投注看跌，您可以通过向网络支付100k BTS来借入100k PM.PRESIDENT2016。

注意：  
    由于PM-Assets在技术上可以被任何其他资产挂钩，您可能需要支付USD（或其他任何东西）而不是BTS。

一旦你借入代币，你可以在0~1之间的任意价格卖出他们。如果你认为看跌的概率是0.2，你可以考虑以0.2的价格卖出。

如果你看跌(feed price = 0)，你的负债价值：debt = amount * price = 0 BTS。你可以以零成本收回抵押的资产，并以0.2的价格卖出，获得20%的收益。相反，如果看涨，并且卖出了所有的tokens，你不能平掉你的借入持仓去兑换回抵押的资产。但是，在市场上卖出tokens的行为会导致你的总损失减少了20%。

如果在投注结束时，您仍然有一些代币，您当然可以部分关闭您的借入头寸并赎回相应的抵押品百分比。

* Borrowing in the CLI wallet:  
``` shell
    >>> borrow_asset <account> <amount> <PMsymbol> <1:1-amount> true  
```
* Borrowing in the GUI wallet:  
  Of course, the asset can also be borrowed in the GUI/web wallet by using the Borrow x button in the market.


### 2.6.3表决
预测市场需要通过资产发行者或者feed producer发布一个喂价。它本质上是一个global settlement，它将设置资产的参数，比如能够设置投注结果(0或1)的资产的持有者。详细信息显示在指南pm-close-manual中（参考：dev.bitshares.works资料）


# 用户指南

## 1. BitShares账户

在BitShares中，您可以使用BitShares UI钱包很容易地创建帐户。 该帐户附带私钥/公钥。 你需要把这些信息存放到安全可靠的地方。 此外，BitShares帐户为您提供一些好处（即终身会员（LTM）和推荐计划）和重要角色（即投票）。 我们建议您阅读BitShares帐户信息以了解更多信息。

**Table of Contents**

* Account
    * BitShares UI Wallet
    * Identifier
    * Accounts and keys

----------------------

当您第一次连接到其中一个BitShares UI钱包时，您会看到Welcome to BitShares页面。默认情况下，您将创建云钱包。您可以将Cloud Wallet smiler想象成您的普通银行账户。您记住了自己的帐户名和密码，银行为您管理并节省了资金。

与云钱包相对的本地钱包是另一种类型的钱包。您可以创建帐户名和密码，还必须管理资金。这意味着您必须创建帐户备份文件并将其保存在安全的地方。本地钱包创建表单是高级表单。您可以在同一个“欢迎使用BitShares”页面上找到该链接。

重要的是要了解只有你知道你的密码，没有人可以恢复它。帐户信息使用帐户的私钥/公钥注册到区块链。只有帐户创建者知道密码并找出私钥。我们将在另一部分中研究三种类型的密钥（即active，owner和memo key）。


# 资源