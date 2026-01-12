# Storage Functions

Online storage and custom data persistence functions.

---

## Frame Anchor Storage

### GetOnlineFrameAnchor {#GetOnlineFrameAnchor}

```lua
tData = GetOnlineFrameAnchor(szKey)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szKey | `string` | Storage key |

**Returns:** `any` - Stored data

Get online frame anchor data. Used for storing UI frame positions across sessions.

---

### SetOnlineFrameAnchor {#SetOnlineFrameAnchor}

```lua
SetOnlineFrameAnchor(szKey, data)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szKey | `string` | Storage key |
| data | `any` | Data to store |

**Returns:** `void`

Set online frame anchor data.

---

## Addon Custom Data

### GetAddonCustomData {#GetAddonCustomData}

```lua
tData = GetAddonCustomData(szSubKey)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szSubKey | `string` | Optional: Sub-key for data |

**Returns:** `any` - Stored custom data

Get addon-specific custom data. The storage key is automatically namespaced by addon package name.

---

### SetAddonCustomData {#SetAddonCustomData}

```lua
SetAddonCustomData(szSubKey, data)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szSubKey | `string` | Optional: Sub-key for data |
| data | `any` | Data to store |

**Returns:** `void`

Set addon-specific custom data. Data is namespaced by addon package name.

---

## Online Addon Data

### GetOnlineAddonCustomData {#GetOnlineAddonCustomData}

```lua
tData = GetOnlineAddonCustomData(szSubKey)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szSubKey | `string` | Optional: Sub-key for data |

**Returns:** `any` - Stored online data

Get addon-specific online custom data (synced to server).

---

### SetOnlineAddonCustomData {#SetOnlineAddonCustomData}

```lua
SetOnlineAddonCustomData(szSubKey, data)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szSubKey | `string` | Optional: Sub-key for data |
| data | `any` | Data to store |

**Returns:** `void`

Set addon-specific online custom data (synced to server).

---

## Navigator

### Navigator_SetID {#Navigator_SetID}

```lua
Navigator_SetID(nID)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nID | `number` | Navigator ID |

**Returns:** `void`

Set navigator target by ID.

---

### Navigator_SetPoint {#Navigator_SetPoint}

```lua
Navigator_SetPoint(nMapID, nX, nY)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nMapID | `number` | Map ID |
| nX | `number` | X coordinate |
| nY | `number` | Y coordinate |

**Returns:** `void`

Set navigator target point.

---

### Navigator_Remove {#Navigator_Remove}

```lua
Navigator_Remove()
```

**Returns:** `void`

Remove current navigator target.
