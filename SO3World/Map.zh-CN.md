[English](./Map.md) | 中文

# 地图函数

地图相关操作函数。

## 函数

[`GetMapID`](#GetMapID)
[`GetMapName`](#GetMapName)
[`GetMapInfo`](#GetMapInfo)
[`GetMapParams`](#GetMapParams)
[`GetMapCopyIndex`](#GetMapCopyIndex)
[`Scene2World`](#Scene2World)
[`World2Scene`](#World2Scene)

---

* <h4 id="GetMapID">GetMapID</h4>

获取当前地图 ID。

 > (`number` nMapID) GetMapID()

* <h4 id="GetMapName">GetMapName</h4>

根据 ID 获取地图名称。

 > (`string` szName) GetMapName(`number` nMapID)

* <h4 id="GetMapInfo">GetMapInfo</h4>

获取地图信息。

 > (`table` tMapInfo) GetMapInfo(`number` nMapID)

* <h4 id="GetMapParams">GetMapParams</h4>

获取地图参数。

 > (`table` tParams) GetMapParams(`number` nMapID)

* <h4 id="GetMapCopyIndex">GetMapCopyIndex</h4>

获取地图副本索引。

 > (`number` nCopyIndex) GetMapCopyIndex()

* <h4 id="Scene2World">Scene2World</h4>

将场景坐标转换为世界坐标。

 > (`number` nX, `number` nY) Scene2World(`number` nSceneX, `number` nSceneY)

* <h4 id="World2Scene">World2Scene</h4>

将世界坐标转换为场景坐标。

 > (`number` nSceneX, `number` nSceneY) World2Scene(`number` nX, `number` nY)

---

## 已禁用的函数

以下函数在源码中存在但已被注释，无法使用：

* <h4 id="GetMinimapLayer">~~GetMinimapLayer~~</h4>

⚠️ **已禁用** - 此函数已被注释。

```lua
-- 已注释
-- local nLayer = GetMinimapLayer()
```

* <h4 id="GetRegionInfo">~~GetRegionInfo~~</h4>

⚠️ **已禁用** - 此函数已被注释。

```lua
-- 已注释
-- local tInfo = GetRegionInfo(nMapID, nRegionID)
```
