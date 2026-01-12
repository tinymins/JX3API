# Buff Management

Buff monitoring and management functions for addon development.

---

## BuffMgr {#BuffMgr}

Global Buff Manager object for buff-related operations.

### Properties

| Property | Type | Description |
|----------|------|-------------|
| `BuffMgr.tBuffList` | `table` | Cached buff list |

### Methods

See individual function documentation below.

---

## GetBuffInfo {#GetBuffInfo}

Get detailed buff information by buff ID.

### Syntax

```lua
local tBuffInfo = GetBuffInfo(dwBuffID, nLevel)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `dwBuffID` | `number` | Buff ID |
| `nLevel` | `number` | Buff level |

### Returns

| Type | Description |
|------|-------------|
| `table` | Buff information table |

### Return Table Fields

| Field | Type | Description |
|-------|------|-------------|
| `dwID` | `number` | Buff ID |
| `szName` | `string` | Buff name |
| `nLevel` | `number` | Buff level |
| `nIconID` | `number` | Icon ID |
| `szDesc` | `string` | Description |
| `bCanCancel` | `boolean` | Whether can be manually cancelled |
| `bIsDebuff` | `boolean` | Whether is a debuff |

### Example

```lua
local tBuff = GetBuffInfo(123, 1)
if tBuff then
    Output("Buff: " .. tBuff.szName)
end
```

---

## GetBuffTime {#GetBuffTime}

Get remaining time for a buff on a target.

### Syntax

```lua
local nTime = GetBuffTime(dwCharacterID, dwBuffID, nLevel)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `dwCharacterID` | `number` | Character ID (player or NPC) |
| `dwBuffID` | `number` | Buff ID |
| `nLevel` | `number` | Buff level |

### Returns

| Type | Description |
|------|-------------|
| `number` | Remaining time in frames, or 0 if buff not found |

### Example

```lua
local player = GetClientPlayer()
local nTime = GetBuffTime(player.dwID, 123, 1)
if nTime > 0 then
    Output("Buff remaining: " .. (nTime / 16) .. " seconds")
end
```

---

## Buff_AddonSetFilter {#Buff_AddonSetFilter}

Set buff filter for addon buff monitoring.

### Syntax

```lua
Buff_AddonSetFilter(szFilterID, tFilter)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `szFilterID` | `string` | Unique filter identifier |
| `tFilter` | `table` | Filter configuration table |

### Filter Table Fields

| Field | Type | Description |
|-------|------|-------------|
| `bOnlyMine` | `boolean` | Only show buffs cast by self |
| `bShowDebuff` | `boolean` | Show debuffs |
| `bShowBuff` | `boolean` | Show buffs |
| `tBuffList` | `table` | Array of buff IDs to track |

### Example

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

Update addon buff display.

### Syntax

```lua
Buff_AddonUpdate(szFilterID, dwTargetID)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `szFilterID` | `string` | Filter identifier set by `Buff_AddonSetFilter` |
| `dwTargetID` | `number` | Target character ID |

---

## Buffer_IsDispel {#Buffer_IsDispel}

Check if a buff can be dispelled.

### Syntax

```lua
local bCanDispel = Buffer_IsDispel(dwBuffID, nLevel)
-- or
local bCanDispel = IsBuffDispel(dwBuffID, nLevel)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `dwBuffID` | `number` | Buff ID |
| `nLevel` | `number` | Buff level |

### Returns

| Type | Description |
|------|-------------|
| `boolean` | `true` if buff can be dispelled |

### Example

```lua
if Buffer_IsDispel(123, 1) then
    Output("This buff can be dispelled")
end
```

---

## OutputBuffTip {#OutputBuffTip}

Display buff tooltip at cursor position.

### Syntax

```lua
OutputBuffTip(dwCharacterID, nIndex, tParams)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `dwCharacterID` | `number` | Character ID |
| `nIndex` | `number` | Buff index in buff list |
| `tParams` | `table` | (Optional) Additional parameters |

---

## GetBuffDesc {#GetBuffDesc}

Get buff description text.

### Syntax

```lua
local szDesc = GetBuffDesc(dwBuffID, nLevel, tParams)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `dwBuffID` | `number` | Buff ID |
| `nLevel` | `number` | Buff level |
| `tParams` | `table` | (Optional) Format parameters |

### Returns

| Type | Description |
|------|-------------|
| `string` | Buff description |

---

## GetBindBuffDesc {#GetBindBuffDesc}

Get bind buff description (buffs that are linked).

### Syntax

```lua
local szDesc = GetBindBuffDesc(dwBuffID, nLevel)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `dwBuffID` | `number` | Buff ID |
| `nLevel` | `number` | Buff level |

### Returns

| Type | Description |
|------|-------------|
| `string` | Bind buff description |

---

## See Also

- [KPlayer](../../SO3World/KGameObject/KPlayer.md) - Player buff methods (`GetBuff`, `GetBuffCount`, `CancelBuff`)
- [Table](./Table.md) - `Table_GetBuff*` functions
