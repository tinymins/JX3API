# Hand (Drag & Drop) Functions

Functions for managing the cursor hand object and drag-drop operations.

---

## Hand_IsEmpty {#Hand_IsEmpty}

Check if the hand cursor is empty (not holding anything).

### Syntax

```lua
local bEmpty = Hand_IsEmpty()
```

### Returns

| Type | Description |
|------|-------------|
| `boolean` | true if hand is empty |

### Example

```lua
if Hand_IsEmpty() then
    Output("Not holding anything")
end
```

---

## Hand_Clear {#Hand_Clear}

Clear the hand cursor, dropping any held object.

### Syntax

```lua
Hand_Clear()
```

### Example

```lua
-- Cancel drag operation
if not Hand_IsEmpty() then
    Hand_Clear()
end
```

---

## Hand_Get {#Hand_Get}

Get information about the currently held object.

### Syntax

```lua
local nType, ... = Hand_Get()
```

### Returns

| Type | Description |
|------|-------------|
| `number` | Object type (UI_OBJECT constant) |
| `...` | Additional data depending on type |

### Object Types

| Type | Additional Returns |
|------|-------------------|
| `UI_OBJECT_ITEM` | dwBox, dwX |
| `UI_OBJECT_SKILL` | dwSkillID, dwLevel |
| `UI_OBJECT_ITEM_INFO` | nTabType, nIndex |

### Example

```lua
local nType = Hand_Get()
if nType == UI_OBJECT_ITEM then
    local _, dwBox, dwX = Hand_Get()
    Output("Holding item from box " .. dwBox .. " slot " .. dwX)
elseif nType == UI_OBJECT_SKILL then
    local _, dwSkillID, dwLevel = Hand_Get()
    Output("Holding skill " .. dwSkillID)
end
```

---

## Hand_Pick {#Hand_Pick}

Pick up an object to the hand cursor.

### Syntax

```lua
Hand_Pick(nType, ...)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `nType` | `number` | Object type (UI_OBJECT constant) |
| `...` | `any` | Additional parameters based on type |

### Pick Item

```lua
-- Pick up item from inventory
Hand_Pick(UI_OBJECT_ITEM, INVENTORY_INDEX.PACKAGE, nSlotIndex)
```

### Pick Skill

```lua
-- Pick up a skill
Hand_Pick(UI_OBJECT_SKILL, dwSkillID, nSkillLevel)
```

### Pick Item Info

```lua
-- Pick up item by info
Hand_Pick(UI_OBJECT_ITEM_INFO, nTabType, nIndex)
```

---

## Hand_DropHandObj {#Hand_DropHandObj}

Drop the currently held object at a specific location.

### Syntax

```lua
Hand_DropHandObj(nDestType, ...)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `nDestType` | `number` | Destination type |
| `...` | `any` | Destination parameters |

---

## IsCursorInExclusiveMode {#IsCursorInExclusiveMode}

Check if cursor is in exclusive mode (e.g., ground targeting).

### Syntax

```lua
local bExclusive = IsCursorInExclusiveMode()
```

### Returns

| Type | Description |
|------|-------------|
| `boolean` | true if in exclusive mode |

### Example

```lua
if IsCursorInExclusiveMode() then
    -- Don't process normal click
    return
end
```

---

## Usage Examples

### Drag Item Between Slots

```lua
-- On source slot click
function OnSourceSlotClick()
    if Hand_IsEmpty() then
        -- Pick up item
        local dwBox = INVENTORY_INDEX.PACKAGE
        local dwSlot = 0
        Hand_Pick(UI_OBJECT_ITEM, dwBox, dwSlot)
    end
end

-- On destination slot click
function OnDestSlotClick()
    if not Hand_IsEmpty() then
        local nType, dwBox, dwSlot = Hand_Get()
        if nType == UI_OBJECT_ITEM then
            -- Perform item move operation
            Output("Moving item from " .. dwSlot)
            Hand_Clear()
        end
    end
end
```

### Check Hand Content

```lua
function GetHandDescription()
    if Hand_IsEmpty() then
        return "Empty"
    end

    local nType = Hand_Get()
    if nType == UI_OBJECT_ITEM then
        local _, dwBox, dwX = Hand_Get()
        local item = GetPlayerItem(dwBox, dwX)
        if item then
            return "Item: " .. GetItemNameByItem(item)
        end
    elseif nType == UI_OBJECT_SKILL then
        local _, dwSkillID, dwLevel = Hand_Get()
        return "Skill: " .. Table_GetSkillName(dwSkillID, dwLevel)
    end

    return "Unknown object"
end
```

### Skill Bar Assignment

```lua
-- Pick skill to assign to action bar
function PickSkillForActionBar(dwSkillID, nLevel)
    if not Hand_IsEmpty() then
        Hand_Clear()
    end
    Hand_Pick(UI_OBJECT_SKILL, dwSkillID, nLevel)
    Output("Click an action bar slot to assign skill")
end
```

---

## See Also

- [UIObject Constants](./UIObject.md) - UI object type constants
- [Misc Functions](./Misc.md) - Miscellaneous utility functions
