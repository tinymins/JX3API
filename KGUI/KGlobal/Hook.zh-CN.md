# Hook 与过滤器函数

消息过滤、Hook 和拦截函数。

---

## 聊天过滤器

### RegisterTalkFilter {#RegisterTalkFilter}

```lua
RegisterTalkFilter(fnFilter)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| fnFilter | `function` | 过滤函数 `function(szMsg, dwTalkerID, nChannel) return bBlock, szNewMsg` |

**返回:** `void`

注册聊天消息过滤器。过滤函数可以修改或阻止聊天消息。

**过滤函数参数：**
- `szMsg` - 原始消息文本
- `dwTalkerID` - 说话者 ID
- `nChannel` - 聊天频道

**过滤函数返回：**
- `bBlock` - 返回 true 阻止消息
- `szNewMsg` - 修改后的消息（可选）

---

### UnRegisterTalkFilter {#UnRegisterTalkFilter}

```lua
UnRegisterTalkFilter(fnFilter)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| fnFilter | `function` | 之前注册的过滤函数 |

**返回:** `void`

注销聊天消息过滤器。

---

## 消息过滤器

### RegisterMsgFilter {#RegisterMsgFilter}

```lua
RegisterMsgFilter(fnFilter)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| fnFilter | `function` | 消息过滤函数 |

**返回:** `void`

注册系统消息过滤器。

---

### UnRegisterMsgFilter {#UnRegisterMsgFilter}

```lua
UnRegisterMsgFilter(fnFilter)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| fnFilter | `function` | 之前注册的过滤函数 |

**返回:** `void`

注销系统消息过滤器。

---

## 消息 Hook

### RegisterMsgHook {#RegisterMsgHook}

```lua
RegisterMsgHook(fnHook)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| fnHook | `function` | 消息 Hook 函数 |

**返回:** `void`

注册消息 Hook 以拦截消息。

---

### UnRegisterMsgHook {#UnRegisterMsgHook}

```lua
UnRegisterMsgHook(fnHook)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| fnHook | `function` | 之前注册的 Hook 函数 |

**返回:** `void`

注销消息 Hook。

---

## 表函数 Hook

### HookTableFunc {#HookTableFunc}

```lua
fnOriginal = HookTableFunc(tTable, szFuncName, fnHook)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| tTable | `table` | 包含函数的表 |
| szFuncName | `string` | 要 Hook 的函数名 |
| fnHook | `function` | Hook 函数 |

**返回:** `function` - 原始函数

Hook 表中的函数。Hook 函数将代替原始函数被调用。

**示例：**
```lua
local fnOriginal = HookTableFunc(SomeTable, "SomeFunc", function(...)
    -- 前处理
    local result = fnOriginal(...)
    -- 后处理
    return result
end)
```

---

### UnhookTableFunc {#UnhookTableFunc}

```lua
UnhookTableFunc(tTable, szFuncName, fnHook)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| tTable | `table` | 包含函数的表 |
| szFuncName | `string` | 被 Hook 的函数名 |
| fnHook | `function` | 要移除的 Hook 函数 |

**返回:** `void`

从表函数移除 Hook。

---

## 文本过滤

### TextFilterCheck {#TextFilterCheck}

```lua
bBlocked = TextFilterCheck(szText)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szText | `string` | 要检查的文本 |

**返回:** `boolean` - 如果包含屏蔽词返回 true

检查文本是否包含屏蔽/敏感词。

---

### TextFilterReplace {#TextFilterReplace}

```lua
szFiltered = TextFilterReplace(szText)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szText | `string` | 要过滤的文本 |

**返回:** `string` - 替换屏蔽词后的文本

将文本中的屏蔽/敏感词替换为星号或占位符。
