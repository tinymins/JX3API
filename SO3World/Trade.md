English | [中文](./Trade.zh-CN.md)

# Trade Functions

Functions for trading operations.

## Functions

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

Gets the mail client object.

 > ([`KMailClient`](./KClient/KMailClient.md) mailClient) GetMailClient()

* <h4 id="GetAuctionClient">GetAuctionClient</h4>

Gets the auction client object.

 > ([`KAuctionClient`](./KClient/KAuctionClient.md) auctionClient) GetAuctionClient()

* <h4 id="OpenBank">OpenBank</h4>

Opens the bank interface.

 > (`void`) OpenBank()

* <h4 id="CloseBank">CloseBank</h4>

Closes the bank interface.

 > (`void`) CloseBank()

* <h4 id="IsBankOpen">IsBankOpen</h4>

Checks if the bank interface is open.

 > (`boolean` bOpen) IsBankOpen()

* <h4 id="GetExchangeShopNpcID">GetExchangeShopNpcID</h4>

Gets the NPC ID of the current exchange shop.

 > (`number` dwNpcID) GetExchangeShopNpcID()

* <h4 id="OpenShop">OpenShop</h4>

Opens a shop interface.

 > (`void`) OpenShop(`number` dwNpcID)

* <h4 id="CloseShop">CloseShop</h4>

Closes the shop interface.

 > (`void`) CloseShop()

* <h4 id="BuyItem">BuyItem</h4>

Buys an item from a shop.

 > (`void`) BuyItem(`number` nIndex, `number` nCount)

* <h4 id="SellItem">SellItem</h4>

Sells an item to a shop.

 > (`void`) SellItem(`number` nPackage, `number` nIndex, `number` nCount)

* <h4 id="RepairItem">RepairItem</h4>

Repairs a single item.

 > (`void`) RepairItem(`number` nPackage, `number` nIndex)

* <h4 id="RepairAllItem">RepairAllItem</h4>

Repairs all items.

 > (`void`) RepairAllItem()

---

## Disabled Functions

The following functions exist in source but are commented out and cannot be used:

* <h4 id="TradingConfirm">~~TradingConfirm~~</h4>

⚠️ **Disabled** - This function is commented out.

```lua
-- Commented out
-- TradingConfirm()
```
