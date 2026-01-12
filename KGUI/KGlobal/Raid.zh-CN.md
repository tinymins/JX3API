# 团队（Raid）

团队管理和配置函数。

---

## Raid_SetConfig {#Raid_SetConfig}

设置团队界面配置选项。

### 语法

```lua
Raid_SetConfig(szKey, value)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `szKey` | `string` | 配置键名 |
| `value` | `any` | 配置值 |

### 配置键

| 键名 | 类型 | 说明 |
|------|------|------|
| `"ShowBuffTime"` | `boolean` | 显示 Buff 剩余时间 |
| `"ShowDebuff"` | `boolean` | 显示减益效果 |
| `"ShowDistance"` | `boolean` | 显示与成员的距离 |
| `"ShowTargetOfTarget"` | `boolean` | 显示目标的目标 |
| `"LifePercentage"` | `boolean` | 以百分比显示生命值 |
| `"ManaPercentage"` | `boolean` | 以百分比显示内力值 |

### 示例

```lua
Raid_SetConfig("ShowBuffTime", true)
Raid_SetConfig("ShowDebuff", true)
```

---

## Raid_GetConfig {#Raid_GetConfig}

获取团队界面配置值。

### 语法

```lua
local value = Raid_GetConfig(szKey)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `szKey` | `string` | 配置键名 |

### 返回值

| 类型 | 说明 |
|------|------|
| `any` | 配置值 |

### 示例

```lua
local bShowDebuff = Raid_GetConfig("ShowDebuff")
```

---

## Raid_SetBufftimeParam {#Raid_SetBufftimeParam}

设置团队框架中 Buff 时间显示参数。

### 语法

```lua
Raid_SetBufftimeParam(tParam)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `tParam` | `table` | Buff 时间显示参数 |

### 参数表字段

| 字段 | 类型 | 说明 |
|------|------|------|
| `nFontSize` | `number` | 时间显示字体大小 |
| `nOffsetX` | `number` | X 偏移 |
| `nOffsetY` | `number` | Y 偏移 |
| `bShowSeconds` | `boolean` | 显示秒数 |

---

## Raid_MonitorBuffs {#Raid_MonitorBuffs}

设置在团队框架中监控的 Buff。

### 语法

```lua
Raid_MonitorBuffs(tBuffList)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `tBuffList` | `table` | 要监控的 Buff ID 数组 |

### 示例

```lua
-- 监控特定减益效果
Raid_MonitorBuffs({
    12345, -- Boss 减益 1
    12346, -- Boss 减益 2
})
```

---

## Raid_GetMemberHandle {#Raid_GetMemberHandle}

获取团队成员的 UI 句柄。

### 语法

```lua
local hMember = Raid_GetMemberHandle(dwPlayerID)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `dwPlayerID` | `number` | 玩家 ID |

### 返回值

| 类型 | 说明 |
|------|------|
| `userdata` | 成员框架的 UI 句柄 |

### 示例

```lua
local hMember = Raid_GetMemberHandle(dwTargetID)
if hMember then
    -- 操作成员框架
end
```

---

## OpenRaidPanel {#OpenRaidPanel}

打开团队管理面板。

### 语法

```lua
OpenRaidPanel()
```

### 示例

```lua
OpenRaidPanel()
```

---

## CloseRaidPanel {#CloseRaidPanel}

关闭团队管理面板。

### 语法

```lua
CloseRaidPanel()
```

---

## Send_RaidReadyConfirm {#Send_RaidReadyConfirm}

向所有团队成员发送就位确认（仅限团长）。

### 语法

```lua
Send_RaidReadyConfirm()
```

### 注意

此函数只能由团长调用。

### 示例

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

请求地图进入信息（副本可用性）。

### 语法

```lua
ApplyMapEnterInfo()
```

### 注意

此函数有 500 毫秒的冷却时间，以防止滥用。

---

## ApplyMapSaveCopy {#ApplyMapSaveCopy}

请求保存副本进度。

### 语法

```lua
ApplyMapSaveCopy()
```

---

## ApplyDungeonRoleProgress {#ApplyDungeonRoleProgress}

请求副本角色进度数据。

### 语法

```lua
ApplyDungeonRoleProgress(dwMapID)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `dwMapID` | `number` | 副本地图 ID |

---

## GetDungeonRoleProgress {#GetDungeonRoleProgress}

获取副本角色进度数据。

### 语法

```lua
local tProgress = GetDungeonRoleProgress(dwMapID)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `dwMapID` | `number` | 副本地图 ID |

### 返回值

| 类型 | 说明 |
|------|------|
| `table` | 副本进度数据 |

### 返回表字段

| 字段 | 类型 | 说明 |
|------|------|------|
| `nBossKilled` | `number` | 已击杀 Boss 数量 |
| `nTotalBoss` | `number` | Boss 总数 |
| `tBossState` | `table` | Boss 状态数组 |

---

## 另见

- [KTeamClient](../../SO3World/KClient/KTeamClient.zh-CN.md) - 队伍/小队客户端函数
- [Event](./Event.zh-CN.md) - 事件注册
