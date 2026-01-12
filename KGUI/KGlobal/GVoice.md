# GVoice (Team Voice)

Team voice chat system functions using GVoice SDK.

---

## GVoiceBase_IsOpen {#GVoiceBase_IsOpen}

Check if GVoice is enabled and open.

### Syntax

```lua
local bOpen = GVoiceBase_IsOpen()
```

### Returns

| Type | Description |
|------|-------------|
| `boolean` | `true` if GVoice is open and available |

### Example

```lua
if GVoiceBase_IsOpen() then
    Output("Voice chat is available")
end
```

---

## GVoiceBase_GetMicState {#GVoiceBase_GetMicState}

Get current microphone state.

### Syntax

```lua
local nState = GVoiceBase_GetMicState()
```

### Returns

| Type | Description |
|------|-------------|
| `number` | Microphone state (0=off, 1=on, 2=muted) |

### Example

```lua
local nState = GVoiceBase_GetMicState()
if nState == 1 then
    Output("Microphone is on")
end
```

---

## GVoiceBase_SwitchMicState {#GVoiceBase_SwitchMicState}

Toggle or set microphone state.

### Syntax

```lua
GVoiceBase_SwitchMicState(bEnable)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `bEnable` | `boolean` | (Optional) Enable or disable mic. If omitted, toggles current state. |

### Example

```lua
-- Toggle mic
GVoiceBase_SwitchMicState()

-- Explicitly enable
GVoiceBase_SwitchMicState(true)

-- Explicitly disable
GVoiceBase_SwitchMicState(false)
```

---

## GVoiceBase_CheckMicState {#GVoiceBase_CheckMicState}

Check and validate microphone state (for troubleshooting).

### Syntax

```lua
local bValid = GVoiceBase_CheckMicState()
```

### Returns

| Type | Description |
|------|-------------|
| `boolean` | `true` if microphone is working properly |

---

## GVoiceBase_GetSpeakerState {#GVoiceBase_GetSpeakerState}

Get current speaker/output state.

### Syntax

```lua
local nState = GVoiceBase_GetSpeakerState()
```

### Returns

| Type | Description |
|------|-------------|
| `number` | Speaker state (0=off, 1=on) |

---

## GVoiceBase_SwitchSpeakerState {#GVoiceBase_SwitchSpeakerState}

Toggle or set speaker state.

### Syntax

```lua
GVoiceBase_SwitchSpeakerState(bEnable)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `bEnable` | `boolean` | (Optional) Enable or disable speaker |

### Example

```lua
-- Mute voice chat output
GVoiceBase_SwitchSpeakerState(false)
```

---

## GVoiceBase_GetSaying {#GVoiceBase_GetSaying}

Get currently speaking player.

### Syntax

```lua
local dwPlayerID = GVoiceBase_GetSaying()
```

### Returns

| Type | Description |
|------|-------------|
| `number` | Player ID of currently speaking player, or 0 if none |

### Example

```lua
local dwSpeaking = GVoiceBase_GetSaying()
if dwSpeaking > 0 then
    local player = GetPlayer(dwSpeaking)
    if player then
        Output(player.szName .. " is speaking")
    end
end
```

---

## GVoiceBase_IsMemberSaying {#GVoiceBase_IsMemberSaying}

Check if a specific member is currently speaking.

### Syntax

```lua
local bSaying = GVoiceBase_IsMemberSaying(dwPlayerID)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `dwPlayerID` | `number` | Player ID to check |

### Returns

| Type | Description |
|------|-------------|
| `boolean` | `true` if the player is speaking |

### Example

```lua
if GVoiceBase_IsMemberSaying(dwTeammateID) then
    -- Show speaking indicator
end
```

---

## GVoiceBase_IsMemberForbid {#GVoiceBase_IsMemberForbid}

Check if a member is forbidden/muted in voice chat.

### Syntax

```lua
local bForbid = GVoiceBase_IsMemberForbid(dwPlayerID)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `dwPlayerID` | `number` | Player ID to check |

### Returns

| Type | Description |
|------|-------------|
| `boolean` | `true` if the player is muted |

---

## GVoiceBase_ForbidMember {#GVoiceBase_ForbidMember}

Mute or unmute a specific member in voice chat.

### Syntax

```lua
GVoiceBase_ForbidMember(dwPlayerID, bForbid)
```

### Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `dwPlayerID` | `number` | Player ID to mute/unmute |
| `bForbid` | `boolean` | `true` to mute, `false` to unmute |

### Example

```lua
-- Mute a player
GVoiceBase_ForbidMember(dwPlayerID, true)

-- Unmute a player
GVoiceBase_ForbidMember(dwPlayerID, false)
```

---

## See Also

- [KTeamClient](../../SO3World/KClient/KTeamClient.md) - Team client functions
- [Raid](./Raid.md) - Raid management functions
