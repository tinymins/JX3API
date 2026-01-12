English | [中文](./Tab.zh-CN.md)

# Tab

## Functions

* <h4 id="LuaTab_Create">Create</h4>
> Tab.Create(dummy) -> ITabFile

Creates an `ITabFile` userdata.

- `dummy`: any value. This argument is required.

* <h4 id="LuaTab_Open">Open</h4>
> Tab.Open(pcszFileName) -> ITabFile

Opens a tab file and returns an `ITabFile` userdata.

Returns nothing on failure.

* <h4 id="LuaTab_AdjustOpen">AdjustOpen</h4>
> Tab.AdjustOpen(pcszFileName) -> ITabFile

Like `Tab.Open`, but will try an adjusted path first.

Returns nothing on failure.
