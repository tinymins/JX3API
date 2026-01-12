English | [中文](./KAuctionClient.zh-CN.md)

# KAuctionClient

Auction house client object for auction operations.

Notes:

- Obtained via `GetAuctionClient()`

## Methods

[`Sell`](#KAuctionClient_Sell)
[`Bid`](#KAuctionClient_Bid)

---

* <h4 id="KAuctionClient_Sell">Sell</h4>

Lists an item for sale on the auction house.

 > (`void`) KAuctionClient:Sell(`number` nPackage, `number` nIndex, `number` nPrice, `number` nBuyoutPrice, `number` nDuration)

* <h4 id="KAuctionClient_Bid">Bid</h4>

Places a bid on an auction item.

 > (`void`) KAuctionClient:Bid(`number` dwAuctionID, `number` nPrice)
