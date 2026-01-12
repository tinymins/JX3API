# Hook & Filter Functions

Message filtering, hooking, and interception functions.

---

## Talk Filter

### RegisterTalkFilter {#RegisterTalkFilter}

```lua
RegisterTalkFilter(fnFilter)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| fnFilter | `function` | Filter function `function(szMsg, dwTalkerID, nChannel) return bBlock, szNewMsg` |

**Returns:** `void`

Register a talk message filter. The filter function can modify or block chat messages.

**Filter function parameters:**
- `szMsg` - Original message text
- `dwTalkerID` - ID of the speaker
- `nChannel` - Chat channel

**Filter function returns:**
- `bBlock` - true to block the message
- `szNewMsg` - Modified message (optional)

---

### UnRegisterTalkFilter {#UnRegisterTalkFilter}

```lua
UnRegisterTalkFilter(fnFilter)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| fnFilter | `function` | Previously registered filter function |

**Returns:** `void`

Unregister a talk message filter.

---

## Message Filter

### RegisterMsgFilter {#RegisterMsgFilter}

```lua
RegisterMsgFilter(fnFilter)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| fnFilter | `function` | Message filter function |

**Returns:** `void`

Register a system message filter.

---

### UnRegisterMsgFilter {#UnRegisterMsgFilter}

```lua
UnRegisterMsgFilter(fnFilter)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| fnFilter | `function` | Previously registered filter function |

**Returns:** `void`

Unregister a system message filter.

---

## Message Hook

### RegisterMsgHook {#RegisterMsgHook}

```lua
RegisterMsgHook(fnHook)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| fnHook | `function` | Message hook function |

**Returns:** `void`

Register a message hook to intercept messages.

---

### UnRegisterMsgHook {#UnRegisterMsgHook}

```lua
UnRegisterMsgHook(fnHook)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| fnHook | `function` | Previously registered hook function |

**Returns:** `void`

Unregister a message hook.

---

## Table Hook

### HookTableFunc {#HookTableFunc}

```lua
fnOriginal = HookTableFunc(tTable, szFuncName, fnHook)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| tTable | `table` | Table containing the function |
| szFuncName | `string` | Name of the function to hook |
| fnHook | `function` | Hook function |

**Returns:** `function` - Original function

Hook a function in a table. The hook function will be called instead of the original.

**Example:**
```lua
local fnOriginal = HookTableFunc(SomeTable, "SomeFunc", function(...)
    -- Pre-processing
    local result = fnOriginal(...)
    -- Post-processing
    return result
end)
```

---

### UnhookTableFunc {#UnhookTableFunc}

```lua
UnhookTableFunc(tTable, szFuncName, fnHook)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| tTable | `table` | Table containing the function |
| szFuncName | `string` | Name of the hooked function |
| fnHook | `function` | Hook function to remove |

**Returns:** `void`

Remove a hook from a table function.

---

## Text Filter

### TextFilterCheck {#TextFilterCheck}

```lua
bBlocked = TextFilterCheck(szText)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szText | `string` | Text to check |

**Returns:** `boolean` - true if text contains blocked words

Check if text contains blocked/sensitive words.

---

### TextFilterReplace {#TextFilterReplace}

```lua
szFiltered = TextFilterReplace(szText)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szText | `string` | Text to filter |

**Returns:** `string` - Text with blocked words replaced

Replace blocked/sensitive words in text with asterisks or placeholders.
