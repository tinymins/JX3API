# Lua Extensions

Extended Lua functions and utilities provided by the game engine.

---

## class {#class}

Create a class with optional inheritance.

### Syntax

```lua
local MyClass = class(szClassName)
local MyClass = class(szClassName, BaseClass)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `szClassName` | `string` | Class name |
| `BaseClass` | `table` | Base class to inherit from (optional) |

### Returns

| Type | Description |
|------|-------------|
| `table` | New class table |

### Example

```lua
-- Define base class
local Animal = class("Animal")

function Animal:ctor(name)
    self.name = name
end

function Animal:Speak()
    Output(self.name .. " makes a sound")
end

-- Inherit from Animal
local Dog = class("Dog", Animal)

function Dog:ctor(name, breed)
    Animal.ctor(self, name)
    self.breed = breed
end

function Dog:Speak()
    Output(self.name .. " barks!")
end

-- Usage
local dog = Dog.new("Buddy", "Labrador")
dog:Speak()  -- Output: "Buddy barks!"
```

---

## clone {#clone}

Create a deep copy of a table.

### Syntax

```lua
local tCopy = clone(tSource)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `tSource` | `table` | Source table to clone |

### Returns

| Type | Description |
|------|-------------|
| `table` | Deep copy of the source table |

### Example

```lua
local original = {
    name = "Test",
    data = { 1, 2, 3 },
    nested = { a = 1, b = 2 }
}

local copy = clone(original)
copy.data[1] = 999
copy.nested.a = 999

-- original remains unchanged
Output(original.data[1])    -- 1
Output(original.nested.a)   -- 1
```

---

## var2str {#var2str}

Convert any Lua variable to a string representation.

### Syntax

```lua
local szString = var2str(var)
local szString = var2str(var, szIndent)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `var` | `any` | Variable to convert |
| `szIndent` | `string` | Indentation string (optional) |

### Returns

| Type | Description |
|------|-------------|
| `string` | String representation |

### Example

```lua
local tData = {
    name = "Player",
    level = 100,
    items = { "sword", "shield" },
}

local szStr = var2str(tData)
Output(szStr)
-- Output:
-- {
--     ["name"] = "Player",
--     ["level"] = 100,
--     ["items"] = {
--         [1] = "sword",
--         [2] = "shield",
--     },
-- }
```

---

## count_c {#count_c}

Count the number of elements in a table (optimized C implementation).

### Syntax

```lua
local nCount = count_c(tTable)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `tTable` | `table` | Table to count |

### Returns

| Type | Description |
|------|-------------|
| `number` | Number of elements |

### Example

```lua
local tData = { a = 1, b = 2, c = 3, [1] = "x", [2] = "y" }
local count = count_c(tData)
Output(count)  -- 5
```

---

## pairs_c {#pairs_c}

Optimized pairs iterator (C implementation).

### Syntax

```lua
for k, v in pairs_c(tTable) do
    -- ...
end
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `tTable` | `table` | Table to iterate |

### Example

```lua
local tData = { a = 1, b = 2, c = 3 }
for key, value in pairs_c(tData) do
    Output(key .. " = " .. value)
end
```

---

## ipairs_c {#ipairs_c}

Optimized ipairs iterator (C implementation).

### Syntax

```lua
for i, v in ipairs_c(tArray) do
    -- ...
end
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `tArray` | `table` | Array to iterate |

### Example

```lua
local tArray = { "a", "b", "c" }
for index, value in ipairs_c(tArray) do
    Output(index .. ": " .. value)
end
```

---

## SetmetaReadonly {#SetmetaReadonly}

Make a table read-only by setting a metatable.

### Syntax

```lua
SetmetaReadonly(tTable)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `tTable` | `table` | Table to make read-only |

### Example

```lua
local CONFIG = {
    MAX_LEVEL = 100,
    MAX_GOLD = 99999999,
}
SetmetaReadonly(CONFIG)

-- This will raise an error:
-- CONFIG.MAX_LEVEL = 200  -- Error!
```

---

## tweenlite {#tweenlite}

Animation tweening utility for smooth transitions.

### Syntax

```lua
tweenlite.to(tTarget, nDuration, tParams)
tweenlite.from(tTarget, nDuration, tParams)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `tTarget` | `table` | Target object with properties to animate |
| `nDuration` | `number` | Animation duration in seconds |
| `tParams` | `table` | Animation parameters |

### Parameters Table

| Field | Type | Description |
|-------|------|-------------|
| `onComplete` | `function` | Callback when animation completes |
| `onUpdate` | `function` | Callback on each update |
| `ease` | `string` | Easing function name |

### Example

```lua
local panel = { x = 0, y = 0, alpha = 255 }

-- Animate to new position
tweenlite.to(panel, 0.5, {
    x = 100,
    y = 200,
    alpha = 128,
    ease = "easeOutQuad",
    onComplete = function()
        Output("Animation complete!")
    end,
})
```

---

## spairs {#spairs}

Sorted pairs iterator.

### Syntax

```lua
for k, v in spairs(tTable) do
    -- Keys are sorted alphabetically
end

for k, v in spairs(tTable, fnSort) do
    -- Keys sorted using custom function
end
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `tTable` | `table` | Table to iterate |
| `fnSort` | `function` | Custom sort function (optional) |

### Example

```lua
local tData = { z = 3, a = 1, m = 2 }

for k, v in spairs(tData) do
    Output(k .. " = " .. v)
end
-- Output in order: a = 1, m = 2, z = 3

-- Custom sort (reverse)
for k, v in spairs(tData, function(a, b) return a > b end) do
    Output(k .. " = " .. v)
end
-- Output in order: z = 3, m = 2, a = 1
```

---

## wstring {#wstring}

Wide string utilities for handling multi-byte characters.

### Methods

| Method | Description |
|--------|-------------|
| `wstring.len(szStr)` | Get length in characters (not bytes) |
| `wstring.sub(szStr, nStart, nEnd)` | Substring by character position |

### Example

```lua
local szText = "你好世界"
Output(string.len(szText))   -- Byte length (varies)
Output(wstring.len(szText))  -- 4 (character count)

local szSub = wstring.sub(szText, 1, 2)
Output(szSub)  -- "你好"
```

---

## StringToTable {#StringToTable}

Parse a string representation of a table back to a table.

### Syntax

```lua
local tResult = StringToTable(szString)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `szString` | `string` | String representation of table |

### Returns

| Type | Description |
|------|-------------|
| `table` | Parsed table |

### Example

```lua
local szData = '{ name = "Test", value = 123 }'
local tData = StringToTable(szData)
Output(tData.name)   -- "Test"
Output(tData.value)  -- 123
```

---

## SafeCall {#SafeCall}

Safely call a function with error handling.

### Syntax

```lua
local bSuccess, ... = SafeCall(fnFunction, ...)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `fnFunction` | `function` | Function to call |
| `...` | `any` | Arguments to pass |

### Returns

| Type | Description |
|------|-------------|
| `boolean` | Whether call succeeded |
| `...` | Return values or error message |

### Example

```lua
local function RiskyOperation(x)
    if x < 0 then
        error("Negative value not allowed")
    end
    return x * 2
end

local ok, result = SafeCall(RiskyOperation, 10)
if ok then
    Output("Result: " .. result)  -- Result: 20
end

local ok2, err = SafeCall(RiskyOperation, -5)
if not ok2 then
    Output("Error: " .. err)
end
```

---

## See Also

- [Bitwise Operations](./Bitwise.md) - Bitwise functions
- [Global Functions](./Global.md) - Global utility functions

---

## Disabled Functions

The following functions exist in source but are commented out and cannot be used:

### ~~module~~ {#module}

⚠️ **Disabled** - The Lua 5.1 `module` function has been disabled. Use `return` statement to export modules instead.

```lua
-- Commented out
-- module("MyModule", package.seeall)

-- Recommended alternative:
local M = {}
-- ... module code ...
return M
```
