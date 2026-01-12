# 位运算

用于二进制操作的位运算函数。

---

## BitwiseAnd {#BitwiseAnd}

执行按位与运算。

### 语法

```lua
local nResult = BitwiseAnd(nValue1, nValue2)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `nValue1` | `number` | 第一个操作数 |
| `nValue2` | `number` | 第二个操作数 |

### 返回值

| 类型 | 说明 |
|------|------|
| `number` | 按位与运算的结果 |

### 示例

```lua
local result = BitwiseAnd(0xFF, 0x0F)  -- 结果：0x0F (15)
local flags = BitwiseAnd(nFlags, FLAG_MASK)  -- 检查标志位
```

---

## BitwiseOr {#BitwiseOr}

执行按位或运算。

### 语法

```lua
local nResult = BitwiseOr(nValue1, nValue2)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `nValue1` | `number` | 第一个操作数 |
| `nValue2` | `number` | 第二个操作数 |

### 返回值

| 类型 | 说明 |
|------|------|
| `number` | 按位或运算的结果 |

### 示例

```lua
local result = BitwiseOr(0xF0, 0x0F)  -- 结果：0xFF (255)
local flags = BitwiseOr(nFlags, NEW_FLAG)  -- 添加标志位
```

---

## BitwiseXor {#BitwiseXor}

执行按位异或运算。

### 语法

```lua
local nResult = BitwiseXor(nValue1, nValue2)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `nValue1` | `number` | 第一个操作数 |
| `nValue2` | `number` | 第二个操作数 |

### 返回值

| 类型 | 说明 |
|------|------|
| `number` | 按位异或运算的结果 |

### 示例

```lua
local result = BitwiseXor(0xFF, 0x0F)  -- 结果：0xF0 (240)
local flags = BitwiseXor(nFlags, TOGGLE_FLAG)  -- 切换标志位
```

---

## GetNumberBit {#GetNumberBit}

获取数值中指定位的值。

### 语法

```lua
local nBit = GetNumberBit(nValue, nBitIndex)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `nValue` | `number` | 要提取位的数值 |
| `nBitIndex` | `number` | 位索引（从0开始，从右往左） |

### 返回值

| 类型 | 说明 |
|------|------|
| `number` | 0 或 1（位的值） |

### 示例

```lua
local value = 0b10101010  -- 十进制 170
local bit0 = GetNumberBit(value, 0)  -- 0
local bit1 = GetNumberBit(value, 1)  -- 1
local bit7 = GetNumberBit(value, 7)  -- 1
```

---

## SetNumberBit {#SetNumberBit}

设置数值中指定位的值。

### 语法

```lua
local nResult = SetNumberBit(nValue, nBitIndex, nBitValue)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `nValue` | `number` | 原始数值 |
| `nBitIndex` | `number` | 位索引（从0开始，从右往左） |
| `nBitValue` | `number` | 要设置的位值（0 或 1） |

### 返回值

| 类型 | 说明 |
|------|------|
| `number` | 修改后的数值 |

### 示例

```lua
local value = 0
value = SetNumberBit(value, 0, 1)  -- 设置第0位：0b00000001 (1)
value = SetNumberBit(value, 3, 1)  -- 设置第3位：0b00001001 (9)
value = SetNumberBit(value, 0, 0)  -- 清除第0位：0b00001000 (8)
```

---

## BigIntAdd {#BigIntAdd}

大整数加法（字符串形式），用于超出 Lua 精度范围的数值运算。

### 语法

```lua
local szResult = BigIntAdd(szNum1, szNum2)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `szNum1` | `string` | 第一个数字（字符串形式） |
| `szNum2` | `string` | 第二个数字（字符串形式） |

### 返回值

| 类型 | 说明 |
|------|------|
| `string` | 和（字符串形式） |

### 示例

```lua
local sum = BigIntAdd("99999999999999999", "1")
-- 结果："100000000000000000"
```

---

## BigIntSub {#BigIntSub}

大整数减法（字符串形式）。

### 语法

```lua
local szResult = BigIntSub(szNum1, szNum2)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `szNum1` | `string` | 第一个数字（字符串形式） |
| `szNum2` | `string` | 第二个数字（字符串形式） |

### 返回值

| 类型 | 说明 |
|------|------|
| `string` | 差（字符串形式） |

### 示例

```lua
local diff = BigIntSub("100000000000000000", "1")
-- 结果："99999999999999999"
```

---

## 使用场景

### 标志位操作

```lua
-- 定义标志位
local FLAG_VISIBLE = 1      -- 第0位
local FLAG_ENABLED = 2      -- 第1位
local FLAG_ACTIVE = 4       -- 第2位

-- 检查标志位是否设置
local function HasFlag(nFlags, nFlag)
    return BitwiseAnd(nFlags, nFlag) ~= 0
end

-- 添加标志位
local function AddFlag(nFlags, nFlag)
    return BitwiseOr(nFlags, nFlag)
end

-- 移除标志位
local function RemoveFlag(nFlags, nFlag)
    return BitwiseAnd(nFlags, BitwiseXor(0xFFFFFFFF, nFlag))
end

-- 使用示例
local flags = 0
flags = AddFlag(flags, FLAG_VISIBLE)
flags = AddFlag(flags, FLAG_ENABLED)
if HasFlag(flags, FLAG_VISIBLE) then
    Output("可见标志已设置")
end
```

---

## 相关链接

- [Lua扩展函数](./LuaExt.zh-CN.md) - Lua 扩展函数
