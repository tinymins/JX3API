# 家园函数

家园（住房系统）相关函数。

---

## 关系中心

### GetRelationCenter {#GetRelationCenter}

```lua
tCenter = GetRelationCenter(nCenterID)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| nCenterID | `number` | 关系中心 ID |

**返回:** `table` - 关系中心数据

获取家园的关系中心信息。

---

## 社区

### DaTangJiaYuan_GoToCommunityIndex {#DaTangJiaYuan_GoToCommunityIndex}

```lua
DaTangJiaYuan_GoToCommunityIndex(nIndex)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| nIndex | `number` | 社区索引 |

**返回:** `void`

导航到大唐家园（家园系统）的社区索引。

---

## 家具

### GetNearbyFurnitureInfoList {#GetNearbyFurnitureInfoList}

```lua
tList = GetNearbyFurnitureInfoList(nRange)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| nRange | `number` | 搜索范围 |

**返回:** `table` - 附近家具信息列表

获取附近家具信息列表。

---

### InteractFurniture {#InteractFurniture}

```lua
InteractFurniture(dwFurnitureID)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| dwFurnitureID | `number` | 家具 ID |

**返回:** `void`

与家具对象交互。

---

### HomeLand_GetFurniture2GameID {#HomeLand_GetFurniture2GameID}

```lua
dwGameID = HomeLand_GetFurniture2GameID(dwFurnitureID)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| dwFurnitureID | `number` | 家具 ID |

**返回:** `number` - 游戏对象 ID

从家具 ID 获取游戏对象 ID。

---

### Homeland_GetFurnitureConfig {#Homeland_GetFurnitureConfig}

```lua
tConfig = Homeland_GetFurnitureConfig(dwFurnitureID)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| dwFurnitureID | `number` | 家具 ID |

**返回:** `table` - 家具配置

获取家具物品的配置。

---

## 小游戏

### HomeLand_GetMiniGameInfo {#HomeLand_GetMiniGameInfo}

```lua
tInfo = HomeLand_GetMiniGameInfo(dwFurnitureID)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| dwFurnitureID | `number` | 家具 ID |

**返回:** `table` - 小游戏信息

获取家具物品的小游戏信息。

---

### HomeLand_GetBoxTypeByItem {#HomeLand_GetBoxTypeByItem}

```lua
nType = HomeLand_GetBoxTypeByItem(dwItemID)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| dwItemID | `number` | 物品 ID |

**返回:** `number` - 盒子类型

通过物品 ID 获取盒子类型。

---

### HousePlayPanel_OnClickBtnSure {#HousePlayPanel_OnClickBtnSure}

```lua
HousePlayPanel_OnClickBtnSure()
```

**返回:** `void`

触发房屋游戏面板中的确认按钮点击。

---

## 脚本

### HomeLand_GetDwordScript {#HomeLand_GetDwordScript}

```lua
tScript = HomeLand_GetDwordScript(nDataType, ...)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| nDataType | `number` | 数据类型（LAND_OBJECT_TYPE 常量） |
| ... | `any` | 附加参数 |

**返回:** `table` - 脚本数据

按类型获取 DWORD 脚本数据。

数据类型：
- `LAND_OBJECT_TYPE.SD_EIGHT_DWORD_SCRIPT`
- `LAND_OBJECT_TYPE.SD_FOUR_DWORD_SCRIPT`
- `LAND_OBJECT_TYPE.FOUR_DWORD_SCRIPT`

---

### HomeLand_CallDwordScript {#HomeLand_CallDwordScript}

```lua
result = HomeLand_CallDwordScript(nDataType, ...)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| nDataType | `number` | 数据类型（LAND_OBJECT_TYPE 常量） |
| ... | `any` | 脚本参数 |

**返回:** `any` - 脚本结果

按类型调用 DWORD 脚本。

---

### HomeLand_GetDWORDValueByuint {#HomeLand_GetDWORDValueByuint}

```lua
nValue = HomeLand_GetDWORDValueByuint(nData, nStart, nBitLength)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| nData | `number` | 源数据 |
| nStart | `number` | 起始位置 |
| nBitLength | `number` | 位长度（8 或 16） |

**返回:** `number` - 提取的值

按位长度（uint8 或 uint16）从 DWORD 数据中提取值。
