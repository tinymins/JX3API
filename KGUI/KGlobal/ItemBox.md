# ItemBox Update Functions

Functions for updating and managing item boxes and UI item displays.

---

## UpdateBoxObject {#UpdateBoxObject}

Update a box with object data.

### Syntax

```lua
UpdateBoxObject(box, nType, ...)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `box` | `ItemBox` | The ItemBox element |
| `nType` | `number` | Object type (UI_OBJECT constant) |
| `...` | `any` | Additional parameters based on type |

---

## UpdataItemBoxObject {#UpdataItemBoxObject}

Update an item box with item data.

### Syntax

```lua
UpdataItemBoxObject(box, item, bShowBinding)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `box` | `ItemBox` | The ItemBox element |
| `item` | `KGItem` | Item object |
| `bShowBinding` | `boolean` | Whether to show binding status |

### Example

```lua
local item = GetPlayerItem(INVENTORY_INDEX.PACKAGE, 0)
local box = this:Lookup("Box_Item")
if item and box then
    UpdataItemBoxObject(box, item, true)
end
```

---

## UpdataItemInfoBoxObject {#UpdataItemInfoBoxObject}

Update an item box with item info data.

### Syntax

```lua
UpdataItemInfoBoxObject(box, nTabType, nIndex)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `box` | `ItemBox` | The ItemBox element |
| `nTabType` | `number` | Item tab type |
| `nIndex` | `number` | Item index |

---

## UpdateSkillRecipeBoxObject {#UpdateSkillRecipeBoxObject}

Update a box with skill recipe data.

### Syntax

```lua
UpdateSkillRecipeBoxObject(box, dwRecipeID)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `box` | `ItemBox` | The ItemBox element |
| `dwRecipeID` | `number` | Recipe ID |

---

## UpdateMountBoxObject {#UpdateMountBoxObject}

Update a box with mount data.

### Syntax

```lua
UpdateMountBoxObject(box, dwMountID)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `box` | `ItemBox` | The ItemBox element |
| `dwMountID` | `number` | Mount ID |

---

## UpdateItemBoxExtend {#UpdateItemBoxExtend}

Update item box with extended information.

### Syntax

```lua
UpdateItemBoxExtend(box, item, bShowCount, bShowCooldown)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `box` | `ItemBox` | The ItemBox element |
| `item` | `KGItem` | Item object |
| `bShowCount` | `boolean` | Show item count |
| `bShowCooldown` | `boolean` | Show cooldown overlay |

---

## UpdataItemCDProgress {#UpdataItemCDProgress}

Update item cooldown progress display.

### Syntax

```lua
UpdataItemCDProgress(box, item)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `box` | `ItemBox` | The ItemBox element |
| `item` | `KGItem` | Item object |

### Example

```lua
-- Update CD progress in breathe call
function OnBreathe()
    local item = GetPlayerItem(INVENTORY_INDEX.EQUIP, EQUIPMENT_INVENTORY.MELEE_WEAPON)
    if item then
        UpdataItemCDProgress(this, item)
    end
end
```

---

## UpdataSkillCDProgress {#UpdataSkillCDProgress}

Update skill cooldown progress display.

### Syntax

```lua
UpdataSkillCDProgress(box, dwSkillID, nLevel)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `box` | `ItemBox` | The ItemBox element |
| `dwSkillID` | `number` | Skill ID |
| `nLevel` | `number` | Skill level |

---

## Item Interaction Functions

### OnUseItem {#OnUseItem}

Handle item use action.

```lua
OnUseItem(item)
```

### OnSplitBoxItem {#OnSplitBoxItem}

Handle item split action.

```lua
OnSplitBoxItem(dwBox, dwX, nCount)
```

### OnExchangeItem {#OnExchangeItem}

Handle item exchange between slots.

```lua
OnExchangeItem(dwSrcBox, dwSrcX, dwDestBox, dwDestX)
```

### OnDestroyItem {#OnDestroyItem}

Handle item destroy action.

```lua
OnDestroyItem(item)
```

### OnDestroyItemTable {#OnDestroyItemTable}

Handle destroying items from item table.

```lua
OnDestroyItemTable(nTabType, nIndex)
```

---

## Item Utility Functions

### GetItemFontColorByQuality {#GetItemFontColorByQuality}

Get font color based on item quality.

### Syntax

```lua
local r, g, b = GetItemFontColorByQuality(nQuality)
```

### Quality Colors

| Quality | Color |
|---------|-------|
| 0 (Gray) | Gray |
| 1 (White) | White |
| 2 (Green) | Green |
| 3 (Blue) | Blue |
| 4 (Purple) | Purple |
| 5 (Orange) | Orange |

---

### GetWeapenType {#GetWeapenType}

Get weapon type string.

```lua
local szType = GetWeapenType(nWeaponType)
```

---

### GetItemNameByUIID {#GetItemNameByUIID}

Get item name by UI ID.

```lua
local szName = GetItemNameByUIID(nUIID)
```

---

### GetItemPosByItemTypeIndex {#GetItemPosByItemTypeIndex}

Get item position by type and index.

```lua
local dwBox, dwX = GetItemPosByItemTypeIndex(nTabType, nIndex)
```

---

### GetItemPosInPackage {#GetItemPosInPackage}

Get item position in package.

```lua
local dwBox, dwX = GetItemPosInPackage(item)
```

---

### PlayItemSound {#PlayItemSound}

Play item pickup/drop sound.

```lua
PlayItemSound(item, bPickup)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `item` | `KGItem` | Item object |
| `bPickup` | `boolean` | true for pickup, false for drop |

---

### FormatAttributeValue {#FormatAttributeValue}

Format attribute value for display.

```lua
local szValue = FormatAttributeValue(nAttributeID, nValue)
```

---

## Example: Complete Item Box Setup

```lua
-- Initialize item box
function InitItemBox(box, item)
    if not item then
        box:ClearObject()
        return
    end

    -- Update box with item
    UpdataItemBoxObject(box, item, true)

    -- Set quality border color
    local r, g, b = GetItemFontColorByQuality(item.nQuality)
    box:SetOverText(0, tostring(item.nStackNum))
    box:SetOverTextFontColor(0, r, g, b)
end

-- Handle item box click
function OnItemBoxClick()
    if not Hand_IsEmpty() then
        -- Drop item here
        local nType, dwSrcBox, dwSrcX = Hand_Get()
        if nType == UI_OBJECT_ITEM then
            local dwDestBox = this.dwBox
            local dwDestX = this.dwX
            OnExchangeItem(dwSrcBox, dwSrcX, dwDestBox, dwDestX)
        end
        Hand_Clear()
    else
        -- Pick up item
        local item = GetPlayerItem(this.dwBox, this.dwX)
        if item then
            Hand_Pick(UI_OBJECT_ITEM, this.dwBox, this.dwX)
        end
    end
end

-- Update cooldown in breathe
function OnBreathItemBox()
    local item = GetPlayerItem(this.dwBox, this.dwX)
    if item then
        UpdataItemCDProgress(this, item)
    end
end
```

---

## See Also

- [Hand Functions](./Hand.md) - Drag and drop functions
- [Tooltip Functions](./Tooltip.md) - Tooltip display functions
- [UIObject Constants](./UIObject.md) - UI object type constants
