English | [中文](./Map.zh-CN.md)

# Map Functions

Functions for map-related operations.

## Functions

[`GetMapID`](#GetMapID)
[`GetMapName`](#GetMapName)
[`GetMapInfo`](#GetMapInfo)
[`GetMapParams`](#GetMapParams)
[`GetMapCopyIndex`](#GetMapCopyIndex)
[`Scene2World`](#Scene2World)
[`World2Scene`](#World2Scene)

---

* <h4 id="GetMapID">GetMapID</h4>

Gets the current map ID.

 > (`number` nMapID) GetMapID()

* <h4 id="GetMapName">GetMapName</h4>

Gets the name of a map by ID.

 > (`string` szName) GetMapName(`number` nMapID)

* <h4 id="GetMapInfo">GetMapInfo</h4>

Gets map information.

 > (`table` tMapInfo) GetMapInfo(`number` nMapID)

* <h4 id="GetMapParams">GetMapParams</h4>

Gets map parameters.

 > (`table` tParams) GetMapParams(`number` nMapID)

* <h4 id="GetMapCopyIndex">GetMapCopyIndex</h4>

Gets the map copy index.

 > (`number` nCopyIndex) GetMapCopyIndex()

* <h4 id="Scene2World">Scene2World</h4>

Converts scene coordinates to world coordinates.

 > (`number` nX, `number` nY) Scene2World(`number` nSceneX, `number` nSceneY)

* <h4 id="World2Scene">World2Scene</h4>

Converts world coordinates to scene coordinates.

 > (`number` nSceneX, `number` nSceneY) World2Scene(`number` nX, `number` nY)

---

## Disabled Functions

The following functions exist in source but are commented out and cannot be used:

* <h4 id="GetMinimapLayer">~~GetMinimapLayer~~</h4>

⚠️ **Disabled** - This function is commented out.

```lua
-- Commented out
-- local nLayer = GetMinimapLayer()
```

* <h4 id="GetRegionInfo">~~GetRegionInfo~~</h4>

⚠️ **Disabled** - This function is commented out.

```lua
-- Commented out
-- local tInfo = GetRegionInfo(nMapID, nRegionID)
```
