[English](./Global.md) | 中文

# Global

## 函数

* <h4 id="LuaPlaySound">PlaySound</h4>
> PlaySound(nType, pcszFilePath[, bGetID[, nPriority[, bCallBackStop]]]) -> [dwSoundID]

播放音效。

- `bGetID`（可选）：boolean。为真时返回 `dwSoundID`。
- `nPriority`（可选）：number。
- `bCallBackStop`（可选）：boolean。

* <h4 id="LuaStopSound">StopSound</h4>
> StopSound(dwSoundID[, bImmediately])

按 ID 停止音效。
