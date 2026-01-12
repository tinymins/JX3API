# GoldTeam (金团)

Functions for managing gold team (金团) bidding system.

---

## GoldTeamBase_GetAllBiddingInfos {#GoldTeamBase_GetAllBiddingInfos}

Get all bidding information for the current gold team.

### Syntax

```lua
local tBiddingInfos = GoldTeamBase_GetAllBiddingInfos()
```

### Returns

| Type | Description |
|------|-------------|
| `table` | Array of bidding information tables |

### Bidding Info Structure

| Field | Type | Description |
|-------|------|-------------|
| `dwItemID` | `number` | Item ID being bid on |
| `dwItemIndex` | `number` | Item index |
| `nCurrentPrice` | `number` | Current highest bid |
| `szCurrentBidder` | `string` | Current highest bidder name |
| `dwCurrentBidderID` | `number` | Current bidder's player ID |
| `nStartPrice` | `number` | Starting price |
| `nMinIncrement` | `number` | Minimum bid increment |
| `nTimeRemaining` | `number` | Remaining time in seconds |
| `bEnded` | `boolean` | Whether bidding has ended |

### Example

```lua
local tInfos = GoldTeamBase_GetAllBiddingInfos()
if tInfos then
    for _, info in ipairs(tInfos) do
        Output(string.format(
            "Item %d: Current bid %d gold by %s",
            info.dwItemID,
            info.nCurrentPrice,
            info.szCurrentBidder or "None"
        ))
    end
end
```

---

## OpenGoldTeam {#OpenGoldTeam}

Open the gold team interface panel.

### Syntax

```lua
OpenGoldTeam()
```

### Example

```lua
-- Open gold team panel
OpenGoldTeam()
```

---

## Gold Team System Overview

The gold team (金团) system allows raid leaders to run loot auctions where players bid gold for dropped items.

### Typical Workflow

1. Leader sets up gold team settings
2. Raid clears boss and loot drops
3. Leader starts bidding for each item
4. Players bid using the gold team interface
5. Highest bidder wins the item
6. Gold is collected and distributed

### Example: Display Current Auctions

```lua
local function ShowCurrentAuctions()
    local tInfos = GoldTeamBase_GetAllBiddingInfos()
    if not tInfos or #tInfos == 0 then
        Output("No active auctions")
        return
    end

    Output("=== Current Auctions ===")
    for i, info in ipairs(tInfos) do
        local szStatus = info.bEnded and "[ENDED]" or
            string.format("[%ds left]", info.nTimeRemaining)

        Output(string.format(
            "%d. Item %d - %d gold %s",
            i,
            info.dwItemID,
            info.nCurrentPrice,
            szStatus
        ))

        if info.szCurrentBidder then
            Output(string.format(
                "   Highest bidder: %s",
                info.szCurrentBidder
            ))
        end
    end
end

-- Call to display
ShowCurrentAuctions()
```

---

## See Also

- [Raid Functions](./Raid.md) - Raid management functions
- [Team Functions](./Team.md) - Team/Party functions
