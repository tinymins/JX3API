# 玩家资源函数

玩家视觉资源和动画函数。

---

## 动画资源

### Player_GetAnimationResource {#Player_GetAnimationResource}

```lua
szPath = Player_GetAnimationResource(dwPlayerID, szAnimationName)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| dwPlayerID | `number` | 玩家 ID |
| szAnimationName | `string` | 动画名称 |

**返回:** `string` - 动画资源路径

获取玩家的动画资源路径。

---

### Player_GetRidesAnimationResource {#Player_GetRidesAnimationResource}

```lua
szPath = Player_GetRidesAnimationResource(dwPlayerID, szAnimationName)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| dwPlayerID | `number` | 玩家 ID |
| szAnimationName | `string` | 动画名称 |

**返回:** `string` - 坐骑动画资源路径

获取玩家的坐骑动画资源路径。

---

## 装备资源

### Player_GetEquipResource {#Player_GetEquipResource}

```lua
szPath = Player_GetEquipResource(dwPlayerID, nEquipSlot)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| dwPlayerID | `number` | 玩家 ID |
| nEquipSlot | `number` | 装备槽位索引 |

**返回:** `string` - 装备资源路径

获取玩家的装备资源路径。

---

### Player_GetRidesEquipResource {#Player_GetRidesEquipResource}

```lua
szPath = Player_GetRidesEquipResource(dwPlayerID, nEquipSlot)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| dwPlayerID | `number` | 玩家 ID |
| nEquipSlot | `number` | 装备槽位索引 |

**返回:** `string` - 坐骑装备资源路径

获取玩家的坐骑装备资源路径。

---

## NPC 资源

### NPC_GetProtrait {#NPC_GetProtrait}

```lua
szPath = NPC_GetProtrait(dwNpcTemplateID)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| dwNpcTemplateID | `number` | NPC 模板 ID |

**返回:** `string` - 头像图片路径

获取 NPC 的头像图片路径。

---

### NPC_GetHeadImageFile {#NPC_GetHeadImageFile}

```lua
szPath = NPC_GetHeadImageFile(dwNpcTemplateID)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| dwNpcTemplateID | `number` | NPC 模板 ID |

**返回:** `string` - 头像文件路径

获取 NPC 的头像文件路径。

---

## 玩家能量 UI

### PlayerEnergyUI_Update {#PlayerEnergyUI_Update}

```lua
PlayerEnergyUI_Update()
```

**返回:** `void`

更新玩家能量 UI 显示。

---

### PlayerEnergyUI_GetUpdateFunc {#PlayerEnergyUI_GetUpdateFunc}

```lua
fnUpdate = PlayerEnergyUI_GetUpdateFunc()
```

**返回:** `function` - 更新函数

获取玩家能量 UI 更新函数。

---

### PlayerEnergyUI_ChangeStyle {#PlayerEnergyUI_ChangeStyle}

```lua
PlayerEnergyUI_ChangeStyle(nStyle)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| nStyle | `number` | 样式 ID |

**返回:** `void`

更改玩家能量 UI 样式。

---

## 相机

### Camera_GetRTParams {#Camera_GetRTParams}

```lua
tParams = Camera_GetRTParams()
```

**返回:** `table` - 相机实时参数

获取相机实时参数。

---

### Camera_GetParams {#Camera_GetParams}

```lua
tParams = Camera_GetParams()
```

**返回:** `table` - 相机参数

获取相机参数。
