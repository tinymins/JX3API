# Player Resource Functions

Player visual resource and animation functions.

---

## Animation Resources

### Player_GetAnimationResource {#Player_GetAnimationResource}

```lua
szPath = Player_GetAnimationResource(dwPlayerID, szAnimationName)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwPlayerID | `number` | Player ID |
| szAnimationName | `string` | Animation name |

**Returns:** `string` - Animation resource path

Get the animation resource path for a player.

---

### Player_GetRidesAnimationResource {#Player_GetRidesAnimationResource}

```lua
szPath = Player_GetRidesAnimationResource(dwPlayerID, szAnimationName)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwPlayerID | `number` | Player ID |
| szAnimationName | `string` | Animation name |

**Returns:** `string` - Mount animation resource path

Get the mount animation resource path for a player.

---

## Equipment Resources

### Player_GetEquipResource {#Player_GetEquipResource}

```lua
szPath = Player_GetEquipResource(dwPlayerID, nEquipSlot)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwPlayerID | `number` | Player ID |
| nEquipSlot | `number` | Equipment slot index |

**Returns:** `string` - Equipment resource path

Get the equipment resource path for a player.

---

### Player_GetRidesEquipResource {#Player_GetRidesEquipResource}

```lua
szPath = Player_GetRidesEquipResource(dwPlayerID, nEquipSlot)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwPlayerID | `number` | Player ID |
| nEquipSlot | `number` | Equipment slot index |

**Returns:** `string` - Mount equipment resource path

Get the mount equipment resource path for a player.

---

## NPC Resources

### NPC_GetProtrait {#NPC_GetProtrait}

```lua
szPath = NPC_GetProtrait(dwNpcTemplateID)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwNpcTemplateID | `number` | NPC template ID |

**Returns:** `string` - Portrait image path

Get the portrait image path for an NPC.

---

### NPC_GetHeadImageFile {#NPC_GetHeadImageFile}

```lua
szPath = NPC_GetHeadImageFile(dwNpcTemplateID)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwNpcTemplateID | `number` | NPC template ID |

**Returns:** `string` - Head image file path

Get the head image file path for an NPC.

---

## Player Energy UI

### PlayerEnergyUI_Update {#PlayerEnergyUI_Update}

```lua
PlayerEnergyUI_Update()
```

**Returns:** `void`

Update the player energy UI display.

---

### PlayerEnergyUI_GetUpdateFunc {#PlayerEnergyUI_GetUpdateFunc}

```lua
fnUpdate = PlayerEnergyUI_GetUpdateFunc()
```

**Returns:** `function` - Update function

Get the player energy UI update function.

---

### PlayerEnergyUI_ChangeStyle {#PlayerEnergyUI_ChangeStyle}

```lua
PlayerEnergyUI_ChangeStyle(nStyle)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nStyle | `number` | Style ID |

**Returns:** `void`

Change the player energy UI style.

---

## Camera

### Camera_GetRTParams {#Camera_GetRTParams}

```lua
tParams = Camera_GetRTParams()
```

**Returns:** `table` - Camera real-time parameters

Get camera real-time parameters.

---

### Camera_GetParams {#Camera_GetParams}

```lua
tParams = Camera_GetParams()
```

**Returns:** `table` - Camera parameters

Get camera parameters.
