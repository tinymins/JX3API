# ItemBox 更新函数

用于更新和管理物品格子及 UI 物品显示的函数。

---

## UpdateBoxObject {#UpdateBoxObject}

用对象数据更新格子。

### 语法

```lua
UpdateBoxObject(box, nType, ...)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `box` | `ItemBox` | ItemBox 元素 |
| `nType` | `number` | 对象类型（UI_OBJECT 常量） |
| `...` | `any` | 根据类型不同的附加参数 |

---

## UpdataItemBoxObject {#UpdataItemBoxObject}

用物品数据更新物品格子。

### 语法

```lua
UpdataItemBoxObject(box, item, bShowBinding)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `box` | `ItemBox` | ItemBox 元素 |
| `item` | `KGItem` | 物品对象 |
| `bShowBinding` | `boolean` | 是否显示绑定状态 |

### 示例

```lua
local item = GetPlayerItem(INVENTORY_INDEX.PACKAGE, 0)
local box = this:Lookup("Box_Item")
if item and box then
    UpdataItemBoxObject(box, item, true)
end
```

---

## UpdataItemInfoBoxObject {#UpdataItemInfoBoxObject}

用物品信息数据更新物品格子。

### 语法

```lua
UpdataItemInfoBoxObject(box, nTabType, nIndex)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `box` | `ItemBox` | ItemBox 元素 |
| `nTabType` | `number` | 物品表类型 |
| `nIndex` | `number` | 物品索引 |

---

## UpdateSkillRecipeBoxObject {#UpdateSkillRecipeBoxObject}

用技能秘籍数据更新格子。

### 语法

```lua
UpdateSkillRecipeBoxObject(box, dwRecipeID)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `box` | `ItemBox` | ItemBox 元素 |
| `dwRecipeID` | `number` | 秘籍 ID |

---

## UpdateMountBoxObject {#UpdateMountBoxObject}

用坐骑数据更新格子。

### 语法

```lua
UpdateMountBoxObject(box, dwMountID)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `box` | `ItemBox` | ItemBox 元素 |
| `dwMountID` | `number` | 坐骑 ID |

---

## UpdateItemBoxExtend {#UpdateItemBoxExtend}

用扩展信息更新物品格子。

### 语法

```lua
UpdateItemBoxExtend(box, item, bShowCount, bShowCooldown)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `box` | `ItemBox` | ItemBox 元素 |
| `item` | `KGItem` | 物品对象 |
| `bShowCount` | `boolean` | 显示物品数量 |
| `bShowCooldown` | `boolean` | 显示冷却遮罩 |

---

## UpdataItemCDProgress {#UpdataItemCDProgress}

更新物品冷却进度显示。

### 语法

```lua
UpdataItemCDProgress(box, item)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `box` | `ItemBox` | ItemBox 元素 |
| `item` | `KGItem` | 物品对象 |

### 示例

```lua
-- 在呼吸函数中更新 CD 进度
function OnBreathe()
    local item = GetPlayerItem(INVENTORY_INDEX.EQUIP, EQUIPMENT_INVENTORY.MELEE_WEAPON)
    if item then
        UpdataItemCDProgress(this, item)
    end
end
```

---

## UpdataSkillCDProgress {#UpdataSkillCDProgress}

更新技能冷却进度显示。

### 语法

```lua
UpdataSkillCDProgress(box, dwSkillID, nLevel)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `box` | `ItemBox` | ItemBox 元素 |
| `dwSkillID` | `number` | 技能 ID |
| `nLevel` | `number` | 技能等级 |

---

## 物品交互函数

### OnUseItem {#OnUseItem}

处理使用物品操作。

```lua
OnUseItem(item)
```

### OnSplitBoxItem {#OnSplitBoxItem}

处理拆分物品操作。

```lua
OnSplitBoxItem(dwBox, dwX, nCount)
```

### OnExchangeItem {#OnExchangeItem}

处理格子间物品交换。

```lua
OnExchangeItem(dwSrcBox, dwSrcX, dwDestBox, dwDestX)
```

### OnDestroyItem {#OnDestroyItem}

处理销毁物品操作。

```lua
OnDestroyItem(item)
```

### OnDestroyItemTable {#OnDestroyItemTable}

处理从物品表销毁物品。

```lua
OnDestroyItemTable(nTabType, nIndex)
```

---

## 物品工具函数

### GetItemFontColorByQuality {#GetItemFontColorByQuality}

根据物品品质获取字体颜色。

### 语法

```lua
local r, g, b = GetItemFontColorByQuality(nQuality)
```

### 品质颜色

| 品质 | 颜色 |
|------|------|
| 0（灰色） | 灰色 |
| 1（白色） | 白色 |
| 2（绿色） | 绿色 |
| 3（蓝色） | 蓝色 |
| 4（紫色） | 紫色 |
| 5（橙色） | 橙色 |

---

### GetWeapenType {#GetWeapenType}

获取武器类型字符串。

```lua
local szType = GetWeapenType(nWeaponType)
```

---

### GetItemNameByUIID {#GetItemNameByUIID}

通过 UI ID 获取物品名称。

```lua
local szName = GetItemNameByUIID(nUIID)
```

---

### GetItemPosByItemTypeIndex {#GetItemPosByItemTypeIndex}

通过类型和索引获取物品位置。

```lua
local dwBox, dwX = GetItemPosByItemTypeIndex(nTabType, nIndex)
```

---

### GetItemPosInPackage {#GetItemPosInPackage}

获取物品在背包中的位置。

```lua
local dwBox, dwX = GetItemPosInPackage(item)
```

---

### PlayItemSound {#PlayItemSound}

播放物品拾取/放下音效。

```lua
PlayItemSound(item, bPickup)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `item` | `KGItem` | 物品对象 |
| `bPickup` | `boolean` | true 为拾取，false 为放下 |

---

### FormatAttributeValue {#FormatAttributeValue}

格式化属性值用于显示。

```lua
local szValue = FormatAttributeValue(nAttributeID, nValue)
```

---

## 示例：完整物品格子设置

```lua
-- 初始化物品格子
function InitItemBox(box, item)
    if not item then
        box:ClearObject()
        return
    end

    -- 用物品更新格子
    UpdataItemBoxObject(box, item, true)

    -- 设置品质边框颜色
    local r, g, b = GetItemFontColorByQuality(item.nQuality)
    box:SetOverText(0, tostring(item.nStackNum))
    box:SetOverTextFontColor(0, r, g, b)
end

-- 处理物品格子点击
function OnItemBoxClick()
    if not Hand_IsEmpty() then
        -- 放下物品到这里
        local nType, dwSrcBox, dwSrcX = Hand_Get()
        if nType == UI_OBJECT_ITEM then
            local dwDestBox = this.dwBox
            local dwDestX = this.dwX
            OnExchangeItem(dwSrcBox, dwSrcX, dwDestBox, dwDestX)
        end
        Hand_Clear()
    else
        -- 拾取物品
        local item = GetPlayerItem(this.dwBox, this.dwX)
        if item then
            Hand_Pick(UI_OBJECT_ITEM, this.dwBox, this.dwX)
        end
    end
end

-- 在呼吸函数中更新冷却
function OnBreathItemBox()
    local item = GetPlayerItem(this.dwBox, this.dwX)
    if item then
        UpdataItemCDProgress(this, item)
    end
end
```

---

## 相关链接

- [拖放函数](./Hand.zh-CN.md) - 拖放函数
- [Tooltip 函数](./Tooltip.zh-CN.md) - 提示框显示函数
- [UI 对象常量](./UIObject.zh-CN.md) - UI 对象类型常量
