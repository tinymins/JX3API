[English](./Represent.md) | 中文

# 表现函数（SO3UI）

SO3UI 模块提供的角色和NPC资源表现函数。

源码：`Source/Client/SO3UI/krepresentscripttable.cpp`

---

## 玩家资源函数

### Player_GetAnimationResource {#Player_GetAnimationResource}

```lua
szResource = Player_GetAnimationResource(dwRoleType, dwMountType)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| dwRoleType | `number` | 玩家角色类型 ID |
| dwMountType | `number` | 坐骑类型 ID（无坐骑为 0） |

**返回：** `string` - 动画资源路径

获取玩家角色的动画资源路径。

---

### Player_GetEquipResource {#Player_GetEquipResource}

```lua
szResource = Player_GetEquipResource(dwRoleType, nRepresentIndex, dwRepresentID)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| dwRoleType | `number` | 玩家角色类型 ID |
| nRepresentIndex | `number` | 表现索引（装备槽位） |
| dwRepresentID | `number` | 表现 ID |

**返回：** `string` - 装备资源路径

获取玩家角色的装备资源路径。

---

### Player_GetRidesAnimationResource {#Player_GetRidesAnimationResource}

```lua
szResource = Player_GetRidesAnimationResource(dwMountType, dwRoleType)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| dwMountType | `number` | 坐骑类型 ID |
| dwRoleType | `number` | 玩家角色类型 ID |

**返回：** `string` - 坐骑动画资源路径

获取坐骑的动画资源路径。

---

### Player_GetRidesEquipResource {#Player_GetRidesEquipResource}

```lua
szResource = Player_GetRidesEquipResource(dwMountType, nRepresentIndex, dwRepresentID)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| dwMountType | `number` | 坐骑类型 ID |
| nRepresentIndex | `number` | 表现索引 |
| dwRepresentID | `number` | 表现 ID |

**返回：** `string` - 坐骑装备资源路径

获取坐骑的装备资源路径。

---

## NPC 资源函数

### NPC_GetProtrait {#NPC_GetProtrait}

```lua
szImagePath, nFrame = NPC_GetProtrait(dwTemplateID)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| dwTemplateID | `number` | NPC 模板 ID |

**返回：** `string, number` - 头像图片路径和帧索引

获取 NPC 的头像图片。

---

### NPC_GetHeadImageFile {#NPC_GetHeadImageFile}

```lua
szImagePath = NPC_GetHeadImageFile(dwTemplateID)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| dwTemplateID | `number` | NPC 模板 ID |

**返回：** `string` - 头像图片文件路径

获取 NPC 的头像图片文件路径。

---

### NPC_GetAnimationResource {#NPC_GetAnimationResource}

```lua
szResource = NPC_GetAnimationResource(dwTemplateID)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| dwTemplateID | `number` | NPC 模板 ID |

**返回：** `string` - 动画资源路径

获取 NPC 的动画资源路径。

---

### NPC_GetEquipResource {#NPC_GetEquipResource}

```lua
szResource = NPC_GetEquipResource(dwTemplateID, nRepresentIndex)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| dwTemplateID | `number` | NPC 模板 ID |
| nRepresentIndex | `number` | 表现索引 |

**返回：** `string` - 装备资源路径

获取 NPC 的装备资源路径。

---

## 角色模型函数

### Character_Create {#Character_Create}

```lua
hCharacter = Character_Create(szSceneName, szName)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| szSceneName | `string` | 场景名称 |
| szName | `string` | 角色名称 |

**返回：** `userdata` - 角色句柄

创建用于渲染的角色对象。

---

### Character_Delete {#Character_Delete}

```lua
Character_Delete(hCharacter)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| hCharacter | `userdata` | 角色句柄 |

**返回：** `void`

删除角色对象。

---

### Character_Load {#Character_Load}

```lua
bSuccess = Character_Load(hCharacter, szAnimationSet, szEquip, nSocketIndex)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| hCharacter | `userdata` | 角色句柄 |
| szAnimationSet | `string` | 动画集路径 |
| szEquip | `string` | 装备资源路径 |
| nSocketIndex | `number` | 插槽索引 |

**返回：** `boolean` - 是否加载成功

加载角色资源。

---

### Character_UnloadPart {#Character_UnloadPart}

```lua
Character_UnloadPart(hCharacter, nSocketIndex)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| hCharacter | `userdata` | 角色句柄 |
| nSocketIndex | `number` | 插槽索引 |

**返回：** `void`

卸载角色的特定部件。

---

### Character_ExchangePart {#Character_ExchangePart}

```lua
Character_ExchangePart(hCharacter, nSocketIndex, szEquip)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| hCharacter | `userdata` | 角色句柄 |
| nSocketIndex | `number` | 插槽索引 |
| szEquip | `string` | 装备资源路径 |

**返回：** `void`

更换角色部件。

---

### Character_PlayAnimation {#Character_PlayAnimation}

```lua
Character_PlayAnimation(hCharacter, szAnimation, bLoop, fSpeed)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| hCharacter | `userdata` | 角色句柄 |
| szAnimation | `string` | 动画名称 |
| bLoop | `boolean` | 是否循环播放 |
| fSpeed | `number` | 播放速度 |

**返回：** `void`

播放角色动画。

---

### Character_SetPosition {#Character_SetPosition}

```lua
Character_SetPosition(hCharacter, fX, fY, fZ)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| hCharacter | `userdata` | 角色句柄 |
| fX | `number` | X 位置 |
| fY | `number` | Y 位置 |
| fZ | `number` | Z 位置 |

**返回：** `void`

设置角色位置。

---

### Character_SetDirection {#Character_SetDirection}

```lua
Character_SetDirection(hCharacter, fYaw, fPitch, fRoll)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| hCharacter | `userdata` | 角色句柄 |
| fYaw | `number` | 偏航角 |
| fPitch | `number` | 俯仰角 |
| fRoll | `number` | 翻滚角 |

**返回：** `void`

设置角色朝向/旋转。

---

### Character_SetScale {#Character_SetScale}

```lua
Character_SetScale(hCharacter, fScale)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| hCharacter | `userdata` | 角色句柄 |
| fScale | `number` | 缩放因子 |

**返回：** `void`

设置角色缩放。
