# Menu Registration

Functions for registering and managing context menus in the game.

---

## Addon_RegisterPlayerMenu {#Addon_RegisterPlayerMenu}

Register a custom menu callback for player context menus.

### Syntax

```lua
Addon_RegisterPlayerMenu(szAddonName, fnCallback)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `szAddonName` | `string` | Unique addon identifier |
| `fnCallback` | `function` | Callback function that returns menu items |

### Callback Function

```lua
function fnCallback(dwID, szName)
    -- dwID: Player's dwID
    -- szName: Player's name
    -- Return: Table of menu items or nil
end
```

### Example

```lua
Addon_RegisterPlayerMenu("MyAddon", function(dwID, szName)
    return {
        {
            szOption = "Send Message",
            fnAction = function()
                Output("Hello " .. szName)
            end,
        },
        {
            szOption = "View Info",
            fnAction = function()
                ViewPlayerInfo(dwID)
            end,
        },
    }
end)
```

---

## Addon_RegisterTargetMenu {#Addon_RegisterTargetMenu}

Register a custom menu callback for target context menus.

### Syntax

```lua
Addon_RegisterTargetMenu(szAddonName, fnCallback)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `szAddonName` | `string` | Unique addon identifier |
| `fnCallback` | `function` | Callback function that returns menu items |

### Example

```lua
Addon_RegisterTargetMenu("MyAddon", function(dwID)
    local target = GetNpc(dwID) or GetPlayer(dwID)
    if not target then
        return nil
    end
    return {
        {
            szOption = "Mark Target",
            fnAction = function()
                SetTeamMark(1, dwID)
            end,
        },
    }
end)
```

---

## Addon_RegisterTraceButtonMenu {#Addon_RegisterTraceButtonMenu}

Register a custom menu callback for trace button context menus.

### Syntax

```lua
Addon_RegisterTraceButtonMenu(szAddonName, fnCallback)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `szAddonName` | `string` | Unique addon identifier |
| `fnCallback` | `function` | Callback function that returns menu items |

---

## Addon_RegisterPanel {#Addon_RegisterPanel}

Register an addon panel in the system settings/addon management interface.

### Syntax

```lua
Addon_RegisterPanel(szAddonName, szDisplayName, szDescription, szIcon, fnOpenPanel)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `szAddonName` | `string` | Unique addon identifier |
| `szDisplayName` | `string` | Display name in panel list |
| `szDescription` | `string` | Addon description |
| `szIcon` | `string` | Icon path (optional) |
| `fnOpenPanel` | `function` | Callback when panel is opened |

### Example

```lua
Addon_RegisterPanel(
    "MyAddon",
    "My Addon Settings",
    "Configure my awesome addon",
    "ui/Image/icon.uitex",
    function()
        OpenMyAddonPanel()
    end
)
```

---

## InsertPlayerMenu {#InsertPlayerMenu}

Insert menu items directly into the player context menu.

### Syntax

```lua
InsertPlayerMenu(tMenu)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `tMenu` | `table` | Array of menu item tables |

### Menu Item Structure

| Field | Type | Description |
|-------|------|-------------|
| `szOption` | `string` | Menu item text |
| `fnAction` | `function` | Click callback |
| `bDisable` | `boolean` | Disabled state (optional) |
| `bCheck` | `boolean` | Show checkmark (optional) |
| `fnDisable` | `function` | Function to determine disabled state (optional) |

---

## InsertTargetMenu {#InsertTargetMenu}

Insert menu items directly into the target context menu.

### Syntax

```lua
InsertTargetMenu(tMenu)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `tMenu` | `table` | Array of menu item tables |

---

## InsertTeammateMenu {#InsertTeammateMenu}

Insert menu items into teammate context menus.

### Syntax

```lua
InsertTeammateMenu(tMenu)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `tMenu` | `table` | Array of menu item tables |

---

## PopupMenu {#PopupMenu}

Display a popup menu at the current cursor position.

### Syntax

```lua
PopupMenu(tMenu)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `tMenu` | `table` | Menu structure table |

### Example

```lua
PopupMenu({
    { szOption = "Option 1", fnAction = function() Output("1") end },
    { szOption = "Option 2", fnAction = function() Output("2") end },
    { bDevide = true },  -- Separator
    {
        szOption = "Submenu",
        {
            { szOption = "Sub Option 1", fnAction = function() end },
            { szOption = "Sub Option 2", fnAction = function() end },
        }
    },
})
```

---

## Menu Item Properties

### Basic Properties

| Property | Type | Description |
|----------|------|-------------|
| `szOption` | `string` | Display text |
| `fnAction` | `function` | Click callback |
| `bDisable` | `boolean` | Disabled state |
| `bCheck` | `boolean` | Show checkmark |
| `bDevide` | `boolean` | Is separator line |
| `rgb` | `table` | Text color {r, g, b} |

### Advanced Properties

| Property | Type | Description |
|----------|------|-------------|
| `szIcon` | `string` | Icon texture path |
| `nFrame` | `number` | Icon frame number |
| `szLayer` | `string` | Layer name |
| `fnMouseEnter` | `function` | Mouse enter callback |
| `fnMouseLeave` | `function` | Mouse leave callback |

---

## Example: Complete Menu System

```lua
-- Register player menu
Addon_RegisterPlayerMenu("DKP_Manager", function(dwID, szName)
    local player = GetPlayer(dwID)
    if not player then
        return nil
    end

    return {
        {
            szOption = "DKP Manager",
            {
                {
                    szOption = "Add DKP",
                    fnAction = function()
                        AddPlayerDKP(szName, 10)
                    end,
                },
                {
                    szOption = "Remove DKP",
                    fnAction = function()
                        AddPlayerDKP(szName, -10)
                    end,
                },
                { bDevide = true },
                {
                    szOption = "View History",
                    fnAction = function()
                        ShowDKPHistory(szName)
                    end,
                },
            },
        },
    }
end)

-- Register settings panel
Addon_RegisterPanel(
    "DKP_Manager",
    "DKP Manager",
    "Manage guild DKP points",
    nil,
    function()
        Wnd.OpenWindow("Interface/DKP/DKPPanel.ini", "DKPPanel")
    end
)
```

---

## See Also

- [Global Functions](./Global.md) - Global UI functions
