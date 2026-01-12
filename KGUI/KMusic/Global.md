English | [中文](./Global.zh-CN.md)

# Global

## Functions

* <h4 id="LuaPlaySound">PlaySound</h4>
> PlaySound(nType, pcszFilePath[, bGetID[, nPriority[, bCallBackStop]]]) -> [dwSoundID]

Plays a sound.

- `bGetID` (optional): boolean. If true, returns `dwSoundID`.
- `nPriority` (optional): number.
- `bCallBackStop` (optional): boolean.

* <h4 id="LuaStopSound">StopSound</h4>
> StopSound(dwSoundID[, bImmediately])

Stops a sound by ID.
