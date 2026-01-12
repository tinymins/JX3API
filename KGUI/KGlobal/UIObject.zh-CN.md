# UI 对象常量

用于拖放操作的 UI 对象类型常量。

---

## UI_OBJECT_* {#UI_OBJECT}

addonapi.lua 导出的 UI 对象类型常量。

| 常量 | 描述 |
|------|------|
| `UI_OBJECT_NOT_OBJ` | 非对象 |
| `UI_OBJECT_PLAYER` | 玩家对象 |
| `UI_OBJECT_PLAYER_ID` | 玩家 ID 对象 |
| `UI_OBJECT_PLAYER_SEARCH` | 玩家搜索对象 |
| `UI_OBJECT_PLAYER_NEARBY` | 附近玩家对象 |
| `UI_OBJECT_NPC` | NPC 对象 |
| `UI_OBJECT_ITEM` | 物品对象 |
| `UI_OBJECT_ITEM_ONLY_ID` | 仅物品 ID 对象 |
| `UI_OBJECT_ITEM_INFO` | 物品信息对象 |
| `UI_OBJECT_SKILL` | 技能对象 |
| `UI_OBJECT_CRAFT` | 生活技能对象 |
| `UI_OBJECT_SKILL_RECIPE` | 技能秘籍对象 |
| `UI_OBJECT_SYS_BTN` | 系统按钮对象 |
| `UI_OBJECT_MACRO` | 宏对象 |
| `UI_OBJECT_MOUNT` | 坐骑对象 |
| `UI_OBJECT_ENCHANT` | 附魔对象 |
| `UI_OBJECT_NOT_NEED_KNOWN` | 无需知道的对象 |

**用法：**

这些常量用于在处理 UI 元素中的拖放操作时识别对象类型。

```lua
-- 示例：检查拖动的对象是否为物品
local nType = this:GetObjectType()
if nType == UI_OBJECT_ITEM then
    -- 处理物品
end

-- 示例：设置用于拖动的对象数据
this:SetObjectType(UI_OBJECT_SKILL)
```
