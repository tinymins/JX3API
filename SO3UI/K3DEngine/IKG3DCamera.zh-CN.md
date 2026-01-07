# IKG3DCamera

Methods:
- `GetPosition`
- `SetPosition`
- `GetLookAtPosition`
- `SetLookAtPosition`
- `GetUpDirection`
- `SetUpDirection`
- `GetCurrentState`
- `UpdateCamera`
- `SetPerspective`
- `SetOrthogonal`

* <h4 id="LuaCamera_GetPosition">GetPosition</h4>
> (number, number, number) IKG3DCamera:GetPosition()

返回相机位置 `x, y, z`。

* <h4 id="LuaCamera_SetPosition">SetPosition</h4>
> () IKG3DCamera:SetPosition(x, y, z)

设置相机位置。

* <h4 id="LuaCamera_GetLookAtPosition">GetLookAtPosition</h4>
> (number, number, number) IKG3DCamera:GetLookAtPosition()

返回相机朝向点（look-at）位置 `x, y, z`。

* <h4 id="LuaCamera_SetLookAtPosition">SetLookAtPosition</h4>
> () IKG3DCamera:SetLookAtPosition(x, y, z)

设置相机朝向点位置。

* <h4 id="LuaCamera_GetUpDirection">GetUpDirection</h4>
> (number, number, number) IKG3DCamera:GetUpDirection()

返回相机上方向向量 `x, y, z`。

* <h4 id="LuaCamera_SetUpDirection">SetUpDirection</h4>
> () IKG3DCamera:SetUpDirection(x, y, z)

设置相机上方向。

* <h4 id="LuaCamera_GetCurrentState">GetCurrentState</h4>
> (number) IKG3DCamera:GetCurrentState()

返回当前状态值（number）。

* <h4 id="LuaCamera_UpdateCamera">UpdateCamera</h4>
> () IKG3DCamera:UpdateCamera(px, py, pz, ax, ay, az, fLookAtOffset, fTargetSpeed)

用目标位置向量 `(px,py,pz)`、轴向向量 `(ax,ay,az)` 以及两个标量参数更新相机。

* <h4 id="LuaCamera_SetPerspective">SetPerspective</h4>
> () IKG3DCamera:SetPerspective(fFovy, fAspect, fZNear, fZFar)

设置全局透视投影参数。

实现会先读取当前值，然后对传入参数中“是 number 的项”进行覆盖后再写回。

* <h4 id="LuaCamera_SetOrthogonal">SetOrthogonal</h4>
> () IKG3DCamera:SetOrthogonal(fWidth, fHeight, fZNear, fZFar)

设置全局正交投影参数。

实现会先读取当前值，然后对传入参数中“是 number 的项”进行覆盖后再写回。
