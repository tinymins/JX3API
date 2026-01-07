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

Returns the camera position as `x, y, z`.

* <h4 id="LuaCamera_SetPosition">SetPosition</h4>
> () IKG3DCamera:SetPosition(x, y, z)

Sets the camera position.

* <h4 id="LuaCamera_GetLookAtPosition">GetLookAtPosition</h4>
> (number, number, number) IKG3DCamera:GetLookAtPosition()

Returns the camera look-at position as `x, y, z`.

* <h4 id="LuaCamera_SetLookAtPosition">SetLookAtPosition</h4>
> () IKG3DCamera:SetLookAtPosition(x, y, z)

Sets the camera look-at position.

* <h4 id="LuaCamera_GetUpDirection">GetUpDirection</h4>
> (number, number, number) IKG3DCamera:GetUpDirection()

Returns the camera up direction as `x, y, z`.

* <h4 id="LuaCamera_SetUpDirection">SetUpDirection</h4>
> () IKG3DCamera:SetUpDirection(x, y, z)

Sets the camera up direction.

* <h4 id="LuaCamera_GetCurrentState">GetCurrentState</h4>
> (number) IKG3DCamera:GetCurrentState()

Returns the current state value as a number.

* <h4 id="LuaCamera_UpdateCamera">UpdateCamera</h4>
> () IKG3DCamera:UpdateCamera(px, py, pz, ax, ay, az, fLookAtOffset, fTargetSpeed)

Updates the camera with a target position vector `(px,py,pz)`, axes vector `(ax,ay,az)`, and two scalar parameters.

* <h4 id="LuaCamera_SetPerspective">SetPerspective</h4>
> () IKG3DCamera:SetPerspective(fFovy, fAspect, fZNear, fZFar)

Sets global perspective parameters.

The function first queries current values and then overwrites them with the provided arguments (if the argument is a number).

* <h4 id="LuaCamera_SetOrthogonal">SetOrthogonal</h4>
> () IKG3DCamera:SetOrthogonal(fWidth, fHeight, fZNear, fZFar)

Sets global orthogonal projection parameters.

The function first queries current values and then overwrites them with the provided arguments (if the argument is a number).
