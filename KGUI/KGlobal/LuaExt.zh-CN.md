# Lua 扩展函数

游戏引擎提供的扩展 Lua 函数和工具。

---

## class {#class}

创建一个类，支持可选的继承。

### 语法

```lua
local MyClass = class(szClassName)
local MyClass = class(szClassName, BaseClass)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `szClassName` | `string` | 类名 |
| `BaseClass` | `table` | 要继承的基类（可选） |

### 返回值

| 类型 | 说明 |
|------|------|
| `table` | 新的类表 |

### 示例

```lua
-- 定义基类
local Animal = class("Animal")

function Animal:ctor(name)
    self.name = name
end

function Animal:Speak()
    Output(self.name .. " 发出声音")
end

-- 继承 Animal
local Dog = class("Dog", Animal)

function Dog:ctor(name, breed)
    Animal.ctor(self, name)
    self.breed = breed
end

function Dog:Speak()
    Output(self.name .. " 汪汪叫！")
end

-- 使用
local dog = Dog.new("小黄", "拉布拉多")
dog:Speak()  -- 输出："小黄 汪汪叫！"
```

---

## clone {#clone}

创建表的深拷贝。

### 语法

```lua
local tCopy = clone(tSource)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `tSource` | `table` | 要克隆的源表 |

### 返回值

| 类型 | 说明 |
|------|------|
| `table` | 源表的深拷贝 |

### 示例

```lua
local original = {
    name = "测试",
    data = { 1, 2, 3 },
    nested = { a = 1, b = 2 }
}

local copy = clone(original)
copy.data[1] = 999
copy.nested.a = 999

-- original 保持不变
Output(original.data[1])    -- 1
Output(original.nested.a)   -- 1
```

---

## var2str {#var2str}

将任意 Lua 变量转换为字符串表示。

### 语法

```lua
local szString = var2str(var)
local szString = var2str(var, szIndent)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `var` | `any` | 要转换的变量 |
| `szIndent` | `string` | 缩进字符串（可选） |

### 返回值

| 类型 | 说明 |
|------|------|
| `string` | 字符串表示 |

### 示例

```lua
local tData = {
    name = "玩家",
    level = 100,
    items = { "剑", "盾" },
}

local szStr = var2str(tData)
Output(szStr)
-- 输出：
-- {
--     ["name"] = "玩家",
--     ["level"] = 100,
--     ["items"] = {
--         [1] = "剑",
--         [2] = "盾",
--     },
-- }
```

---

## count_c {#count_c}

统计表中元素的数量（优化的 C 实现）。

### 语法

```lua
local nCount = count_c(tTable)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `tTable` | `table` | 要统计的表 |

### 返回值

| 类型 | 说明 |
|------|------|
| `number` | 元素数量 |

### 示例

```lua
local tData = { a = 1, b = 2, c = 3, [1] = "x", [2] = "y" }
local count = count_c(tData)
Output(count)  -- 5
```

---

## pairs_c {#pairs_c}

优化的 pairs 迭代器（C 实现）。

### 语法

```lua
for k, v in pairs_c(tTable) do
    -- ...
end
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `tTable` | `table` | 要迭代的表 |

### 示例

```lua
local tData = { a = 1, b = 2, c = 3 }
for key, value in pairs_c(tData) do
    Output(key .. " = " .. value)
end
```

---

## ipairs_c {#ipairs_c}

优化的 ipairs 迭代器（C 实现）。

### 语法

```lua
for i, v in ipairs_c(tArray) do
    -- ...
end
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `tArray` | `table` | 要迭代的数组 |

### 示例

```lua
local tArray = { "a", "b", "c" }
for index, value in ipairs_c(tArray) do
    Output(index .. ": " .. value)
end
```

---

## SetmetaReadonly {#SetmetaReadonly}

通过设置元表使表变为只读。

### 语法

```lua
SetmetaReadonly(tTable)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `tTable` | `table` | 要设为只读的表 |

### 示例

```lua
local CONFIG = {
    MAX_LEVEL = 100,
    MAX_GOLD = 99999999,
}
SetmetaReadonly(CONFIG)

-- 这将引发错误：
-- CONFIG.MAX_LEVEL = 200  -- 错误！
```

---

## tweenlite {#tweenlite}

动画缓动工具，用于平滑过渡。

### 语法

```lua
tweenlite.to(tTarget, nDuration, tParams)
tweenlite.from(tTarget, nDuration, tParams)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `tTarget` | `table` | 包含要动画属性的目标对象 |
| `nDuration` | `number` | 动画持续时间（秒） |
| `tParams` | `table` | 动画参数 |

### 参数表

| 字段 | 类型 | 说明 |
|------|------|------|
| `onComplete` | `function` | 动画完成时的回调 |
| `onUpdate` | `function` | 每次更新时的回调 |
| `ease` | `string` | 缓动函数名称 |

### 示例

```lua
local panel = { x = 0, y = 0, alpha = 255 }

-- 动画到新位置
tweenlite.to(panel, 0.5, {
    x = 100,
    y = 200,
    alpha = 128,
    ease = "easeOutQuad",
    onComplete = function()
        Output("动画完成！")
    end,
})
```

---

## spairs {#spairs}

排序的 pairs 迭代器。

### 语法

```lua
for k, v in spairs(tTable) do
    -- 键按字母顺序排序
end

for k, v in spairs(tTable, fnSort) do
    -- 使用自定义函数排序键
end
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `tTable` | `table` | 要迭代的表 |
| `fnSort` | `function` | 自定义排序函数（可选） |

### 示例

```lua
local tData = { z = 3, a = 1, m = 2 }

for k, v in spairs(tData) do
    Output(k .. " = " .. v)
end
-- 按顺序输出：a = 1, m = 2, z = 3

-- 自定义排序（倒序）
for k, v in spairs(tData, function(a, b) return a > b end) do
    Output(k .. " = " .. v)
end
-- 按顺序输出：z = 3, m = 2, a = 1
```

---

## wstring {#wstring}

宽字符串工具，用于处理多字节字符。

### 方法

| 方法 | 说明 |
|------|------|
| `wstring.len(szStr)` | 获取字符长度（非字节长度） |
| `wstring.sub(szStr, nStart, nEnd)` | 按字符位置截取子串 |

### 示例

```lua
local szText = "你好世界"
Output(string.len(szText))   -- 字节长度（因编码而异）
Output(wstring.len(szText))  -- 4（字符数）

local szSub = wstring.sub(szText, 1, 2)
Output(szSub)  -- "你好"
```

---

## StringToTable {#StringToTable}

将表的字符串表示解析回表。

### 语法

```lua
local tResult = StringToTable(szString)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `szString` | `string` | 表的字符串表示 |

### 返回值

| 类型 | 说明 |
|------|------|
| `table` | 解析后的表 |

### 示例

```lua
local szData = '{ name = "测试", value = 123 }'
local tData = StringToTable(szData)
Output(tData.name)   -- "测试"
Output(tData.value)  -- 123
```

---

## SafeCall {#SafeCall}

安全调用函数，带错误处理。

### 语法

```lua
local bSuccess, ... = SafeCall(fnFunction, ...)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `fnFunction` | `function` | 要调用的函数 |
| `...` | `any` | 传递的参数 |

### 返回值

| 类型 | 说明 |
|------|------|
| `boolean` | 调用是否成功 |
| `...` | 返回值或错误信息 |

### 示例

```lua
local function RiskyOperation(x)
    if x < 0 then
        error("不允许负数")
    end
    return x * 2
end

local ok, result = SafeCall(RiskyOperation, 10)
if ok then
    Output("结果：" .. result)  -- 结果：20
end

local ok2, err = SafeCall(RiskyOperation, -5)
if not ok2 then
    Output("错误：" .. err)
end
```

---

## 相关链接

- [位运算](./Bitwise.zh-CN.md) - 位运算函数
- [全局函数](./Global.zh-CN.md) - 全局工具函数

---

## 已禁用的函数

以下函数在源码中存在但已被注释，无法使用：

### ~~module~~ {#module}

⚠️ **已禁用** - Lua 5.1 的 `module` 函数已被禁用。建议使用 `return` 语句导出模块。

```lua
-- 已注释
-- module("MyModule", package.seeall)

-- 推荐的替代方式：
local M = {}
-- ... 模块代码 ...
return M
```
