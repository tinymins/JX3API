[English](./Sound.md) | 中文

# 声音函数

声音播放相关函数。

## 函数

[`PlaySound`](#PlaySound)
[`StopSound`](#StopSound)
[`PlayMusic`](#PlayMusic)
[`StopMusic`](#StopMusic)
[`SetMusicVolume`](#SetMusicVolume)
[`GetMusicVolume`](#GetMusicVolume)
[`SetSoundVolume`](#SetSoundVolume)
[`GetSoundVolume`](#GetSoundVolume)

---

* <h4 id="PlaySound">PlaySound</h4>

播放音效。

 > (`number` nSoundID) PlaySound(`number` nSoundType, `string` szFile)

* <h4 id="StopSound">StopSound</h4>

停止播放音效。

 > (`void`) StopSound(`number` nSoundID)

* <h4 id="PlayMusic">PlayMusic</h4>

播放背景音乐。

 > (`void`) PlayMusic(`string` szFile)

* <h4 id="StopMusic">StopMusic</h4>

停止背景音乐。

 > (`void`) StopMusic()

* <h4 id="SetMusicVolume">SetMusicVolume</h4>

设置音乐音量。

 > (`void`) SetMusicVolume(`number` nVolume)

* <h4 id="GetMusicVolume">GetMusicVolume</h4>

获取音乐音量。

 > (`number` nVolume) GetMusicVolume()

* <h4 id="SetSoundVolume">SetSoundVolume</h4>

设置音效音量。

 > (`void`) SetSoundVolume(`number` nVolume)

* <h4 id="GetSoundVolume">GetSoundVolume</h4>

获取音效音量。

 > (`number` nVolume) GetSoundVolume()
