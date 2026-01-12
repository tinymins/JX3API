# Homeland Functions

Homeland (housing system) related functions.

---

## Relation Center

### GetRelationCenter {#GetRelationCenter}

```lua
tCenter = GetRelationCenter(nCenterID)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nCenterID | `number` | Relation center ID |

**Returns:** `table` - Relation center data

Get relation center information for homeland.

---

## Community

### DaTangJiaYuan_GoToCommunityIndex {#DaTangJiaYuan_GoToCommunityIndex}

```lua
DaTangJiaYuan_GoToCommunityIndex(nIndex)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nIndex | `number` | Community index |

**Returns:** `void`

Navigate to a community index in Da Tang Jia Yuan (homeland system).

---

## Furniture

### GetNearbyFurnitureInfoList {#GetNearbyFurnitureInfoList}

```lua
tList = GetNearbyFurnitureInfoList(nRange)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nRange | `number` | Search range |

**Returns:** `table` - List of nearby furniture info

Get a list of nearby furniture information.

---

### InteractFurniture {#InteractFurniture}

```lua
InteractFurniture(dwFurnitureID)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwFurnitureID | `number` | Furniture ID |

**Returns:** `void`

Interact with a furniture object.

---

### HomeLand_GetFurniture2GameID {#HomeLand_GetFurniture2GameID}

```lua
dwGameID = HomeLand_GetFurniture2GameID(dwFurnitureID)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwFurnitureID | `number` | Furniture ID |

**Returns:** `number` - Game object ID

Get the game object ID from a furniture ID.

---

### Homeland_GetFurnitureConfig {#Homeland_GetFurnitureConfig}

```lua
tConfig = Homeland_GetFurnitureConfig(dwFurnitureID)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwFurnitureID | `number` | Furniture ID |

**Returns:** `table` - Furniture configuration

Get the configuration for a furniture item.

---

## Mini Games

### HomeLand_GetMiniGameInfo {#HomeLand_GetMiniGameInfo}

```lua
tInfo = HomeLand_GetMiniGameInfo(dwFurnitureID)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwFurnitureID | `number` | Furniture ID |

**Returns:** `table` - Mini game information

Get mini game information for a furniture item.

---

### HomeLand_GetBoxTypeByItem {#HomeLand_GetBoxTypeByItem}

```lua
nType = HomeLand_GetBoxTypeByItem(dwItemID)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwItemID | `number` | Item ID |

**Returns:** `number` - Box type

Get the box type by item ID.

---

### HousePlayPanel_OnClickBtnSure {#HousePlayPanel_OnClickBtnSure}

```lua
HousePlayPanel_OnClickBtnSure()
```

**Returns:** `void`

Trigger the confirm button click in house play panel.

---

## Scripts

### HomeLand_GetDwordScript {#HomeLand_GetDwordScript}

```lua
tScript = HomeLand_GetDwordScript(nDataType, ...)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nDataType | `number` | Data type (LAND_OBJECT_TYPE constant) |
| ... | `any` | Additional parameters |

**Returns:** `table` - Script data

Get DWORD script data by type.

Data types:
- `LAND_OBJECT_TYPE.SD_EIGHT_DWORD_SCRIPT`
- `LAND_OBJECT_TYPE.SD_FOUR_DWORD_SCRIPT`
- `LAND_OBJECT_TYPE.FOUR_DWORD_SCRIPT`

---

### HomeLand_CallDwordScript {#HomeLand_CallDwordScript}

```lua
result = HomeLand_CallDwordScript(nDataType, ...)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nDataType | `number` | Data type (LAND_OBJECT_TYPE constant) |
| ... | `any` | Script parameters |

**Returns:** `any` - Script result

Call a DWORD script by type.

---

### HomeLand_GetDWORDValueByuint {#HomeLand_GetDWORDValueByuint}

```lua
nValue = HomeLand_GetDWORDValueByuint(nData, nStart, nBitLength)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nData | `number` | Source data |
| nStart | `number` | Start position |
| nBitLength | `number` | Bit length (8 or 16) |

**Returns:** `number` - Extracted value

Extract a value from DWORD data by bit length (uint8 or uint16).
