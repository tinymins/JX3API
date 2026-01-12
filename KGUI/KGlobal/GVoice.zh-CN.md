# 团队语音（GVoice）

使用 GVoice SDK 的团队语音聊天系统函数。

---

## GVoiceBase_IsOpen {#GVoiceBase_IsOpen}

检查 GVoice 是否已启用并打开。

### 语法

```lua
local bOpen = GVoiceBase_IsOpen()
```

### 返回值

| 类型 | 说明 |
|------|------|
| `boolean` | 如果 GVoice 已打开并可用则返回 `true` |

### 示例

```lua
if GVoiceBase_IsOpen() then
    Output("语音聊天可用")
end
```

---

## GVoiceBase_GetMicState {#GVoiceBase_GetMicState}

获取当前麦克风状态。

### 语法

```lua
local nState = GVoiceBase_GetMicState()
```

### 返回值

| 类型 | 说明 |
|------|------|
| `number` | 麦克风状态（0=关闭, 1=开启, 2=静音） |

### 示例

```lua
local nState = GVoiceBase_GetMicState()
if nState == 1 then
    Output("麦克风已开启")
end
```

---

## GVoiceBase_SwitchMicState {#GVoiceBase_SwitchMicState}

切换或设置麦克风状态。

### 语法

```lua
GVoiceBase_SwitchMicState(bEnable)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `bEnable` | `boolean` | （可选）启用或禁用麦克风。如果省略，则切换当前状态。 |

### 示例

```lua
-- 切换麦克风
GVoiceBase_SwitchMicState()

-- 显式启用
GVoiceBase_SwitchMicState(true)

-- 显式禁用
GVoiceBase_SwitchMicState(false)
```

---

## GVoiceBase_CheckMicState {#GVoiceBase_CheckMicState}

检查并验证麦克风状态（用于故障排除）。

### 语法

```lua
local bValid = GVoiceBase_CheckMicState()
```

### 返回值

| 类型 | 说明 |
|------|------|
| `boolean` | 如果麦克风工作正常则返回 `true` |

---

## GVoiceBase_GetSpeakerState {#GVoiceBase_GetSpeakerState}

获取当前扬声器/输出状态。

### 语法

```lua
local nState = GVoiceBase_GetSpeakerState()
```

### 返回值

| 类型 | 说明 |
|------|------|
| `number` | 扬声器状态（0=关闭, 1=开启） |

---

## GVoiceBase_SwitchSpeakerState {#GVoiceBase_SwitchSpeakerState}

切换或设置扬声器状态。

### 语法

```lua
GVoiceBase_SwitchSpeakerState(bEnable)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `bEnable` | `boolean` | （可选）启用或禁用扬声器 |

### 示例

```lua
-- 静音语音聊天输出
GVoiceBase_SwitchSpeakerState(false)
```

---

## GVoiceBase_GetSaying {#GVoiceBase_GetSaying}

获取当前正在说话的玩家。

### 语法

```lua
local dwPlayerID = GVoiceBase_GetSaying()
```

### 返回值

| 类型 | 说明 |
|------|------|
| `number` | 正在说话的玩家 ID，如果没有则返回 0 |

### 示例

```lua
local dwSpeaking = GVoiceBase_GetSaying()
if dwSpeaking > 0 then
    local player = GetPlayer(dwSpeaking)
    if player then
        Output(player.szName .. " 正在说话")
    end
end
```

---

## GVoiceBase_IsMemberSaying {#GVoiceBase_IsMemberSaying}

检查特定成员是否正在说话。

### 语法

```lua
local bSaying = GVoiceBase_IsMemberSaying(dwPlayerID)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `dwPlayerID` | `number` | 要检查的玩家 ID |

### 返回值

| 类型 | 说明 |
|------|------|
| `boolean` | 如果该玩家正在说话则返回 `true` |

### 示例

```lua
if GVoiceBase_IsMemberSaying(dwTeammateID) then
    -- 显示说话指示器
end
```

---

## GVoiceBase_IsMemberForbid {#GVoiceBase_IsMemberForbid}

检查成员是否在语音聊天中被禁言/静音。

### 语法

```lua
local bForbid = GVoiceBase_IsMemberForbid(dwPlayerID)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `dwPlayerID` | `number` | 要检查的玩家 ID |

### 返回值

| 类型 | 说明 |
|------|------|
| `boolean` | 如果该玩家被静音则返回 `true` |

---

## GVoiceBase_ForbidMember {#GVoiceBase_ForbidMember}

在语音聊天中静音或取消静音特定成员。

### 语法

```lua
GVoiceBase_ForbidMember(dwPlayerID, bForbid)
```

### 参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `dwPlayerID` | `number` | 要静音/取消静音的玩家 ID |
| `bForbid` | `boolean` | `true` 静音，`false` 取消静音 |

### 示例

```lua
-- 静音某玩家
GVoiceBase_ForbidMember(dwPlayerID, true)

-- 取消静音某玩家
GVoiceBase_ForbidMember(dwPlayerID, false)
```

---

## 另见

- [KTeamClient](../../SO3World/KClient/KTeamClient.zh-CN.md) - 队伍客户端函数
- [Raid](./Raid.zh-CN.md) - 团队管理函数
