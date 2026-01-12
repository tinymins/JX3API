# 存储函数

在线存储和自定义数据持久化函数。

---

## 窗口锚点存储

### GetOnlineFrameAnchor {#GetOnlineFrameAnchor}

```lua
tData = GetOnlineFrameAnchor(szKey)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szKey | `string` | 存储键名 |

**返回:** `any` - 存储的数据

获取在线窗口锚点数据。用于跨会话存储 UI 窗口位置。

---

### SetOnlineFrameAnchor {#SetOnlineFrameAnchor}

```lua
SetOnlineFrameAnchor(szKey, data)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szKey | `string` | 存储键名 |
| data | `any` | 要存储的数据 |

**返回:** `void`

设置在线窗口锚点数据。

---

## 插件自定义数据

### GetAddonCustomData {#GetAddonCustomData}

```lua
tData = GetAddonCustomData(szSubKey)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szSubKey | `string` | 可选：数据子键名 |

**返回:** `any` - 存储的自定义数据

获取插件特定的自定义数据。存储键名自动按插件包名进行命名空间隔离。

---

### SetAddonCustomData {#SetAddonCustomData}

```lua
SetAddonCustomData(szSubKey, data)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szSubKey | `string` | 可选：数据子键名 |
| data | `any` | 要存储的数据 |

**返回:** `void`

设置插件特定的自定义数据。数据按插件包名进行命名空间隔离。

---

## 在线插件数据

### GetOnlineAddonCustomData {#GetOnlineAddonCustomData}

```lua
tData = GetOnlineAddonCustomData(szSubKey)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szSubKey | `string` | 可选：数据子键名 |

**返回:** `any` - 存储的在线数据

获取插件特定的在线自定义数据（同步到服务器）。

---

### SetOnlineAddonCustomData {#SetOnlineAddonCustomData}

```lua
SetOnlineAddonCustomData(szSubKey, data)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szSubKey | `string` | 可选：数据子键名 |
| data | `any` | 要存储的数据 |

**返回:** `void`

设置插件特定的在线自定义数据（同步到服务器）。

---

## 导航器

### Navigator_SetID {#Navigator_SetID}

```lua
Navigator_SetID(nID)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| nID | `number` | 导航器 ID |

**返回:** `void`

通过 ID 设置导航目标。

---

### Navigator_SetPoint {#Navigator_SetPoint}

```lua
Navigator_SetPoint(nMapID, nX, nY)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| nMapID | `number` | 地图 ID |
| nX | `number` | X 坐标 |
| nY | `number` | Y 坐标 |

**返回:** `void`

设置导航目标点。

---

### Navigator_Remove {#Navigator_Remove}

```lua
Navigator_Remove()
```

**返回:** `void`

移除当前导航目标。
