# Raid

Raid party management and configuration functions.

---

## Raid_SetConfig {#Raid_SetConfig}

Set raid UI configuration options.

### Syntax

```lua
Raid_SetConfig(szKey, value)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `szKey` | `string` | Configuration key |
| `value` | `any` | Configuration value |

### Configuration Keys

| Key | Type | Description |
|-----|------|-------------|
| `"ShowBuffTime"` | `boolean` | Show buff remaining time |
| `"ShowDebuff"` | `boolean` | Show debuffs |
| `"ShowDistance"` | `boolean` | Show distance to members |
| `"ShowTargetOfTarget"` | `boolean` | Show target of target |
| `"LifePercentage"` | `boolean` | Show life as percentage |
| `"ManaPercentage"` | `boolean` | Show mana as percentage |

### Example

```lua
Raid_SetConfig("ShowBuffTime", true)
Raid_SetConfig("ShowDebuff", true)
```

---

## Raid_GetConfig {#Raid_GetConfig}

Get raid UI configuration value.

### Syntax

```lua
local value = Raid_GetConfig(szKey)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `szKey` | `string` | Configuration key |

### Returns

| Type | Description |
|------|-------------|
| `any` | Configuration value |

### Example

```lua
local bShowDebuff = Raid_GetConfig("ShowDebuff")
```

---

## Raid_SetBufftimeParam {#Raid_SetBufftimeParam}

Set buff time display parameters for raid frames.

### Syntax

```lua
Raid_SetBufftimeParam(tParam)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `tParam` | `table` | Buff time display parameters |

### Parameter Table Fields

| Field | Type | Description |
|-------|------|-------------|
| `nFontSize` | `number` | Font size for time display |
| `nOffsetX` | `number` | X offset |
| `nOffsetY` | `number` | Y offset |
| `bShowSeconds` | `boolean` | Show seconds |

---

## Raid_MonitorBuffs {#Raid_MonitorBuffs}

Set buffs to monitor in raid frames.

### Syntax

```lua
Raid_MonitorBuffs(tBuffList)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `tBuffList` | `table` | Array of buff IDs to monitor |

### Example

```lua
-- Monitor specific debuffs
Raid_MonitorBuffs({
    12345, -- Boss debuff 1
    12346, -- Boss debuff 2
})
```

---

## Raid_GetMemberHandle {#Raid_GetMemberHandle}

Get UI handle for a raid member.

### Syntax

```lua
local hMember = Raid_GetMemberHandle(dwPlayerID)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `dwPlayerID` | `number` | Player ID |

### Returns

| Type | Description |
|------|-------------|
| `userdata` | UI handle for the member frame |

### Example

```lua
local hMember = Raid_GetMemberHandle(dwTargetID)
if hMember then
    -- Manipulate the member frame
end
```

---

## OpenRaidPanel {#OpenRaidPanel}

Open the raid management panel.

### Syntax

```lua
OpenRaidPanel()
```

### Example

```lua
OpenRaidPanel()
```

---

## CloseRaidPanel {#CloseRaidPanel}

Close the raid management panel.

### Syntax

```lua
CloseRaidPanel()
```

---

## Send_RaidReadyConfirm {#Send_RaidReadyConfirm}

Send ready check to all raid members (leader only).

### Syntax

```lua
Send_RaidReadyConfirm()
```

### Note

This function can only be called by the raid leader.

### Example

```lua
local player = GetClientPlayer()
if player.IsInRaid() then
    local hTeam = GetClientTeam()
    local dwLeaderID = hTeam.GetAuthorityInfo(TEAM_AUTHORITY_TYPE.LEADER)
    if dwLeaderID == player.dwID then
        Send_RaidReadyConfirm()
    end
end
```

---

## ApplyMapEnterInfo {#ApplyMapEnterInfo}

Request map enter information (dungeon availability).

### Syntax

```lua
ApplyMapEnterInfo()
```

### Note

This function has a 500ms cooldown to prevent spam.

---

## ApplyMapSaveCopy {#ApplyMapSaveCopy}

Request to save dungeon copy progress.

### Syntax

```lua
ApplyMapSaveCopy()
```

---

## ApplyDungeonRoleProgress {#ApplyDungeonRoleProgress}

Request dungeon role progress data.

### Syntax

```lua
ApplyDungeonRoleProgress(dwMapID)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `dwMapID` | `number` | Dungeon map ID |

---

## GetDungeonRoleProgress {#GetDungeonRoleProgress}

Get dungeon role progress data.

### Syntax

```lua
local tProgress = GetDungeonRoleProgress(dwMapID)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `dwMapID` | `number` | Dungeon map ID |

### Returns

| Type | Description |
|------|-------------|
| `table` | Dungeon progress data |

### Return Table Fields

| Field | Type | Description |
|-------|------|-------------|
| `nBossKilled` | `number` | Number of bosses killed |
| `nTotalBoss` | `number` | Total number of bosses |
| `tBossState` | `table` | Array of boss states |

---

## See Also

- [KTeamClient](../../SO3World/KClient/KTeamClient.md) - Team/Party client functions
- [Event](./Event.md) - Event registration
