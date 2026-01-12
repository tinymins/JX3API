# 菜单注册

用于注册和管理游戏中右键菜单的函数。

---

## Addon_RegisterPlayerMenu {#Addon_RegisterPlayerMenu}

为玩家右键菜单注册自定义菜单回调。

### 语法

```lua
Addon_RegisterPlayerMenu(szAddonName, fnCallback)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `szAddonName` | `string` | 插件唯一标识符 |
| `fnCallback` | `function` | 返回菜单项的回调函数 |

### 回调函数

```lua
function fnCallback(dwID, szName)
    -- dwID: 玩家的 dwID
    -- szName: 玩家名称
    -- 返回：菜单项表或 nil
end
```

### 示例

```lua
Addon_RegisterPlayerMenu("MyAddon", function(dwID, szName)
    return {
        {
            szOption = "发送消息",
            fnAction = function()
                Output("你好 " .. szName)
            end,
        },
        {
            szOption = "查看信息",
            fnAction = function()
                ViewPlayerInfo(dwID)
            end,
        },
    }
end)
```

---

## Addon_RegisterTargetMenu {#Addon_RegisterTargetMenu}

为目标右键菜单注册自定义菜单回调。

### 语法

```lua
Addon_RegisterTargetMenu(szAddonName, fnCallback)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `szAddonName` | `string` | 插件唯一标识符 |
| `fnCallback` | `function` | 返回菜单项的回调函数 |

### 示例

```lua
Addon_RegisterTargetMenu("MyAddon", function(dwID)
    local target = GetNpc(dwID) or GetPlayer(dwID)
    if not target then
        return nil
    end
    return {
        {
            szOption = "标记目标",
            fnAction = function()
                SetTeamMark(1, dwID)
            end,
        },
    }
end)
```

---

## Addon_RegisterTraceButtonMenu {#Addon_RegisterTraceButtonMenu}

为追踪按钮右键菜单注册自定义菜单回调。

### 语法

```lua
Addon_RegisterTraceButtonMenu(szAddonName, fnCallback)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `szAddonName` | `string` | 插件唯一标识符 |
| `fnCallback` | `function` | 返回菜单项的回调函数 |

---

## Addon_RegisterPanel {#Addon_RegisterPanel}

在系统设置/插件管理界面中注册插件面板。

### 语法

```lua
Addon_RegisterPanel(szAddonName, szDisplayName, szDescription, szIcon, fnOpenPanel)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `szAddonName` | `string` | 插件唯一标识符 |
| `szDisplayName` | `string` | 面板列表中显示的名称 |
| `szDescription` | `string` | 插件描述 |
| `szIcon` | `string` | 图标路径（可选） |
| `fnOpenPanel` | `function` | 打开面板时的回调 |

### 示例

```lua
Addon_RegisterPanel(
    "MyAddon",
    "我的插件设置",
    "配置我的插件",
    "ui/Image/icon.uitex",
    function()
        OpenMyAddonPanel()
    end
)
```

---

## InsertPlayerMenu {#InsertPlayerMenu}

直接向玩家右键菜单插入菜单项。

### 语法

```lua
InsertPlayerMenu(tMenu)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `tMenu` | `table` | 菜单项表数组 |

### 菜单项结构

| 字段 | 类型 | 说明 |
|------|------|------|
| `szOption` | `string` | 菜单项文本 |
| `fnAction` | `function` | 点击回调 |
| `bDisable` | `boolean` | 禁用状态（可选） |
| `bCheck` | `boolean` | 显示勾选标记（可选） |
| `fnDisable` | `function` | 判断禁用状态的函数（可选） |

---

## InsertTargetMenu {#InsertTargetMenu}

直接向目标右键菜单插入菜单项。

### 语法

```lua
InsertTargetMenu(tMenu)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `tMenu` | `table` | 菜单项表数组 |

---

## InsertTeammateMenu {#InsertTeammateMenu}

向队友右键菜单插入菜单项。

### 语法

```lua
InsertTeammateMenu(tMenu)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `tMenu` | `table` | 菜单项表数组 |

---

## PopupMenu {#PopupMenu}

在当前光标位置显示弹出菜单。

### 语法

```lua
PopupMenu(tMenu)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `tMenu` | `table` | 菜单结构表 |

### 示例

```lua
PopupMenu({
    { szOption = "选项 1", fnAction = function() Output("1") end },
    { szOption = "选项 2", fnAction = function() Output("2") end },
    { bDevide = true },  -- 分隔线
    {
        szOption = "子菜单",
        {
            { szOption = "子选项 1", fnAction = function() end },
            { szOption = "子选项 2", fnAction = function() end },
        }
    },
})
```

---

## 菜单项属性

### 基本属性

| 属性 | 类型 | 说明 |
|------|------|------|
| `szOption` | `string` | 显示文本 |
| `fnAction` | `function` | 点击回调 |
| `bDisable` | `boolean` | 禁用状态 |
| `bCheck` | `boolean` | 显示勾选标记 |
| `bDevide` | `boolean` | 是否为分隔线 |
| `rgb` | `table` | 文本颜色 {r, g, b} |

### 高级属性

| 属性 | 类型 | 说明 |
|------|------|------|
| `szIcon` | `string` | 图标纹理路径 |
| `nFrame` | `number` | 图标帧编号 |
| `szLayer` | `string` | 层名称 |
| `fnMouseEnter` | `function` | 鼠标进入回调 |
| `fnMouseLeave` | `function` | 鼠标离开回调 |

---

## 示例：完整菜单系统

```lua
-- 注册玩家菜单
Addon_RegisterPlayerMenu("DKP_Manager", function(dwID, szName)
    local player = GetPlayer(dwID)
    if not player then
        return nil
    end

    return {
        {
            szOption = "DKP 管理",
            {
                {
                    szOption = "增加 DKP",
                    fnAction = function()
                        AddPlayerDKP(szName, 10)
                    end,
                },
                {
                    szOption = "扣除 DKP",
                    fnAction = function()
                        AddPlayerDKP(szName, -10)
                    end,
                },
                { bDevide = true },
                {
                    szOption = "查看历史",
                    fnAction = function()
                        ShowDKPHistory(szName)
                    end,
                },
            },
        },
    }
end)

-- 注册设置面板
Addon_RegisterPanel(
    "DKP_Manager",
    "DKP 管理器",
    "管理公会 DKP 分数",
    nil,
    function()
        Wnd.OpenWindow("Interface/DKP/DKPPanel.ini", "DKPPanel")
    end
)
```

---

## 相关链接

- [全局函数](./Global.zh-CN.md) - 全局 UI 函数
