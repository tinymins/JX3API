# ItemImage

[`SetFrame`](#LuaItemImage_SetFrame)
[`GetFrame`](#LuaItemImage_GetFrame)
[`AutoSize`](#LuaItemImage_AutoSize)
[`SetImageType`](#LuaItemImage_SetImageType)
[`GetImageType`](#LuaItemImage_GetImageType)
[`SetPercentage`](#LuaItemImage_SetPercentage)
[`GetPercentage`](#LuaItemImage_GetPercentage)
[`SetRotate`](#LuaItemImage_SetRotate)
[`GetRotate`](#LuaItemImage_GetRotate)
[`SetTimeStartAngle`](#LuaItemImage_SetTimeStartAngle)
[`GetImageID`](#LuaItemImage_GetImageID)
[`GetImageInfoID`](#LuaItemImage_GetImageInfoID)
[`GetImagePath`](#LuaItemImage_GetImagePath)
[`IsFromTexturFile`](#LuaItemImage_IsFromTexturFile)
[`FromUITex`](#LuaItemImage_FromUITex)
[`FromTextureFile`](#LuaItemImage_FromTextureFile)
[`FromRemoteFile`](#LuaItemImage_FromRemoteFile)
[`UnloadSource`](#LuaItemImage_UnloadSource)
[`FromScene`](#LuaItemImage_FromScene)
[`FromImageID`](#LuaItemImage_FromImageID)
[`FromIconID`](#LuaItemImage_FromIconID)
[`FromWindow`](#LuaItemImage_FromWindow)
[`FromItem`](#LuaItemImage_FromItem)
[`ToManagedImage`](#LuaItemImage_ToManagedImage)
[`SetPaintOffset`](#LuaItemImage_SetPaintOffset)
[`FromSpecialMiniScene`](#LuaItemImage_FromSpecialMiniScene)
[`SaveImage`](#LuaItemImage_SaveImage)

* <h4 id="LuaItemImage_SetFrame">SetFrame</h4>
Set image frame.

 > (`void`) ItemImage:SetFrame(`number` nFrame)

 ````lua
 ItemImage:SetFrame(0)
 ````

* <h4 id="LuaItemImage_GetFrame">GetFrame</h4>
Get current image frame.

 > (`number` nFrame) ItemImage:GetFrame()

 ````lua
 local nFrame = ItemImage:GetFrame()
 ````

* <h4 id="LuaItemImage_AutoSize">AutoSize</h4>
Auto size item by current image.

 > (`void`) ItemImage:AutoSize()

 ````lua
 ItemImage:AutoSize()
 ````

* <h4 id="LuaItemImage_SetImageType">SetImageType</h4>
Set image render type.

 > (`void`) ItemImage:SetImageType(`number` nType)

 ````lua
 ItemImage:SetImageType(0)
 ````

* <h4 id="LuaItemImage_GetImageType">GetImageType</h4>
Get image render type.

 > (`number` nType) ItemImage:GetImageType()

 ````lua
 local nType = ItemImage:GetImageType()
 ````

* <h4 id="LuaItemImage_SetPercentage">SetPercentage</h4>
Set image percentage (used by some image types).

 > (`void`) ItemImage:SetPercentage(`number` fPercentage)

 ````lua
 ItemImage:SetPercentage(1.0)
 ````

* <h4 id="LuaItemImage_GetPercentage">GetPercentage</h4>
Get current image percentage.

 > (`number` fPercentage) ItemImage:GetPercentage()

 ````lua
 local fPercentage = ItemImage:GetPercentage()
 ````

* <h4 id="LuaItemImage_SetRotate">SetRotate</h4>
Set image rotation.

 > (`void`) ItemImage:SetRotate(`number` fRotate)

 ````lua
 ItemImage:SetRotate(0)
 ````

* <h4 id="LuaItemImage_GetRotate">GetRotate</h4>
Get image rotation.

 > (`number` fRotate) ItemImage:GetRotate()

 ````lua
 local fRotate = ItemImage:GetRotate()
 ````

* <h4 id="LuaItemImage_SetTimeStartAngle">SetTimeStartAngle</h4>
Set timer start angle (used by some image types).

 > (`void`) ItemImage:SetTimeStartAngle(`number` fAngle)

 ````lua
 ItemImage:SetTimeStartAngle(0)
 ````

* <h4 id="LuaItemImage_GetImageID">GetImageID</h4>
Get current image id.

 > (`number` dwImageID) ItemImage:GetImageID()

 ````lua
 local dwImageID = ItemImage:GetImageID()
 ````

* <h4 id="LuaItemImage_GetImageInfoID">GetImageInfoID</h4>
Get current image info id.

 > (`number` dwImageInfoID) ItemImage:GetImageInfoID()

 ````lua
 local dwImageInfoID = ItemImage:GetImageInfoID()
 ````

* <h4 id="LuaItemImage_GetImagePath">GetImagePath</h4>
Get current image path.

If current frame is >= 0, it will also return the frame.

 > (`string` szPath[, `number` nFrame]) ItemImage:GetImagePath()

 ````lua
 local szPath = ItemImage:GetImagePath()
 local szPath, nFrame = ItemImage:GetImagePath()
 ````

* <h4 id="LuaItemImage_IsFromTexturFile">IsFromTexturFile</h4>
Whether current image source is from texture file.

 > (`bool` bIsFromTextureFile) ItemImage:IsFromTexturFile()

 ````lua
 local bIsFromTextureFile = ItemImage:IsFromTexturFile()
 ````

* <h4 id="LuaItemImage_FromUITex">FromUITex</h4>
Load image from UI texture (with a frame).

 > (`void`) ItemImage:FromUITex(`string` szImage, `number` nFrame)

 ````lua
 ItemImage:FromUITex("interface/ui/image/ui_tex.tga", 0)
 ````

* <h4 id="LuaItemImage_FromTextureFile">FromTextureFile</h4>
Load image from texture file.

 > (`void`) ItemImage:FromTextureFile(`string` szImage[, `bool` bCache])

 ````lua
 ItemImage:FromTextureFile("interface/ui/image/tex.tga")
 ItemImage:FromTextureFile("interface/ui/image/tex.tga", true)
 ````

* <h4 id="LuaItemImage_FromRemoteFile">FromRemoteFile</h4>
Load image from remote URL.

This calls Lua global handler `__OnKItemImage_LoadRemoteFile(ItemImage, url, cache, callback)`.

 > (`void`) ItemImage:FromRemoteFile(`string` szUrl[, `bool` bCache[, `function` fnCallback]])

 ````lua
 ItemImage:FromRemoteFile("https://example.com/a.png")
 ItemImage:FromRemoteFile("https://example.com/a.png", true)
 ItemImage:FromRemoteFile("https://example.com/a.png", true, function(bOk)
     -- callback handled by __OnKItemImage_LoadRemoteFile
 end)
 ````

* <h4 id="LuaItemImage_UnloadSource">UnloadSource</h4>
Unload current image source.

 > (`void`) ItemImage:UnloadSource()

 ````lua
 ItemImage:UnloadSource()
 ````

* <h4 id="LuaItemImage_FromScene">FromScene</h4>
Capture from a scene.

 > (`void`) ItemImage:FromScene(`userdata|number` sceneId)

 ````lua
 ItemImage:FromScene(Scene)
 ````

* <h4 id="LuaItemImage_FromImageID">FromImageID</h4>
Load by image id.

 > (`void`) ItemImage:FromImageID(`number` dwImageID)

 ````lua
 ItemImage:FromImageID(123)
 ````

* <h4 id="LuaItemImage_FromIconID">FromIconID</h4>
Load by icon id.

 > (`void`) ItemImage:FromIconID(`number` nIconID)

 ````lua
 ItemImage:FromIconID(123)
 ````

* <h4 id="LuaItemImage_FromWindow">FromWindow</h4>
Capture from a window.

 > (`void`) ItemImage:FromWindow(`WndWindow` WndWindow)

 ````lua
 ItemImage:FromWindow(WndWindow)
 ````

* <h4 id="LuaItemImage_FromItem">FromItem</h4>
Capture from another item.

 > (`void`) ItemImage:FromItem(`ItemNull` Item)

 ````lua
 ItemImage:FromItem(ItemNull)
 ````

* <h4 id="LuaItemImage_ToManagedImage">ToManagedImage</h4>
Convert to managed image.

 > (`void`) ItemImage:ToManagedImage()

 ````lua
 ItemImage:ToManagedImage()
 ````

* <h4 id="LuaItemImage_SetPaintOffset">SetPaintOffset</h4>
Set paint offset by index (percent values).

 > (`void`) ItemImage:SetPaintOffset(`number` nIndex, `number` fPercentX, `number` fPercentY)

 ````lua
 ItemImage:SetPaintOffset(0, 0.5, 0.5)
 ````

* <h4 id="LuaItemImage_FromSpecialMiniScene">FromSpecialMiniScene</h4>
Capture from special mini scene.

 > (`void`) ItemImage:FromSpecialMiniScene(`userdata|number` sceneId, `string` szImageFile, `number` nUid)

 ````lua
 ItemImage:FromSpecialMiniScene(Scene, "interface/ui/image/out.png", 1)
 ````

* <h4 id="LuaItemImage_SaveImage">SaveImage</h4>
Save current image to file.

 > (`void`) ItemImage:SaveImage(`string` szImageFile)

 ````lua
 ItemImage:SaveImage("interface/ui/image/out.png")
 ````
