[English](./KAuctionClient.md) | 中文

# KAuctionClient（拍卖行客户端）

拍卖行客户端对象，用于拍卖操作。

说明：

- 通过 `GetAuctionClient()` 获取

## 方法

[`Sell`](#KAuctionClient_Sell)
[`Bid`](#KAuctionClient_Bid)

---

* <h4 id="KAuctionClient_Sell">Sell</h4>

在拍卖行上架物品出售。

 > (`void`) KAuctionClient:Sell(`number` nPackage, `number` nIndex, `number` nPrice, `number` nBuyoutPrice, `number` nDuration)

* <h4 id="KAuctionClient_Bid">Bid</h4>

对拍卖物品出价。

 > (`void`) KAuctionClient:Bid(`number` dwAuctionID, `number` nPrice)
