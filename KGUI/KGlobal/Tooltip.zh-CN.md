# Tooltip 函数

用于在游戏 UI 中显示提示框的函数。

---

## OutputTip {#OutputTip}

在光标位置显示通用提示框。

### 语法

```lua
OutputTip(szText, nPosX, nPosY)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `szText` | `string` | 要显示的格式化文本 |
| `nPosX` | `number` | X 坐标（可选，为 nil 时跟随光标） |
| `nPosY` | `number` | Y 坐标（可选，为 nil 时跟随光标） |

---

## HideTip {#HideTip}

隐藏当前显示的提示框。

### 语法

```lua
HideTip()
```

---

## OutputItemTip {#OutputItemTip}

显示物品提示框。

### 语法

```lua
OutputItemTip(item, rect, bShowPrice, bShowFE)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `item` | `KGItem` | 物品对象 |
| `rect` | `table` | 位置矩形 {x, y, w, h} 或 nil 跟随光标 |
| `bShowPrice` | `boolean` | 是否显示价格信息 |
| `bShowFE` | `boolean` | 是否显示附魔信息 |

---

## GetItemTip {#GetItemTip}

获取物品提示文本但不显示。

### 语法

```lua
local szTip = GetItemTip(item)
```

### 返回值

| 类型 | 说明 |
|------|------|
| `string` | 格式化的提示文本 |

---

## GetItemInfoTip {#GetItemInfoTip}

获取物品信息提示（来自表格数据）。

### 语法

```lua
local szTip = GetItemInfoTip(itemInfo)
```

---

## GetItemNameByItem {#GetItemNameByItem}

从物品对象获取物品名称。

### 语法

```lua
local szName = GetItemNameByItem(item)
```

---

## GetItemNameByItemInfo {#GetItemNameByItemInfo}

从物品信息表获取物品名称。

### 语法

```lua
local szName = GetItemNameByItemInfo(itemInfo)
```

---

## OutputSkillTip {#OutputSkillTip}

显示技能提示框。

### 语法

```lua
OutputSkillTip(dwSkillID, nSkillLevel, rect)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `dwSkillID` | `number` | 技能 ID |
| `nSkillLevel` | `number` | 技能等级 |
| `rect` | `table` | 位置矩形或 nil |

---

## OutputSkillLink {#OutputSkillLink}

创建技能聊天链接。

### 语法

```lua
local szLink = OutputSkillLink(dwSkillID, nSkillLevel)
```

---

## OutputSkillRecipeTip {#OutputSkillRecipeTip}

显示技能秘籍提示框。

### 语法

```lua
OutputSkillRecipeTip(dwRecipeID, rect)
```

---

## OutputBuffTip {#OutputBuffTip}

显示 Buff 提示框。

### 语法

```lua
OutputBuffTip(dwCharacterID, bBuff, nIndex, rect)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `dwCharacterID` | `number` | 目标角色 ID |
| `bBuff` | `boolean` | true 为增益，false 为减益 |
| `nIndex` | `number` | Buff 索引 |
| `rect` | `table` | 位置矩形或 nil |

---

## GetBuffDesc {#GetBuffDesc}

获取 Buff 描述文本。

### 语法

```lua
local szDesc = GetBuffDesc(dwBuffID, nBuffLevel)
```

---

## GetBindBuffDesc {#GetBindBuffDesc}

获取绑定 Buff 描述。

### 语法

```lua
local szDesc = GetBindBuffDesc(dwBuffID, nBuffLevel)
```

---

## OutputQuestTip {#OutputQuestTip}

显示任务提示框。

### 语法

```lua
OutputQuestTip(dwQuestID, rect)
```

---

## OutputDoodadTip {#OutputDoodadTip}

显示交互物件提示框。

### 语法

```lua
OutputDoodadTip(doodad, rect)
```

---

## GetDoodadQuestTip {#GetDoodadQuestTip}

获取交互物件的任务相关提示。

### 语法

```lua
local szTip = GetDoodadQuestTip(doodad)
```

---

## OutputCraftTip {#OutputCraftTip}

显示生活技能提示框。

### 语法

```lua
OutputCraftTip(dwCraftID, nCraftLevel, rect)
```

---

## OutputEnchantTip {#OutputEnchantTip}

显示附魔提示框。

### 语法

```lua
OutputEnchantTip(dwEnchantID, rect)
```

---

## OutputEnchantLink {#OutputEnchantLink}

创建附魔聊天链接。

### 语法

```lua
local szLink = OutputEnchantLink(dwEnchantID)
```

---

## OutputBookTipByID {#OutputBookTipByID}

通过 ID 显示书籍/配方提示框。

### 语法

```lua
OutputBookTipByID(dwBookID, dwRecipeID, rect)
```

---

## GetBookTipByItem {#GetBookTipByItem}

从物品获取书籍提示。

### 语法

```lua
local szTip = GetBookTipByItem(item)
```

---

## GetBookTipByItemInfo {#GetBookTipByItemInfo}

从物品信息获取书籍提示。

### 语法

```lua
local szTip = GetBookTipByItemInfo(itemInfo)
```

---

## OutputRecipeLink {#OutputRecipeLink}

创建配方聊天链接。

### 语法

```lua
local szLink = OutputRecipeLink(dwRecipeID)
```

---

## OutputPendantTip {#OutputPendantTip}

显示挂件提示框。

### 语法

```lua
OutputPendantTip(dwPendantID, rect)
```

---

## OutputAchievementTip {#OutputAchievementTip}

显示成就提示框。

### 语法

```lua
OutputAchievementTip(dwAchievementID, rect)
```

---

## OutputDesignationTip {#OutputDesignationTip}

显示称号提示框。

### 语法

```lua
OutputDesignationTip(dwDesignationID, rect)
```

---

## OutputTeamMemberTip {#OutputTeamMemberTip}

显示队伍成员提示框。

### 语法

```lua
OutputTeamMemberTip(dwMemberID, rect)
```

---

## OutputActivityTip {#OutputActivityTip}

显示活动提示框。

### 语法

```lua
OutputActivityTip(dwActivityID, rect)
```

---

## OutputFieldPQTip {#OutputFieldPQTip}

显示野外公共任务提示框。

### 语法

```lua
OutputFieldPQTip(dwPQID, rect)
```

---

## 使用示例

```lua
-- 鼠标移入时显示物品提示
function OnItemMouseEnter()
    local item = GetPlayerItem(INVENTORY_INDEX.PACKAGE, 0)
    if item then
        local x, y = this:GetAbsPos()
        local w, h = this:GetSize()
        OutputItemTip(item, {x, y, w, h})
    end
end

-- 鼠标移出时隐藏提示
function OnItemMouseLeave()
    HideTip()
end

-- 显示技能提示
function OnSkillIconMouseEnter()
    local dwSkillID = 123
    local nLevel = 10
    OutputSkillTip(dwSkillID, nLevel)
end

-- 获取物品信息用于自定义显示
function ShowCustomItemInfo(item)
    local szName = GetItemNameByItem(item)
    local szTip = GetItemTip(item)
    Output("物品：" .. szName)
end
```

---

## 相关链接

- [对话框函数](./Dialog.zh-CN.md) - 消息框和对话框函数
- [UI 函数](./UI.zh-CN.md) - 通用 UI 函数
