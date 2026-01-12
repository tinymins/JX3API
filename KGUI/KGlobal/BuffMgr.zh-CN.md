# Buff 管理

用于插件开发的 Buff 监控和管理函数。

---

## BuffMgr {#BuffMgr}

全局 Buff 管理器对象，用于 Buff 相关操作。

### 属性

| 属性 | 类型 | 说明 |
|------|------|------|
| `BuffMgr.tBuffList` | `table` | 缓存的 Buff 列表 |

### 方法

请参阅下方的各个函数文档。

---

## GetBuffInfo {#GetBuffInfo}

根据 Buff ID 获取详细的 Buff 信息。

### 语法

```lua
local tBuffInfo = GetBuffInfo(dwBuffID, nLevel)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `dwBuffID` | `number` | Buff ID |
| `nLevel` | `number` | Buff 等级 |

### 返回值

| 类型 | 说明 |
|------|------|
| `table` | Buff 信息表 |

### 返回表字段

| 字段 | 类型 | 说明 |
|------|------|------|
| `dwID` | `number` | Buff ID |
| `szName` | `string` | Buff 名称 |
| `nLevel` | `number` | Buff 等级 |
| `nIconID` | `number` | 图标 ID |
| `szDesc` | `string` | 描述 |
| `bCanCancel` | `boolean` | 是否可手动取消 |
| `bIsDebuff` | `boolean` | 是否为减益效果 |

### 示例

```lua
local tBuff = GetBuffInfo(123, 1)
if tBuff then
    Output("Buff: " .. tBuff.szName)
end
```

---

## GetBuffTime {#GetBuffTime}

获取目标身上某个 Buff 的剩余时间。

### 语法

```lua
local nTime = GetBuffTime(dwCharacterID, dwBuffID, nLevel)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `dwCharacterID` | `number` | 角色 ID（玩家或 NPC） |
| `dwBuffID` | `number` | Buff ID |
| `nLevel` | `number` | Buff 等级 |

### 返回值

| 类型 | 说明 |
|------|------|
| `number` | 剩余时间（帧数），如果 Buff 不存在则返回 0 |

### 示例

```lua
local player = GetClientPlayer()
local nTime = GetBuffTime(player.dwID, 123, 1)
if nTime > 0 then
    Output("Buff 剩余: " .. (nTime / 16) .. " 秒")
end
```

---

## Buff_AddonSetFilter {#Buff_AddonSetFilter}

设置插件 Buff 监控的过滤器。

### 语法

```lua
Buff_AddonSetFilter(szFilterID, tFilter)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `szFilterID` | `string` | 唯一的过滤器标识符 |
| `tFilter` | `table` | 过滤器配置表 |

### 过滤器表字段

| 字段 | 类型 | 说明 |
|------|------|------|
| `bOnlyMine` | `boolean` | 仅显示自己施放的 Buff |
| `bShowDebuff` | `boolean` | 显示减益效果 |
| `bShowBuff` | `boolean` | 显示增益效果 |
| `tBuffList` | `table` | 要追踪的 Buff ID 数组 |

### 示例

```lua
Buff_AddonSetFilter("MyAddon_Filter", {
    bOnlyMine = true,
    bShowDebuff = true,
    bShowBuff = true,
    tBuffList = {123, 456, 789}
})
```

---

## Buff_AddonUpdate {#Buff_AddonUpdate}

更新插件 Buff 显示。

### 语法

```lua
Buff_AddonUpdate(szFilterID, dwTargetID)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `szFilterID` | `string` | 由 `Buff_AddonSetFilter` 设置的过滤器标识符 |
| `dwTargetID` | `number` | 目标角色 ID |

---

## Buffer_IsDispel {#Buffer_IsDispel}

检查 Buff 是否可被驱散。

### 语法

```lua
local bCanDispel = Buffer_IsDispel(dwBuffID, nLevel)
-- 或
local bCanDispel = IsBuffDispel(dwBuffID, nLevel)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `dwBuffID` | `number` | Buff ID |
| `nLevel` | `number` | Buff 等级 |

### 返回值

| 类型 | 说明 |
|------|------|
| `boolean` | 如果 Buff 可被驱散则返回 `true` |

### 示例

```lua
if Buffer_IsDispel(123, 1) then
    Output("此 Buff 可被驱散")
end
```

---

## OutputBuffTip {#OutputBuffTip}

在鼠标位置显示 Buff 提示信息。

### 语法

```lua
OutputBuffTip(dwCharacterID, nIndex, tParams)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `dwCharacterID` | `number` | 角色 ID |
| `nIndex` | `number` | Buff 在列表中的索引 |
| `tParams` | `table` | （可选）附加参数 |

---

## GetBuffDesc {#GetBuffDesc}

获取 Buff 描述文本。

### 语法

```lua
local szDesc = GetBuffDesc(dwBuffID, nLevel, tParams)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `dwBuffID` | `number` | Buff ID |
| `nLevel` | `number` | Buff 等级 |
| `tParams` | `table` | （可选）格式化参数 |

### 返回值

| 类型 | 说明 |
|------|------|
| `string` | Buff 描述 |

---

## GetBindBuffDesc {#GetBindBuffDesc}

获取绑定 Buff 的描述（关联的 Buff）。

### 语法

```lua
local szDesc = GetBindBuffDesc(dwBuffID, nLevel)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `dwBuffID` | `number` | Buff ID |
| `nLevel` | `number` | Buff 等级 |

### 返回值

| 类型 | 说明 |
|------|------|
| `string` | 绑定 Buff 描述 |

---

## 另见

- [KPlayer](../../SO3World/KGameObject/KPlayer.zh-CN.md) - 玩家 Buff 方法（`GetBuff`、`GetBuffCount`、`CancelBuff`）
- [Table](./Table.zh-CN.md) - `Table_GetBuff*` 函数
