# Bitwise Operations

Bitwise operation functions for binary manipulation.

---

## BitwiseAnd {#BitwiseAnd}

Perform bitwise AND operation.

### Syntax

```lua
local nResult = BitwiseAnd(nValue1, nValue2)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `nValue1` | `number` | First operand |
| `nValue2` | `number` | Second operand |

### Returns

| Type | Description |
|------|-------------|
| `number` | Result of bitwise AND |

### Example

```lua
local result = BitwiseAnd(0xFF, 0x0F)  -- Result: 0x0F (15)
local flags = BitwiseAnd(nFlags, FLAG_MASK)  -- Check flags
```

---

## BitwiseOr {#BitwiseOr}

Perform bitwise OR operation.

### Syntax

```lua
local nResult = BitwiseOr(nValue1, nValue2)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `nValue1` | `number` | First operand |
| `nValue2` | `number` | Second operand |

### Returns

| Type | Description |
|------|-------------|
| `number` | Result of bitwise OR |

### Example

```lua
local result = BitwiseOr(0xF0, 0x0F)  -- Result: 0xFF (255)
local flags = BitwiseOr(nFlags, NEW_FLAG)  -- Add flag
```

---

## BitwiseXor {#BitwiseXor}

Perform bitwise XOR (exclusive OR) operation.

### Syntax

```lua
local nResult = BitwiseXor(nValue1, nValue2)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `nValue1` | `number` | First operand |
| `nValue2` | `number` | Second operand |

### Returns

| Type | Description |
|------|-------------|
| `number` | Result of bitwise XOR |

### Example

```lua
local result = BitwiseXor(0xFF, 0x0F)  -- Result: 0xF0 (240)
local flags = BitwiseXor(nFlags, TOGGLE_FLAG)  -- Toggle flag
```

---

## GetNumberBit {#GetNumberBit}

Get the value of a specific bit from a number.

### Syntax

```lua
local nBit = GetNumberBit(nValue, nBitIndex)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `nValue` | `number` | The number to extract bit from |
| `nBitIndex` | `number` | Bit index (0-based, from right) |

### Returns

| Type | Description |
|------|-------------|
| `number` | 0 or 1 (the bit value) |

### Example

```lua
local value = 0b10101010  -- 170 in decimal
local bit0 = GetNumberBit(value, 0)  -- 0
local bit1 = GetNumberBit(value, 1)  -- 1
local bit7 = GetNumberBit(value, 7)  -- 1
```

---

## SetNumberBit {#SetNumberBit}

Set a specific bit in a number.

### Syntax

```lua
local nResult = SetNumberBit(nValue, nBitIndex, nBitValue)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `nValue` | `number` | The original number |
| `nBitIndex` | `number` | Bit index (0-based, from right) |
| `nBitValue` | `number` | Bit value to set (0 or 1) |

### Returns

| Type | Description |
|------|-------------|
| `number` | Modified number with bit set |

### Example

```lua
local value = 0
value = SetNumberBit(value, 0, 1)  -- Set bit 0: 0b00000001 (1)
value = SetNumberBit(value, 3, 1)  -- Set bit 3: 0b00001001 (9)
value = SetNumberBit(value, 0, 0)  -- Clear bit 0: 0b00001000 (8)
```

---

## BigIntAdd {#BigIntAdd}

Add two large integers (as strings) for numbers beyond Lua's precision.

### Syntax

```lua
local szResult = BigIntAdd(szNum1, szNum2)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `szNum1` | `string` | First number as string |
| `szNum2` | `string` | Second number as string |

### Returns

| Type | Description |
|------|-------------|
| `string` | Sum as string |

### Example

```lua
local sum = BigIntAdd("99999999999999999", "1")
-- Result: "100000000000000000"
```

---

## BigIntSub {#BigIntSub}

Subtract two large integers (as strings).

### Syntax

```lua
local szResult = BigIntSub(szNum1, szNum2)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `szNum1` | `string` | First number as string |
| `szNum2` | `string` | Second number as string |

### Returns

| Type | Description |
|------|-------------|
| `string` | Difference as string |

### Example

```lua
local diff = BigIntSub("100000000000000000", "1")
-- Result: "99999999999999999"
```

---

## Use Cases

### Flag Manipulation

```lua
-- Define flags
local FLAG_VISIBLE = 1      -- bit 0
local FLAG_ENABLED = 2      -- bit 1
local FLAG_ACTIVE = 4       -- bit 2

-- Check if flag is set
local function HasFlag(nFlags, nFlag)
    return BitwiseAnd(nFlags, nFlag) ~= 0
end

-- Add flag
local function AddFlag(nFlags, nFlag)
    return BitwiseOr(nFlags, nFlag)
end

-- Remove flag
local function RemoveFlag(nFlags, nFlag)
    return BitwiseAnd(nFlags, BitwiseXor(0xFFFFFFFF, nFlag))
end

-- Example usage
local flags = 0
flags = AddFlag(flags, FLAG_VISIBLE)
flags = AddFlag(flags, FLAG_ENABLED)
if HasFlag(flags, FLAG_VISIBLE) then
    Output("Visible flag is set")
end
```

---

## See Also

- [LuaExt](./LuaExt.md) - Lua extension functions
