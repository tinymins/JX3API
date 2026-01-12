# UI Object Constants

UI object type constants used for drag and drop operations.

---

## UI_OBJECT_* {#UI_OBJECT}

UI object type constants exported from addonapi.lua.

| Constant | Description |
|----------|-------------|
| `UI_OBJECT_NOT_OBJ` | Not an object |
| `UI_OBJECT_PLAYER` | Player object |
| `UI_OBJECT_PLAYER_ID` | Player ID object |
| `UI_OBJECT_PLAYER_SEARCH` | Player search object |
| `UI_OBJECT_PLAYER_NEARBY` | Player nearby object |
| `UI_OBJECT_NPC` | NPC object |
| `UI_OBJECT_ITEM` | Item object |
| `UI_OBJECT_ITEM_ONLY_ID` | Item only ID object |
| `UI_OBJECT_ITEM_INFO` | Item info object |
| `UI_OBJECT_SKILL` | Skill object |
| `UI_OBJECT_CRAFT` | Craft object |
| `UI_OBJECT_SKILL_RECIPE` | Skill recipe object |
| `UI_OBJECT_SYS_BTN` | System button object |
| `UI_OBJECT_MACRO` | Macro object |
| `UI_OBJECT_MOUNT` | Mount object |
| `UI_OBJECT_ENCHANT` | Enchant object |
| `UI_OBJECT_NOT_NEED_KNOWN` | Not need known object |

**Usage:**

These constants are used to identify the type of object when handling drag and drop operations in UI elements.

```lua
-- Example: Check if dragged object is an item
local nType = this:GetObjectType()
if nType == UI_OBJECT_ITEM then
    -- Handle item
end

-- Example: Set object data for dragging
this:SetObjectType(UI_OBJECT_SKILL)
```
