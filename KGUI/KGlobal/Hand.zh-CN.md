# Hand 拖放函数

用于管理光标手持对象和拖放操作的函数。

---

## Hand_IsEmpty {#Hand_IsEmpty}

检查手持光标是否为空（没有持有任何物品）。

### 语法

```lua
local bEmpty = Hand_IsEmpty()
```

### 返回值

| 类型 | 说明 |
|------|------|
| `boolean` | 如果手持为空返回 true |

### 示例

```lua
if Hand_IsEmpty() then
    Output("没有持有任何物品")
end
```

---

## Hand_Clear {#Hand_Clear}

清除手持光标，放下任何持有的对象。

### 语法

```lua
Hand_Clear()
```

### 示例

```lua
-- 取消拖动操作
if not Hand_IsEmpty() then
    Hand_Clear()
end
```

---

## Hand_Get {#Hand_Get}

获取当前持有对象的信息。

### 语法

```lua
local nType, ... = Hand_Get()
```

### 返回值

| 类型 | 说明 |
|------|------|
| `number` | 对象类型（UI_OBJECT 常量） |
| `...` | 根据类型不同的附加数据 |

### 对象类型

| 类型 | 附加返回值 |
|------|-----------|
| `UI_OBJECT_ITEM` | dwBox, dwX |
| `UI_OBJECT_SKILL` | dwSkillID, dwLevel |
| `UI_OBJECT_ITEM_INFO` | nTabType, nIndex |

### 示例

```lua
local nType = Hand_Get()
if nType == UI_OBJECT_ITEM then
    local _, dwBox, dwX = Hand_Get()
    Output("持有背包 " .. dwBox .. " 格子 " .. dwX .. " 的物品")
elseif nType == UI_OBJECT_SKILL then
    local _, dwSkillID, dwLevel = Hand_Get()
    Output("持有技能 " .. dwSkillID)
end
```

---

## Hand_Pick {#Hand_Pick}

拾取一个对象到手持光标。

### 语法

```lua
Hand_Pick(nType, ...)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `nType` | `number` | 对象类型（UI_OBJECT 常量） |
| `...` | `any` | 根据类型不同的附加参数 |

### 拾取物品

```lua
-- 从背包拾取物品
Hand_Pick(UI_OBJECT_ITEM, INVENTORY_INDEX.PACKAGE, nSlotIndex)
```

### 拾取技能

```lua
-- 拾取一个技能
Hand_Pick(UI_OBJECT_SKILL, dwSkillID, nSkillLevel)
```

### 拾取物品信息

```lua
-- 通过物品信息拾取
Hand_Pick(UI_OBJECT_ITEM_INFO, nTabType, nIndex)
```

---

## Hand_DropHandObj {#Hand_DropHandObj}

将当前持有的对象放置到指定位置。

### 语法

```lua
Hand_DropHandObj(nDestType, ...)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `nDestType` | `number` | 目标类型 |
| `...` | `any` | 目标参数 |

---

## IsCursorInExclusiveMode {#IsCursorInExclusiveMode}

检查光标是否处于独占模式（如地面目标选择）。

### 语法

```lua
local bExclusive = IsCursorInExclusiveMode()
```

### 返回值

| 类型 | 说明 |
|------|------|
| `boolean` | 如果处于独占模式返回 true |

### 示例

```lua
if IsCursorInExclusiveMode() then
    -- 不处理普通点击
    return
end
```

---

## 使用示例

### 在格子间拖动物品

```lua
-- 源格子点击事件
function OnSourceSlotClick()
    if Hand_IsEmpty() then
        -- 拾取物品
        local dwBox = INVENTORY_INDEX.PACKAGE
        local dwSlot = 0
        Hand_Pick(UI_OBJECT_ITEM, dwBox, dwSlot)
    end
end

-- 目标格子点击事件
function OnDestSlotClick()
    if not Hand_IsEmpty() then
        local nType, dwBox, dwSlot = Hand_Get()
        if nType == UI_OBJECT_ITEM then
            -- 执行物品移动操作
            Output("从格子 " .. dwSlot .. " 移动物品")
            Hand_Clear()
        end
    end
end
```

### 检查手持内容

```lua
function GetHandDescription()
    if Hand_IsEmpty() then
        return "空"
    end

    local nType = Hand_Get()
    if nType == UI_OBJECT_ITEM then
        local _, dwBox, dwX = Hand_Get()
        local item = GetPlayerItem(dwBox, dwX)
        if item then
            return "物品：" .. GetItemNameByItem(item)
        end
    elseif nType == UI_OBJECT_SKILL then
        local _, dwSkillID, dwLevel = Hand_Get()
        return "技能：" .. Table_GetSkillName(dwSkillID, dwLevel)
    end

    return "未知对象"
end
```

### 技能栏分配

```lua
-- 拾取技能以分配到动作栏
function PickSkillForActionBar(dwSkillID, nLevel)
    if not Hand_IsEmpty() then
        Hand_Clear()
    end
    Hand_Pick(UI_OBJECT_SKILL, dwSkillID, nLevel)
    Output("点击动作栏格子以分配技能")
end
```

---

## 相关链接

- [UI 对象常量](./UIObject.zh-CN.md) - UI 对象类型常量
- [杂项函数](./Misc.zh-CN.md) - 杂项工具函数
