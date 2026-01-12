# Constants Part 5 - Auction, Mail and Shop

Game constants for auction, mail, shop, and economy systems.

---

## AUCTION_RESPOND_CODE {#AUCTION_RESPOND_CODE}

Auction respond codes.

| Constant | Description |
|----------|-------------|
| `AUCTION_RESPOND_CODE.INVALID` | Invalid |
| `AUCTION_RESPOND_CODE.SUCCESS` | Success |
| `AUCTION_RESPOND_CODE.FAILED` | Failed |
| `AUCTION_RESPOND_CODE.ITEM_NOT_EXIST` | Item not exist |
| `AUCTION_RESPOND_CODE.NOT_ENOUGH_MONEY` | Not enough money |
| `AUCTION_RESPOND_CODE.PRICE_TOO_LOW` | Price too low |
| `AUCTION_RESPOND_CODE.PRICE_TOO_HIGH` | Price too high |
| `AUCTION_RESPOND_CODE.SELL_LIST_FULL` | Sell list full |
| `AUCTION_RESPOND_CODE.BID_LIST_FULL` | Bid list full |
| `AUCTION_RESPOND_CODE.ITEM_NOT_BIND` | Item not bind |
| `AUCTION_RESPOND_CODE.ITEM_NOT_SELL` | Item not sell |
| `AUCTION_RESPOND_CODE.NOT_ENOUGH_SPACE` | Not enough space |
| `AUCTION_RESPOND_CODE.AUCTION_OVER` | Auction over |
| `AUCTION_RESPOND_CODE.CANNOT_BID_SELF` | Cannot bid self |
| `AUCTION_RESPOND_CODE.ALREADY_HIGHEST` | Already highest |
| `AUCTION_RESPOND_CODE.TOO_FAR` | Too far |
| `AUCTION_RESPOND_CODE.ITEM_CD` | Item cooldown |
| `AUCTION_RESPOND_CODE.NOT_SAME_CAMP` | Not same camp |
| `AUCTION_RESPOND_CODE.CANNOT_CANCEL` | Cannot cancel |
| `AUCTION_RESPOND_CODE.GUILD_AUCTION` | Guild auction |
| `AUCTION_RESPOND_CODE.NOT_IN_GUILD` | Not in guild |
| `AUCTION_RESPOND_CODE.NO_PERMISSION` | No permission |
| `AUCTION_RESPOND_CODE.CANNOT_BUY_UNPROCESSED_ITEM` | Cannot buy unprocessed item |
| `AUCTION_RESPOND_CODE.NOT_SAME_SERVER` | Not same server |
| `AUCTION_RESPOND_CODE.SAFE_LOCK_LIMIT` | Safe lock limit |

---

## MAIL_RESPOND_CODE {#MAIL_RESPOND_CODE}

Mail respond codes.

| Constant | Description |
|----------|-------------|
| `MAIL_RESPOND_CODE.INVALID` | Invalid |
| `MAIL_RESPOND_CODE.SUCCESS` | Success |
| `MAIL_RESPOND_CODE.SEND_MAIL_SUCCESS` | Send mail success |
| `MAIL_RESPOND_CODE.FAILED` | Failed |
| `MAIL_RESPOND_CODE.RECEIVER_NOT_EXIST` | Receiver not exist |
| `MAIL_RESPOND_CODE.NOT_ENOUGH_MONEY` | Not enough money |
| `MAIL_RESPOND_CODE.MAIL_LIST_FULL` | Mail list full |
| `MAIL_RESPOND_CODE.MAIL_NOT_EXIST` | Mail not exist |
| `MAIL_RESPOND_CODE.ITEM_NOT_EXIST` | Item not exist |
| `MAIL_RESPOND_CODE.BAG_FULL` | Bag full |
| `MAIL_RESPOND_CODE.CANNOT_SEND_TO_SELF` | Cannot send to self |
| `MAIL_RESPOND_CODE.CANNOT_SEND_MONEY` | Cannot send money |
| `MAIL_RESPOND_CODE.NOT_SAME_CAMP` | Not same camp |
| `MAIL_RESPOND_CODE.TOO_MANY_ITEMS` | Too many items |
| `MAIL_RESPOND_CODE.ITEM_BINDED` | Item binded |
| `MAIL_RESPOND_CODE.IN_BLACKLIST` | In blacklist |
| `MAIL_RESPOND_CODE.REFUSE_MAIL` | Refuse mail |
| `MAIL_RESPOND_CODE.LEVEL_NOT_ENOUGH` | Level not enough |
| `MAIL_RESPOND_CODE.EMPTY_TITLE` | Empty title |
| `MAIL_RESPOND_CODE.EMPTY_CONTENT` | Empty content |
| `MAIL_RESPOND_CODE.ITEM_OVER_LIMIT` | Item over limit |
| `MAIL_RESPOND_CODE.NOT_PLAYER_MAIL` | Not player mail |
| `MAIL_RESPOND_CODE.HAS_ITEM_OR_MONEY` | Has item or money |
| `MAIL_RESPOND_CODE.RECEIVER_BAG_FULL` | Receiver bag full |
| `MAIL_RESPOND_CODE.TRANSFER_LIMIT` | Transfer limit |
| `MAIL_RESPOND_CODE.SAFE_LOCK_LIMIT` | Safe lock limit |
| `MAIL_RESPOND_CODE.NOT_SAME_SERVER` | Not same server |

---

## MAIL_TYPE {#MAIL_TYPE}

Mail type constants.

| Constant | Description |
|----------|-------------|
| `MAIL_TYPE.INVALID` | Invalid |
| `MAIL_TYPE.PLAYER` | Player |
| `MAIL_TYPE.SYSTEM` | System |
| `MAIL_TYPE.NPC` | NPC |
| `MAIL_TYPE.AUCTION` | Auction |
| `MAIL_TYPE.TONG` | Tong/Guild |
| `MAIL_TYPE.FEEDBACK` | Feedback |
| `MAIL_TYPE.TRANSFER` | Transfer |

---

## COIN_SHOP_PAY_TYPE {#COIN_SHOP_PAY_TYPE}

Coin shop pay type constants.

| Constant | Description |
|----------|-------------|
| `COIN_SHOP_PAY_TYPE.INVALID` | Invalid |
| `COIN_SHOP_PAY_TYPE.COIN` | Coin |
| `COIN_SHOP_PAY_TYPE.COIN_VALUE` | Coin value |
| `COIN_SHOP_PAY_TYPE.COIN_OR_VALUE` | Coin or value |
| `COIN_SHOP_PAY_TYPE.ONLY_COIN` | Only coin |
| `COIN_SHOP_PAY_TYPE.ONLY_VALUE` | Only value |

---

## COIN_SHOP_TIME_LIMIT_TYPE {#COIN_SHOP_TIME_LIMIT_TYPE}

Coin shop time limit type constants.

| Constant | Description |
|----------|-------------|
| `COIN_SHOP_TIME_LIMIT_TYPE.NO_LIMIT` | No limit |
| `COIN_SHOP_TIME_LIMIT_TYPE.DAY` | Day |
| `COIN_SHOP_TIME_LIMIT_TYPE.WEEK` | Week |
| `COIN_SHOP_TIME_LIMIT_TYPE.MONTH` | Month |
| `COIN_SHOP_TIME_LIMIT_TYPE.ALWAYS` | Always |

---

## COIN_SHOP_GOODS_TYPE {#COIN_SHOP_GOODS_TYPE}

Coin shop goods type constants.

| Constant | Description |
|----------|-------------|
| `COIN_SHOP_GOODS_TYPE.INVALID` | Invalid |
| `COIN_SHOP_GOODS_TYPE.ITEM` | Item |
| `COIN_SHOP_GOODS_TYPE.ITEM_PACKAGE` | Item package |
| `COIN_SHOP_GOODS_TYPE.FREE_GIFT` | Free gift |
| `COIN_SHOP_GOODS_TYPE.ITEM_BOX` | Item box |
| `COIN_SHOP_GOODS_TYPE.RANDOM_ITEM` | Random item |

---

## COIN_SHOP_OWN_TYPE {#COIN_SHOP_OWN_TYPE}

Coin shop own type constants.

| Constant | Description |
|----------|-------------|
| `COIN_SHOP_OWN_TYPE.INVALID` | Invalid |
| `COIN_SHOP_OWN_TYPE.ACCOUNT` | Account |
| `COIN_SHOP_OWN_TYPE.ROLE` | Role |

---

## COIN_SHOP_DISCOUNT_TYPE {#COIN_SHOP_DISCOUNT_TYPE}

Coin shop discount type constants.

| Constant | Description |
|----------|-------------|
| `COIN_SHOP_DISCOUNT_TYPE.NONE` | None |
| `COIN_SHOP_DISCOUNT_TYPE.TIME_LIMIT` | Time limit |
| `COIN_SHOP_DISCOUNT_TYPE.PRIVILEGE` | Privilege |
| `COIN_SHOP_DISCOUNT_TYPE.VIP` | VIP |

---

## COIN_SHOP_ERROR_CODE {#COIN_SHOP_ERROR_CODE}

Coin shop error codes.

| Constant | Description |
|----------|-------------|
| `COIN_SHOP_ERROR_CODE.SUCCESS` | Success |
| `COIN_SHOP_ERROR_CODE.FAILED` | Failed |
| `COIN_SHOP_ERROR_CODE.NOT_ENOUGH_COIN` | Not enough coin |
| `COIN_SHOP_ERROR_CODE.NOT_ENOUGH_VALUE` | Not enough value |
| `COIN_SHOP_ERROR_CODE.BAG_FULL` | Bag full |
| `COIN_SHOP_ERROR_CODE.ITEM_NOT_EXIST` | Item not exist |
| `COIN_SHOP_ERROR_CODE.BUY_LIMIT` | Buy limit |
| `COIN_SHOP_ERROR_CODE.NOT_START` | Not start |
| `COIN_SHOP_ERROR_CODE.ALREADY_END` | Already end |
| `COIN_SHOP_ERROR_CODE.SOLD_OUT` | Sold out |
| `COIN_SHOP_ERROR_CODE.NOT_VIP` | Not VIP |
| `COIN_SHOP_ERROR_CODE.LEVEL_NOT_ENOUGH` | Level not enough |
| `COIN_SHOP_ERROR_CODE.SAFE_LOCK_LIMIT` | Safe lock limit |
| `COIN_SHOP_ERROR_CODE.ACCOUNT_LIMIT` | Account limit |
| `COIN_SHOP_ERROR_CODE.ROLE_LIMIT` | Role limit |
| `COIN_SHOP_ERROR_CODE.GIFT_AMOUNT_ERROR` | Gift amount error |
| `COIN_SHOP_ERROR_CODE.GIFT_TARGET_ERROR` | Gift target error |

---

## PEER_PAY_OPERATE_TYPE {#PEER_PAY_OPERATE_TYPE}

Peer pay operate type constants.

| Constant | Description |
|----------|-------------|
| `PEER_PAY_OPERATE_TYPE.INVALID` | Invalid |
| `PEER_PAY_OPERATE_TYPE.CREATE` | Create |
| `PEER_PAY_OPERATE_TYPE.PAY` | Pay |
| `PEER_PAY_OPERATE_TYPE.CANCEL` | Cancel |
| `PEER_PAY_OPERATE_TYPE.RECEIVE` | Receive |

---

## PEER_PAY_RESULT_CODE {#PEER_PAY_RESULT_CODE}

Peer pay result codes.

| Constant | Description |
|----------|-------------|
| `PEER_PAY_RESULT_CODE.SUCCESS` | Success |
| `PEER_PAY_RESULT_CODE.FAILED` | Failed |
| `PEER_PAY_RESULT_CODE.NOT_ENOUGH_MONEY` | Not enough money |
| `PEER_PAY_RESULT_CODE.ORDER_NOT_EXIST` | Order not exist |
| `PEER_PAY_RESULT_CODE.ORDER_EXPIRED` | Order expired |
| `PEER_PAY_RESULT_CODE.ORDER_COMPLETED` | Order completed |
| `PEER_PAY_RESULT_CODE.ORDER_CANCELED` | Order canceled |
| `PEER_PAY_RESULT_CODE.NOT_SAME_SERVER` | Not same server |
| `PEER_PAY_RESULT_CODE.SAFE_LOCK_LIMIT` | Safe lock limit |

---

## COIN_BUY_RESPOND_CODE {#COIN_BUY_RESPOND_CODE}

Coin buy respond codes.

| Constant | Description |
|----------|-------------|
| `COIN_BUY_RESPOND_CODE.INVALID` | Invalid |
| `COIN_BUY_RESPOND_CODE.SUCCESS` | Success |
| `COIN_BUY_RESPOND_CODE.FAILED` | Failed |
| `COIN_BUY_RESPOND_CODE.NOT_ENOUGH_COIN` | Not enough coin |
| `COIN_BUY_RESPOND_CODE.REPEAT_REQUEST` | Repeat request |
| `COIN_BUY_RESPOND_CODE.ALREADY_MAXLEVEL` | Already max level |
| `COIN_BUY_RESPOND_CODE.EXPIRED` | Expired |
| `COIN_BUY_RESPOND_CODE.LOCKED` | Locked |
| `COIN_BUY_RESPOND_CODE.NOT_VIP` | Not VIP |
| `COIN_BUY_RESPOND_CODE.BAG_NOT_ENOUGH` | Bag not enough |
| `COIN_BUY_RESPOND_CODE.FAIL_LIMIT_COUNT` | Fail limit count |

---

## GAME_CARD_RESPOND_CODE {#GAME_CARD_RESPOND_CODE}

Game card respond codes.

| Constant | Description |
|----------|-------------|
| `GAME_CARD_RESPOND_CODE.INVALID` | Invalid |
| `GAME_CARD_RESPOND_CODE.SUCCESS` | Success |
| `GAME_CARD_RESPOND_CODE.FAILED` | Failed |
| `GAME_CARD_RESPOND_CODE.CARD_EXPIRED` | Card expired |
| `GAME_CARD_RESPOND_CODE.CARD_USED` | Card used |
| `GAME_CARD_RESPOND_CODE.CARD_NOT_EXIST` | Card not exist |
| `GAME_CARD_RESPOND_CODE.CARD_INVALID` | Card invalid |
| `GAME_CARD_RESPOND_CODE.BAG_FULL` | Bag full |
| `GAME_CARD_RESPOND_CODE.LEVEL_NOT_ENOUGH` | Level not enough |
| `GAME_CARD_RESPOND_CODE.USE_LIMIT` | Use limit |
| `GAME_CARD_RESPOND_CODE.NOT_IN_TIME` | Not in time |

---

## REWARDS_SHOP_RESPOND_CODE {#REWARDS_SHOP_RESPOND_CODE}

Rewards shop respond codes.

| Constant | Description |
|----------|-------------|
| `REWARDS_SHOP_RESPOND_CODE.SUCCESS` | Success |
| `REWARDS_SHOP_RESPOND_CODE.FAILED` | Failed |
| `REWARDS_SHOP_RESPOND_CODE.NOT_ENOUGH_SCORE` | Not enough score |
| `REWARDS_SHOP_RESPOND_CODE.BAG_FULL` | Bag full |
| `REWARDS_SHOP_RESPOND_CODE.ITEM_NOT_EXIST` | Item not exist |
| `REWARDS_SHOP_RESPOND_CODE.BUY_LIMIT` | Buy limit |

---

## BUY_ITEM_ORDER_RESULT_CODE {#BUY_ITEM_ORDER_RESULT_CODE}

Buy item order result codes.

| Constant | Description |
|----------|-------------|
| `BUY_ITEM_ORDER_RESULT_CODE.SUCCESS` | Success |
| `BUY_ITEM_ORDER_RESULT_CODE.FAILED` | Failed |
| `BUY_ITEM_ORDER_RESULT_CODE.ORDER_NOT_EXIST` | Order not exist |
| `BUY_ITEM_ORDER_RESULT_CODE.NOT_ENOUGH_MONEY` | Not enough money |
| `BUY_ITEM_ORDER_RESULT_CODE.BAG_FULL` | Bag full |
| `BUY_ITEM_ORDER_RESULT_CODE.ORDER_COMPLETED` | Order completed |
| `BUY_ITEM_ORDER_RESULT_CODE.ORDER_CANCELED` | Order canceled |
| `BUY_ITEM_ORDER_RESULT_CODE.SAFE_LOCK_LIMIT` | Safe lock limit |

---

## VIP_TYPE {#VIP_TYPE}

VIP type constants.

| Constant | Description |
|----------|-------------|
| `VIP_TYPE.INVALID` | Invalid |
| `VIP_TYPE.NORMAL` | Normal |
| `VIP_TYPE.VIP` | VIP |
| `VIP_TYPE.SUPER_VIP` | Super VIP |

---

## CHARGE_LIMIT_CODE {#CHARGE_LIMIT_CODE}

Charge limit codes.

| Constant | Description |
|----------|-------------|
| `CHARGE_LIMIT_CODE.SUCCESS` | Success |
| `CHARGE_LIMIT_CODE.FAILED` | Failed |
| `CHARGE_LIMIT_CODE.LIMIT_EXCEED` | Limit exceed |
| `CHARGE_LIMIT_CODE.AGE_NOT_VERIFIED` | Age not verified |

---

## SAFE_LOCK_EFFECT_TYPE {#SAFE_LOCK_EFFECT_TYPE}

Safe lock effect type constants.

| Constant | Description |
|----------|-------------|
| `SAFE_LOCK_EFFECT_TYPE.INVALID` | Invalid |
| `SAFE_LOCK_EFFECT_TYPE.TRADE` | Trade |
| `SAFE_LOCK_EFFECT_TYPE.MAIL` | Mail |
| `SAFE_LOCK_EFFECT_TYPE.AUCTION` | Auction |
| `SAFE_LOCK_EFFECT_TYPE.DESTROY` | Destroy |
| `SAFE_LOCK_EFFECT_TYPE.SHOP` | Shop |
| `SAFE_LOCK_EFFECT_TYPE.COIN_SHOP` | Coin shop |

---

## See Also

- [Constants Part 4 - Guild](./Constants4.md)
- [Constants Part 6 - Battlefield](./Constants6.md)
