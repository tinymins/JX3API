English | [中文](./Represent.zh-CN.md)

# Represent Functions (SO3UI)

Character and NPC resource representation functions provided by SO3UI module.

Source: `Source/Client/SO3UI/krepresentscripttable.cpp`

---

## Player Resource Functions

### Player_GetAnimationResource {#Player_GetAnimationResource}

```lua
szResource = Player_GetAnimationResource(dwRoleType, dwMountType)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwRoleType | `number` | Player role type ID |
| dwMountType | `number` | Mount type ID (0 for no mount) |

**Returns:** `string` - Animation resource path

Get the animation resource path for a player character.

---

### Player_GetEquipResource {#Player_GetEquipResource}

```lua
szResource = Player_GetEquipResource(dwRoleType, nRepresentIndex, dwRepresentID)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwRoleType | `number` | Player role type ID |
| nRepresentIndex | `number` | Representation index (equipment slot) |
| dwRepresentID | `number` | Representation ID |

**Returns:** `string` - Equipment resource path

Get the equipment resource path for a player character.

---

### Player_GetRidesAnimationResource {#Player_GetRidesAnimationResource}

```lua
szResource = Player_GetRidesAnimationResource(dwMountType, dwRoleType)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwMountType | `number` | Mount type ID |
| dwRoleType | `number` | Player role type ID |

**Returns:** `string` - Mount animation resource path

Get the animation resource path for a mount.

---

### Player_GetRidesEquipResource {#Player_GetRidesEquipResource}

```lua
szResource = Player_GetRidesEquipResource(dwMountType, nRepresentIndex, dwRepresentID)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwMountType | `number` | Mount type ID |
| nRepresentIndex | `number` | Representation index |
| dwRepresentID | `number` | Representation ID |

**Returns:** `string` - Mount equipment resource path

Get the equipment resource path for a mount.

---

## NPC Resource Functions

### NPC_GetProtrait {#NPC_GetProtrait}

```lua
szImagePath, nFrame = NPC_GetProtrait(dwTemplateID)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwTemplateID | `number` | NPC template ID |

**Returns:** `string, number` - Portrait image path and frame index

Get the portrait image for an NPC.

---

### NPC_GetHeadImageFile {#NPC_GetHeadImageFile}

```lua
szImagePath = NPC_GetHeadImageFile(dwTemplateID)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwTemplateID | `number` | NPC template ID |

**Returns:** `string` - Head image file path

Get the head image file path for an NPC.

---

### NPC_GetAnimationResource {#NPC_GetAnimationResource}

```lua
szResource = NPC_GetAnimationResource(dwTemplateID)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwTemplateID | `number` | NPC template ID |

**Returns:** `string` - Animation resource path

Get the animation resource path for an NPC.

---

### NPC_GetEquipResource {#NPC_GetEquipResource}

```lua
szResource = NPC_GetEquipResource(dwTemplateID, nRepresentIndex)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwTemplateID | `number` | NPC template ID |
| nRepresentIndex | `number` | Representation index |

**Returns:** `string` - Equipment resource path

Get the equipment resource path for an NPC.

---

## Character Functions

### Character_Create {#Character_Create}

```lua
hCharacter = Character_Create(szSceneName, szName)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szSceneName | `string` | Scene name |
| szName | `string` | Character name |

**Returns:** `userdata` - Character handle

Create a character object for rendering.

---

### Character_Delete {#Character_Delete}

```lua
Character_Delete(hCharacter)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| hCharacter | `userdata` | Character handle |

**Returns:** `void`

Delete a character object.

---

### Character_Load {#Character_Load}

```lua
bSuccess = Character_Load(hCharacter, szAnimationSet, szEquip, nSocketIndex)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| hCharacter | `userdata` | Character handle |
| szAnimationSet | `string` | Animation set path |
| szEquip | `string` | Equipment resource path |
| nSocketIndex | `number` | Socket index |

**Returns:** `boolean` - Whether loading succeeded

Load character resources.

---

### Character_UnloadPart {#Character_UnloadPart}

```lua
Character_UnloadPart(hCharacter, nSocketIndex)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| hCharacter | `userdata` | Character handle |
| nSocketIndex | `number` | Socket index |

**Returns:** `void`

Unload a specific part of the character.

---

### Character_ExchangePart {#Character_ExchangePart}

```lua
Character_ExchangePart(hCharacter, nSocketIndex, szEquip)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| hCharacter | `userdata` | Character handle |
| nSocketIndex | `number` | Socket index |
| szEquip | `string` | Equipment resource path |

**Returns:** `void`

Exchange a character part.

---

### Character_PlayAnimation {#Character_PlayAnimation}

```lua
Character_PlayAnimation(hCharacter, szAnimation, bLoop, fSpeed)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| hCharacter | `userdata` | Character handle |
| szAnimation | `string` | Animation name |
| bLoop | `boolean` | Whether to loop |
| fSpeed | `number` | Playback speed |

**Returns:** `void`

Play a character animation.

---

### Character_SetPosition {#Character_SetPosition}

```lua
Character_SetPosition(hCharacter, fX, fY, fZ)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| hCharacter | `userdata` | Character handle |
| fX | `number` | X position |
| fY | `number` | Y position |
| fZ | `number` | Z position |

**Returns:** `void`

Set character position.

---

### Character_SetDirection {#Character_SetDirection}

```lua
Character_SetDirection(hCharacter, fYaw, fPitch, fRoll)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| hCharacter | `userdata` | Character handle |
| fYaw | `number` | Yaw angle |
| fPitch | `number` | Pitch angle |
| fRoll | `number` | Roll angle |

**Returns:** `void`

Set character direction/rotation.

---

### Character_SetScale {#Character_SetScale}

```lua
Character_SetScale(hCharacter, fScale)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| hCharacter | `userdata` | Character handle |
| fScale | `number` | Scale factor |

**Returns:** `void`

Set character scale.
