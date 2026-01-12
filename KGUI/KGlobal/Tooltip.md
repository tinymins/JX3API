# Tooltip Functions

Functions for displaying tooltips and tips in the game UI.

---

## OutputTip {#OutputTip}

Display a general tooltip at cursor position.

### Syntax

```lua
OutputTip(szText, nPosX, nPosY)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `szText` | `string` | Formatted text to display |
| `nPosX` | `number` | X position (optional, cursor if nil) |
| `nPosY` | `number` | Y position (optional, cursor if nil) |

---

## HideTip {#HideTip}

Hide the currently displayed tooltip.

### Syntax

```lua
HideTip()
```

---

## OutputItemTip {#OutputItemTip}

Display a tooltip for an item.

### Syntax

```lua
OutputItemTip(item, rect, bShowPrice, bShowFE)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `item` | `KGItem` | Item object |
| `rect` | `table` | Position rect {x, y, w, h} or nil for cursor |
| `bShowPrice` | `boolean` | Show price info |
| `bShowFE` | `boolean` | Show enchant info |

---

## GetItemTip {#GetItemTip}

Get item tooltip text without displaying it.

### Syntax

```lua
local szTip = GetItemTip(item)
```

### Returns

| Type | Description |
|------|-------------|
| `string` | Formatted tooltip text |

---

## GetItemInfoTip {#GetItemInfoTip}

Get tooltip for item info (from table data).

### Syntax

```lua
local szTip = GetItemInfoTip(itemInfo)
```

---

## GetItemNameByItem {#GetItemNameByItem}

Get item name from item object.

### Syntax

```lua
local szName = GetItemNameByItem(item)
```

---

## GetItemNameByItemInfo {#GetItemNameByItemInfo}

Get item name from item info table.

### Syntax

```lua
local szName = GetItemNameByItemInfo(itemInfo)
```

---

## OutputSkillTip {#OutputSkillTip}

Display a skill tooltip.

### Syntax

```lua
OutputSkillTip(dwSkillID, nSkillLevel, rect)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `dwSkillID` | `number` | Skill ID |
| `nSkillLevel` | `number` | Skill level |
| `rect` | `table` | Position rect or nil |

---

## OutputSkillLink {#OutputSkillLink}

Create a skill link for chat.

### Syntax

```lua
local szLink = OutputSkillLink(dwSkillID, nSkillLevel)
```

---

## OutputSkillRecipeTip {#OutputSkillRecipeTip}

Display a skill recipe tooltip.

### Syntax

```lua
OutputSkillRecipeTip(dwRecipeID, rect)
```

---

## OutputBuffTip {#OutputBuffTip}

Display a buff tooltip.

### Syntax

```lua
OutputBuffTip(dwCharacterID, bBuff, nIndex, rect)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `dwCharacterID` | `number` | Target character ID |
| `bBuff` | `boolean` | true for buff, false for debuff |
| `nIndex` | `number` | Buff index |
| `rect` | `table` | Position rect or nil |

---

## GetBuffDesc {#GetBuffDesc}

Get buff description text.

### Syntax

```lua
local szDesc = GetBuffDesc(dwBuffID, nBuffLevel)
```

---

## GetBindBuffDesc {#GetBindBuffDesc}

Get bind buff description.

### Syntax

```lua
local szDesc = GetBindBuffDesc(dwBuffID, nBuffLevel)
```

---

## OutputQuestTip {#OutputQuestTip}

Display a quest tooltip.

### Syntax

```lua
OutputQuestTip(dwQuestID, rect)
```

---

## OutputDoodadTip {#OutputDoodadTip}

Display a doodad (interactive object) tooltip.

### Syntax

```lua
OutputDoodadTip(doodad, rect)
```

---

## GetDoodadQuestTip {#GetDoodadQuestTip}

Get quest-related tooltip for a doodad.

### Syntax

```lua
local szTip = GetDoodadQuestTip(doodad)
```

---

## OutputCraftTip {#OutputCraftTip}

Display a craft tooltip.

### Syntax

```lua
OutputCraftTip(dwCraftID, nCraftLevel, rect)
```

---

## OutputEnchantTip {#OutputEnchantTip}

Display an enchant tooltip.

### Syntax

```lua
OutputEnchantTip(dwEnchantID, rect)
```

---

## OutputEnchantLink {#OutputEnchantLink}

Create an enchant link for chat.

### Syntax

```lua
local szLink = OutputEnchantLink(dwEnchantID)
```

---

## OutputBookTipByID {#OutputBookTipByID}

Display a book/recipe tooltip by ID.

### Syntax

```lua
OutputBookTipByID(dwBookID, dwRecipeID, rect)
```

---

## GetBookTipByItem {#GetBookTipByItem}

Get book tooltip from item.

### Syntax

```lua
local szTip = GetBookTipByItem(item)
```

---

## GetBookTipByItemInfo {#GetBookTipByItemInfo}

Get book tooltip from item info.

### Syntax

```lua
local szTip = GetBookTipByItemInfo(itemInfo)
```

---

## OutputRecipeLink {#OutputRecipeLink}

Create a recipe link for chat.

### Syntax

```lua
local szLink = OutputRecipeLink(dwRecipeID)
```

---

## OutputPendantTip {#OutputPendantTip}

Display a pendant (accessory) tooltip.

### Syntax

```lua
OutputPendantTip(dwPendantID, rect)
```

---

## OutputAchievementTip {#OutputAchievementTip}

Display an achievement tooltip.

### Syntax

```lua
OutputAchievementTip(dwAchievementID, rect)
```

---

## OutputDesignationTip {#OutputDesignationTip}

Display a designation (title) tooltip.

### Syntax

```lua
OutputDesignationTip(dwDesignationID, rect)
```

---

## OutputTeamMemberTip {#OutputTeamMemberTip}

Display team member tooltip.

### Syntax

```lua
OutputTeamMemberTip(dwMemberID, rect)
```

---

## OutputActivityTip {#OutputActivityTip}

Display activity tooltip.

### Syntax

```lua
OutputActivityTip(dwActivityID, rect)
```

---

## OutputFieldPQTip {#OutputFieldPQTip}

Display field PQ (public quest) tooltip.

### Syntax

```lua
OutputFieldPQTip(dwPQID, rect)
```

---

## Example Usage

```lua
-- Show item tooltip on mouse enter
function OnItemMouseEnter()
    local item = GetPlayerItem(INVENTORY_INDEX.PACKAGE, 0)
    if item then
        local x, y = this:GetAbsPos()
        local w, h = this:GetSize()
        OutputItemTip(item, {x, y, w, h})
    end
end

-- Hide tooltip on mouse leave
function OnItemMouseLeave()
    HideTip()
end

-- Show skill tooltip
function OnSkillIconMouseEnter()
    local dwSkillID = 123
    local nLevel = 10
    OutputSkillTip(dwSkillID, nLevel)
end

-- Get item info for custom display
function ShowCustomItemInfo(item)
    local szName = GetItemNameByItem(item)
    local szTip = GetItemTip(item)
    Output("Item: " .. szName)
end
```

---

## See Also

- [Dialog Functions](./Dialog.md) - Message box and dialog functions
- [UI Functions](./UI.md) - General UI functions
