
[欢迎来到BitShares文档](https://docs.bitshares.org/)

欢迎访问BitShares Blockchain的文档门户。 此页面上的内容由BitShares社区管理，并不断在完善。

本网站的目的是提供有关BitShares区块链的深入文档，使用户和开发人员可以更轻松地利用BitShares区块链的全部功能。

* [白皮书](https://github.com/bitshares-foundation/bitshares.foundation/blob/master/download/articles/BitSharesBlockchain.pdf)
* [基金会公告](http://www.bitshares.foundation/)


# 技术




# BTS 持有者

## 1. Things you should know  

## 2. 资产token  

### 2.1 用户可以发行的资产(UIAs)

### 2.2 市场挂钩资产(MPAs)

### 2.3 Exchange Backed Assets(EBA)

### 2.4 Privatized BitAssets

### 2.5 Fee Backed Asset

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