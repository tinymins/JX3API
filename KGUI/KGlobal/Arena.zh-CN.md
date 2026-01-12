# 名剑大会（Arena）

名剑大会和名剑大会队伍（Corps）相关函数。

---

## GetArenaStatistics {#GetArenaStatistics}

获取名剑大会战斗统计数据。

### 语法

```lua
local tStatistics = GetArenaStatistics(nArenaType)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `nArenaType` | `number` | 竞技场类型，使用 `ARENA_TYPE` 枚举 |

### ARENA_TYPE 枚举

| 常量 | 值 | 说明 |
|------|-----|------|
| `ARENA_TYPE.INVALID` | 0 | 无效 |
| `ARENA_TYPE.ARENA_2V2` | 1 | 2对2 名剑大会 |
| `ARENA_TYPE.ARENA_3V3` | 2 | 3对3 名剑大会 |
| `ARENA_TYPE.ARENA_5V5` | 3 | 5对5 名剑大会 |

### 返回值

| 类型 | 说明 |
|------|------|
| `table` | 统计数据表 |

### 返回表字段

| 字段 | 类型 | 说明 |
|------|------|------|
| `nWinCount` | `number` | 胜利场次 |
| `nLoseCount` | `number` | 失败场次 |
| `nTotalCount` | `number` | 总场次 |
| `nScore` | `number` | 当前积分 |
| `nMaxScore` | `number` | 历史最高积分 |
| `nRank` | `number` | 当前排名 |

### 示例

```lua
local tStats = GetArenaStatistics(ARENA_TYPE.ARENA_3V3)
if tStats then
    Output("3对3 战绩: " .. tStats.nWinCount .. " 胜 / " .. tStats.nLoseCount .. " 负")
    Output("当前积分: " .. tStats.nScore)
end
```

---

## GetCorpsInfo {#GetCorpsInfo}

获取名剑大会队伍信息。

### 语法

```lua
local tCorpsInfo = GetCorpsInfo(nArenaType)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `nArenaType` | `number` | 竞技场类型（2对2/3对3/5对5），使用 `ARENA_TYPE` 枚举。不同人数的队伍是不一样的。 |

### 返回值

| 类型 | 说明 |
|------|------|
| `table` | 队伍信息表 |

### 返回表字段

| 字段 | 类型 | 说明 |
|------|------|------|
| `dwCorpsID` | `number` | 队伍 ID |
| `szName` | `string` | 队伍名称 |
| `nMemberCount` | `number` | 成员数量 |
| `dwLeaderID` | `number` | 队长玩家 ID |
| `szLeaderName` | `string` | 队长名称 |
| `nScore` | `number` | 队伍积分 |
| `nRank` | `number` | 队伍排名 |

### 示例

```lua
-- 获取 3对3 队伍信息
local tCorps = GetCorpsInfo(ARENA_TYPE.ARENA_3V3)
if tCorps then
    Output("队伍: " .. tCorps.szName)
    Output("积分: " .. tCorps.nScore)
    Output("成员数: " .. tCorps.nMemberCount)
end
```

---

## GetCorpsID {#GetCorpsID}

获取当前玩家的名剑大会队伍 ID。

### 语法

```lua
local dwCorpsID = GetCorpsID(nArenaType)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `nArenaType` | `number` | 竞技场类型，使用 `ARENA_TYPE` 枚举 |

### 返回值

| 类型 | 说明 |
|------|------|
| `number` | 队伍 ID，如果没有加入队伍则返回 0 |

### 示例

```lua
local dwCorpsID = GetCorpsID(ARENA_TYPE.ARENA_3V3)
if dwCorpsID > 0 then
    Output("已加入 3对3 队伍，ID: " .. dwCorpsID)
end
```

---

## GetCorpsRoleInfo {#GetCorpsRoleInfo}

获取玩家在队伍中的角色信息。

### 语法

```lua
local tRoleInfo = GetCorpsRoleInfo(nArenaType)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `nArenaType` | `number` | 竞技场类型，使用 `ARENA_TYPE` 枚举 |

### 返回值

| 类型 | 说明 |
|------|------|
| `table` | 角色信息表 |

### 返回表字段

| 字段 | 类型 | 说明 |
|------|------|------|
| `bIsLeader` | `boolean` | 是否为队长 |
| `nJoinTime` | `number` | 加入时间戳 |

---

## GetCorpsMemberInfo {#GetCorpsMemberInfo}

获取名剑大会队伍成员信息。

### 语法

```lua
local tMemberList = GetCorpsMemberInfo(nArenaType)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `nArenaType` | `number` | 竞技场类型，使用 `ARENA_TYPE` 枚举 |

### 返回值

| 类型 | 说明 |
|------|------|
| `table` | 成员信息数组 |

### 成员表字段

| 字段 | 类型 | 说明 |
|------|------|------|
| `dwID` | `number` | 玩家 ID |
| `szName` | `string` | 玩家名称 |
| `dwForceID` | `number` | 门派 ID |
| `nLevel` | `number` | 玩家等级 |
| `bOnline` | `boolean` | 是否在线 |

### 示例

```lua
local tMembers = GetCorpsMemberInfo(ARENA_TYPE.ARENA_3V3)
if tMembers then
    for i, member in ipairs(tMembers) do
        local status = member.bOnline and "在线" or "离线"
        Output(member.szName .. " - " .. status)
    end
end
```

---

## SyncCorpsBaseData {#SyncCorpsBaseData}

请求同步名剑大会队伍基础数据。

### 语法

```lua
SyncCorpsBaseData(nArenaType)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `nArenaType` | `number` | 竞技场类型，使用 `ARENA_TYPE` 枚举 |

### 示例

```lua
-- 请求同步 3对3 队伍数据
SyncCorpsBaseData(ARENA_TYPE.ARENA_3V3)
```

---

## SyncCorpsMemberData {#SyncCorpsMemberData}

请求同步名剑大会队伍成员数据。

### 语法

```lua
SyncCorpsMemberData(nArenaType)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `nArenaType` | `number` | 竞技场类型，使用 `ARENA_TYPE` 枚举 |

---

## GetBattleFieldStatistics {#GetBattleFieldStatistics}

获取战场统计数据。

### 语法

```lua
local tStats = GetBattleFieldStatistics()
```

### 返回值

| 类型 | 说明 |
|------|------|
| `table` | 战场统计数据 |

### 返回表字段

| 字段 | 类型 | 说明 |
|------|------|------|
| `nWinCount` | `number` | 胜利场次 |
| `nLoseCount` | `number` | 失败场次 |
| `nKillCount` | `number` | 击杀数 |
| `nDeathCount` | `number` | 死亡数 |
| `nDamageTotal` | `number` | 总伤害 |
| `nHealTotal` | `number` | 总治疗 |

---

## BattleField_MatchPlayer {#BattleField_MatchPlayer}

开始战场匹配。

### 语法

```lua
BattleField_MatchPlayer(nBattleFieldID)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `nBattleFieldID` | `number` | 战场地图 ID |

---

## GetBattleFieldPQInfo {#GetBattleFieldPQInfo}

获取战场公共任务（PQ）信息。

### 语法

```lua
local tPQInfo = GetBattleFieldPQInfo()
```

### 返回值

| 类型 | 说明 |
|------|------|
| `table` | 战场 PQ 信息 |

---

## Arena_GetCompetitionIndex {#Arena_GetCompetitionIndex}

获取当前比赛索引。

### 语法

```lua
local nIndex = Arena_GetCompetitionIndex()
```

### 返回值

| 类型 | 说明 |
|------|------|
| `number` | 比赛索引 |

---

## OpenArenaCorpsPanel {#OpenArenaCorpsPanel}

打开名剑大会队伍管理面板。

### 语法

```lua
OpenArenaCorpsPanel(nArenaType)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `nArenaType` | `number` | 竞技场类型，使用 `ARENA_TYPE` 枚举 |

### 示例

```lua
-- 打开 3对3 队伍面板
OpenArenaCorpsPanel(ARENA_TYPE.ARENA_3V3)
```

---

## 另见

- [Constants-Battle](./Constants-Battle.zh-CN.md) - 战斗相关常量
- [KTeamClient](../../SO3World/KClient/KTeamClient.zh-CN.md) - 队伍客户端函数
