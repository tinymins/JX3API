# 金团

用于管理金团竞拍系统的函数。

---

## GoldTeamBase_GetAllBiddingInfos {#GoldTeamBase_GetAllBiddingInfos}

获取当前金团的所有竞拍信息。

### 语法

```lua
local tBiddingInfos = GoldTeamBase_GetAllBiddingInfos()
```

### 返回值

| 类型 | 说明 |
|------|------|
| `table` | 竞拍信息表的数组 |

### 竞拍信息结构

| 字段 | 类型 | 说明 |
|------|------|------|
| `dwItemID` | `number` | 正在竞拍的物品 ID |
| `dwItemIndex` | `number` | 物品索引 |
| `nCurrentPrice` | `number` | 当前最高出价 |
| `szCurrentBidder` | `string` | 当前最高出价者名称 |
| `dwCurrentBidderID` | `number` | 当前出价者的玩家 ID |
| `nStartPrice` | `number` | 起拍价 |
| `nMinIncrement` | `number` | 最小加价幅度 |
| `nTimeRemaining` | `number` | 剩余时间（秒） |
| `bEnded` | `boolean` | 竞拍是否已结束 |

### 示例

```lua
local tInfos = GoldTeamBase_GetAllBiddingInfos()
if tInfos then
    for _, info in ipairs(tInfos) do
        Output(string.format(
            "物品 %d：当前出价 %d 金，出价者：%s",
            info.dwItemID,
            info.nCurrentPrice,
            info.szCurrentBidder or "无"
        ))
    end
end
```

---

## OpenGoldTeam {#OpenGoldTeam}

打开金团界面面板。

### 语法

```lua
OpenGoldTeam()
```

### 示例

```lua
-- 打开金团面板
OpenGoldTeam()
```

---

## 金团系统概述

金团系统允许团长进行装备竞拍，玩家用金币竞拍掉落的物品。

### 典型流程

1. 团长设置金团规则
2. 团队击杀 Boss，装备掉落
3. 团长为每件物品开启竞拍
4. 玩家通过金团界面出价
5. 最高出价者获得物品
6. 金币被收集并分配

### 示例：显示当前竞拍

```lua
local function ShowCurrentAuctions()
    local tInfos = GoldTeamBase_GetAllBiddingInfos()
    if not tInfos or #tInfos == 0 then
        Output("没有正在进行的竞拍")
        return
    end

    Output("=== 当前竞拍 ===")
    for i, info in ipairs(tInfos) do
        local szStatus = info.bEnded and "[已结束]" or
            string.format("[剩余 %d 秒]", info.nTimeRemaining)

        Output(string.format(
            "%d. 物品 %d - %d 金 %s",
            i,
            info.dwItemID,
            info.nCurrentPrice,
            szStatus
        ))

        if info.szCurrentBidder then
            Output(string.format(
                "   最高出价者：%s",
                info.szCurrentBidder
            ))
        end
    end
end

-- 调用显示
ShowCurrentAuctions()
```

---

## 相关链接

- [团队函数](./Raid.zh-CN.md) - 团队管理函数
- [队伍函数](./Team.zh-CN.md) - 队伍/小队函数
