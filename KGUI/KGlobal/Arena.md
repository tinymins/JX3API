# Arena (Sword Competition)

Arena and Corps (team) related functions for the Sword Competition (名剑大会) system.

---

## GetArenaStatistics {#GetArenaStatistics}

Get arena battle statistics for the player.

### Syntax

```lua
local tStatistics = GetArenaStatistics(nArenaType)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `nArenaType` | `number` | Arena type, use `ARENA_TYPE` enum |

### ARENA_TYPE Enum

| Constant | Value | Description |
|----------|-------|-------------|
| `ARENA_TYPE.INVALID` | 0 | Invalid |
| `ARENA_TYPE.ARENA_2V2` | 1 | 2v2 Arena |
| `ARENA_TYPE.ARENA_3V3` | 2 | 3v3 Arena |
| `ARENA_TYPE.ARENA_5V5` | 3 | 5v5 Arena |

### Returns

| Type | Description |
|------|-------------|
| `table` | Statistics data table |

### Return Table Fields

| Field | Type | Description |
|-------|------|-------------|
| `nWinCount` | `number` | Total wins |
| `nLoseCount` | `number` | Total losses |
| `nTotalCount` | `number` | Total matches |
| `nScore` | `number` | Current score/rating |
| `nMaxScore` | `number` | Highest score achieved |
| `nRank` | `number` | Current rank |

### Example

```lua
local tStats = GetArenaStatistics(ARENA_TYPE.ARENA_3V3)
if tStats then
    Output("3v3 Record: " .. tStats.nWinCount .. " wins / " .. tStats.nLoseCount .. " losses")
    Output("Current Score: " .. tStats.nScore)
end
```

---

## GetCorpsInfo {#GetCorpsInfo}

Get Corps (Sword Competition team) information.

### Syntax

```lua
local tCorpsInfo = GetCorpsInfo(nArenaType)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `nArenaType` | `number` | Arena type (2v2/3v3/5v5), use `ARENA_TYPE` enum. Different team sizes have different teams. |

### Returns

| Type | Description |
|------|-------------|
| `table` | Corps information table |

### Return Table Fields

| Field | Type | Description |
|-------|------|-------------|
| `dwCorpsID` | `number` | Corps ID |
| `szName` | `string` | Corps name |
| `nMemberCount` | `number` | Member count |
| `dwLeaderID` | `number` | Leader player ID |
| `szLeaderName` | `string` | Leader name |
| `nScore` | `number` | Corps score/rating |
| `nRank` | `number` | Corps rank |

### Example

```lua
-- Get 3v3 team info
local tCorps = GetCorpsInfo(ARENA_TYPE.ARENA_3V3)
if tCorps then
    Output("Team: " .. tCorps.szName)
    Output("Score: " .. tCorps.nScore)
    Output("Members: " .. tCorps.nMemberCount)
end
```

---

## GetCorpsID {#GetCorpsID}

Get the Corps ID for current player.

### Syntax

```lua
local dwCorpsID = GetCorpsID(nArenaType)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `nArenaType` | `number` | Arena type, use `ARENA_TYPE` enum |

### Returns

| Type | Description |
|------|-------------|
| `number` | Corps ID, or 0 if not in a corps |

### Example

```lua
local dwCorpsID = GetCorpsID(ARENA_TYPE.ARENA_3V3)
if dwCorpsID > 0 then
    Output("In a 3v3 corps, ID: " .. dwCorpsID)
end
```

---

## GetCorpsRoleInfo {#GetCorpsRoleInfo}

Get role information within the corps.

### Syntax

```lua
local tRoleInfo = GetCorpsRoleInfo(nArenaType)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `nArenaType` | `number` | Arena type, use `ARENA_TYPE` enum |

### Returns

| Type | Description |
|------|-------------|
| `table` | Role information in the corps |

### Return Table Fields

| Field | Type | Description |
|-------|------|-------------|
| `bIsLeader` | `boolean` | Whether the player is corps leader |
| `nJoinTime` | `number` | Join timestamp |

---

## GetCorpsMemberInfo {#GetCorpsMemberInfo}

Get member information from the corps.

### Syntax

```lua
local tMemberList = GetCorpsMemberInfo(nArenaType)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `nArenaType` | `number` | Arena type, use `ARENA_TYPE` enum |

### Returns

| Type | Description |
|------|-------------|
| `table` | Array of member information |

### Member Table Fields

| Field | Type | Description |
|-------|------|-------------|
| `dwID` | `number` | Player ID |
| `szName` | `string` | Player name |
| `dwForceID` | `number` | Force/faction ID |
| `nLevel` | `number` | Player level |
| `bOnline` | `boolean` | Whether online |

### Example

```lua
local tMembers = GetCorpsMemberInfo(ARENA_TYPE.ARENA_3V3)
if tMembers then
    for i, member in ipairs(tMembers) do
        local status = member.bOnline and "Online" or "Offline"
        Output(member.szName .. " - " .. status)
    end
end
```

---

## SyncCorpsBaseData {#SyncCorpsBaseData}

Request to sync corps base data from server.

### Syntax

```lua
SyncCorpsBaseData(nArenaType)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `nArenaType` | `number` | Arena type, use `ARENA_TYPE` enum |

### Example

```lua
-- Request 3v3 corps data sync
SyncCorpsBaseData(ARENA_TYPE.ARENA_3V3)
```

---

## SyncCorpsMemberData {#SyncCorpsMemberData}

Request to sync corps member data from server.

### Syntax

```lua
SyncCorpsMemberData(nArenaType)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `nArenaType` | `number` | Arena type, use `ARENA_TYPE` enum |

---

## GetBattleFieldStatistics {#GetBattleFieldStatistics}

Get battlefield statistics for the player.

### Syntax

```lua
local tStats = GetBattleFieldStatistics()
```

### Returns

| Type | Description |
|------|-------------|
| `table` | Battlefield statistics |

### Return Table Fields

| Field | Type | Description |
|-------|------|-------------|
| `nWinCount` | `number` | Total wins |
| `nLoseCount` | `number` | Total losses |
| `nKillCount` | `number` | Total kills |
| `nDeathCount` | `number` | Total deaths |
| `nDamageTotal` | `number` | Total damage dealt |
| `nHealTotal` | `number` | Total healing done |

---

## BattleField_MatchPlayer {#BattleField_MatchPlayer}

Start matchmaking for battlefield.

### Syntax

```lua
BattleField_MatchPlayer(nBattleFieldID)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `nBattleFieldID` | `number` | Battlefield map ID |

---

## GetBattleFieldPQInfo {#GetBattleFieldPQInfo}

Get battlefield PQ (Public Quest) information.

### Syntax

```lua
local tPQInfo = GetBattleFieldPQInfo()
```

### Returns

| Type | Description |
|------|-------------|
| `table` | Battlefield PQ info |

---

## Arena_GetCompetitionIndex {#Arena_GetCompetitionIndex}

Get current competition index.

### Syntax

```lua
local nIndex = Arena_GetCompetitionIndex()
```

### Returns

| Type | Description |
|------|-------------|
| `number` | Competition index |

---

## OpenArenaCorpsPanel {#OpenArenaCorpsPanel}

Open the Arena Corps management panel.

### Syntax

```lua
OpenArenaCorpsPanel(nArenaType)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `nArenaType` | `number` | Arena type, use `ARENA_TYPE` enum |

### Example

```lua
-- Open 3v3 corps panel
OpenArenaCorpsPanel(ARENA_TYPE.ARENA_3V3)
```

---

## See Also

- [Constants-Battle](./Constants-Battle.md) - Battle related constants
- [KTeamClient](../../SO3World/KClient/KTeamClient.md) - Team client functions
