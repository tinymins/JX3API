[English](./Trade.md) | 中文

# 交易函数

交易操作相关函数。

## 函数

[`GetMailClient`](#GetMailClient)
[`GetAuctionClient`](#GetAuctionClient)
[`OpenBank`](#OpenBank)
[`CloseBank`](#CloseBank)
[`IsBankOpen`](#IsBankOpen)
[`GetExchangeShopNpcID`](#GetExchangeShopNpcID)
[`OpenShop`](#OpenShop)
[`CloseShop`](#CloseShop)
[`BuyItem`](#BuyItem)
[`SellItem`](#SellItem)
[`RepairItem`](#RepairItem)
[`RepairAllItem`](#RepairAllItem)

---

* <h4 id="GetMailClient">GetMailClient</h4>

获取邮件客户端对象。

 > ([`KMailClient`](./KClient/KMailClient.zh-CN.md) mailClient) GetMailClient()

* <h4 id="GetAuctionClient">GetAuctionClient</h4>

获取拍卖行客户端对象。

 > ([`KAuctionClient`](./KClient/KAuctionClient.zh-CN.md) auctionClient) GetAuctionClient()

* <h4 id="OpenBank">OpenBank</h4>

打开银行界面。

 > (`void`) OpenBank()

* <h4 id="CloseBank">CloseBank</h4>

关闭银行界面。

 > (`void`) CloseBank()

* <h4 id="IsBankOpen">IsBankOpen</h4>

检查银行界面是否打开。

 > (`boolean` bOpen) IsBankOpen()

* <h4 id="GetExchangeShopNpcID">GetExchangeShopNpcID</h4>

获取当前兑换商店的 NPC ID。

 > (`number` dwNpcID) GetExchangeShopNpcID()

* <h4 id="OpenShop">OpenShop</h4>

打开商店界面。

 > (`void`) OpenShop(`number` dwNpcID)

* <h4 id="CloseShop">CloseShop</h4>

关闭商店界面。

 > (`void`) CloseShop()

* <h4 id="BuyItem">BuyItem</h4>

从商店购买物品。

 > (`void`) BuyItem(`number` nIndex, `number` nCount)

* <h4 id="SellItem">SellItem</h4>

向商店出售物品。

 > (`void`) SellItem(`number` nPackage, `number` nIndex, `number` nCount)

* <h4 id="RepairItem">RepairItem</h4>

修理单个物品。

 > (`void`) RepairItem(`number` nPackage, `number` nIndex)

* <h4 id="RepairAllItem">RepairAllItem</h4>

修理所有物品。

 > (`void`) RepairAllItem()

---

## 已禁用的函数

以下函数在源码中存在但已被注释，无法使用：

* <h4 id="TradingConfirm">~~TradingConfirm~~</h4>

⚠️ **已禁用** - 此函数已被注释。

```lua
-- 已注释
-- TradingConfirm()
```
