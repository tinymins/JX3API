English | [中文](./Logic.zh-CN.md)

# Logic Functions

Game logic functions for player, scene, and target operations.

## Player Functions

[`GetClientPlayer`](#GetClientPlayer)
[`GetPlayer`](#GetPlayer)
[`GetPlayerID`](#GetPlayerID)
[`IsPlayer`](#IsPlayer)
[`GetClientTeam`](#GetClientTeam)
[`GetTeamClient`](#GetTeamClient)
[`GetTongClient`](#GetTongClient)
[`GetFellowshipCardClient`](#GetFellowshipCardClient)

## Scene Functions

[`GetClientScene`](#GetClientScene)
[`GetScene`](#GetScene)
[`GetNpc`](#GetNpc)
[`IsNpc`](#IsNpc)
[`GetDoodad`](#GetDoodad)
[`IsDoodad`](#IsDoodad)

## Target Functions

[`GetTargetHandle`](#GetTargetHandle)
[`SetTarget`](#SetTarget)
[`GetControlPlayerID`](#GetControlPlayerID)

---

* <h4 id="GetClientPlayer">GetClientPlayer</h4>

Gets the client player object (current character).

 > ([`KPlayer`](./KGameObject/KPlayer.md) player) GetClientPlayer()

* <h4 id="GetPlayer">GetPlayer</h4>

Gets a player object by ID.

 > ([`KPlayer`](./KGameObject/KPlayer.md) player) GetPlayer(`number` dwPlayerID)

* <h4 id="GetPlayerID">GetPlayerID</h4>

Gets player ID from a character object.

 > (`number` dwPlayerID) GetPlayerID(`KCharacter` character)

* <h4 id="IsPlayer">IsPlayer</h4>

Checks if an ID belongs to a player.

 > (`boolean` bIsPlayer) IsPlayer(`number` dwID)

* <h4 id="GetClientTeam">GetClientTeam</h4>

Gets the client team object.

 > (`KTeam` team) GetClientTeam()

* <h4 id="GetTeamClient">GetTeamClient</h4>

Gets the team client object.

 > ([`KTeamClient`](./KClient/KTeamClient.md) teamClient) GetTeamClient()

* <h4 id="GetTongClient">GetTongClient</h4>

Gets the guild client object.

 > ([`KTongClient`](./KClient/KTongClient.md) tongClient) GetTongClient()

* <h4 id="GetFellowshipCardClient">GetFellowshipCardClient</h4>

Gets the fellowship card client object.

 > ([`KFellowshipCardClient`](./KClient/KFellowshipCardClient.md) cardClient) GetFellowshipCardClient()

* <h4 id="GetClientScene">GetClientScene</h4>

Gets the client scene object (current map).

 > ([`KScene`](./KGameObject/KScene.md) scene) GetClientScene()

* <h4 id="GetScene">GetScene</h4>

Gets a scene object.

 > ([`KScene`](./KGameObject/KScene.md) scene) GetScene()

* <h4 id="GetNpc">GetNpc</h4>

Gets an NPC object by ID.

 > ([`KNpc`](./KGameObject/KNpc.md) npc) GetNpc(`number` dwNpcID)

* <h4 id="IsNpc">IsNpc</h4>

Checks if an ID belongs to an NPC.

 > (`boolean` bIsNpc) IsNpc(`number` dwID)

* <h4 id="GetDoodad">GetDoodad</h4>

Gets a doodad object by ID.

 > ([`KDoodad`](./KGameObject/KDoodad.md) doodad) GetDoodad(`number` dwDoodadID)

* <h4 id="IsDoodad">IsDoodad</h4>

Checks if an ID belongs to a doodad.

 > (`boolean` bIsDoodad) IsDoodad(`number` dwID)

* <h4 id="GetTargetHandle">GetTargetHandle</h4>

Gets the current target handle.

 > (`number` dwHandle) GetTargetHandle()

* <h4 id="SetTarget">SetTarget</h4>

Sets the current target.

 > (`void`) SetTarget(`number` nTargetType, `number` dwTargetID)

* <h4 id="GetControlPlayerID">GetControlPlayerID</h4>

Gets the ID of the controlled player.

 > (`number` dwPlayerID) GetControlPlayerID()

---

## Disabled Functions

The following functions exist in source but are commented out and cannot be used:

* <h4 id="GetNearbyDoodadList">~~GetNearbyDoodadList~~</h4>

⚠️ **Disabled** - This function is commented out.

```lua
-- Commented out
-- local tList = GetNearbyDoodadList()
```

* <h4 id="GetNearbyNpcList">~~GetNearbyNpcList~~</h4>

⚠️ **Disabled** - This function is commented out.

```lua
-- Commented out
-- local tList = GetNearbyNpcList()
```

* <h4 id="GetNearbyPlayerList">~~GetNearbyPlayerList~~</h4>

⚠️ **Disabled** - This function is commented out.

```lua
-- Commented out
-- local tList = GetNearbyPlayerList()
```
