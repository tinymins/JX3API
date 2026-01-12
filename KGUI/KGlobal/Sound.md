English | [中文](./Sound.zh-CN.md)

# Sound Functions

Functions for sound playback.

## Functions

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

Plays a sound effect.

 > (`number` nSoundID) PlaySound(`number` nSoundType, `string` szFile)

* <h4 id="StopSound">StopSound</h4>

Stops a playing sound.

 > (`void`) StopSound(`number` nSoundID)

* <h4 id="PlayMusic">PlayMusic</h4>

Plays background music.

 > (`void`) PlayMusic(`string` szFile)

* <h4 id="StopMusic">StopMusic</h4>

Stops background music.

 > (`void`) StopMusic()

* <h4 id="SetMusicVolume">SetMusicVolume</h4>

Sets the music volume.

 > (`void`) SetMusicVolume(`number` nVolume)

* <h4 id="GetMusicVolume">GetMusicVolume</h4>

Gets the music volume.

 > (`number` nVolume) GetMusicVolume()

* <h4 id="SetSoundVolume">SetSoundVolume</h4>

Sets the sound volume.

 > (`void`) SetSoundVolume(`number` nVolume)

* <h4 id="GetSoundVolume">GetSoundVolume</h4>

Gets the sound volume.

 > (`number` nVolume) GetSoundVolume()
