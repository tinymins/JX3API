[English](./Tab.md) | 中文

# Tab

## 函数

* <h4 id="LuaTab_Create">Create</h4>
> Tab.Create(dummy) -> ITabFile

创建一个 `ITabFile` userdata。

- `dummy`：任意值。该参数是必填的。

* <h4 id="LuaTab_Open">Open</h4>
> Tab.Open(pcszFileName) -> ITabFile

打开 tab 文件并返回 `ITabFile` userdata。

失败时不返回任何值。

* <h4 id="LuaTab_AdjustOpen">AdjustOpen</h4>
> Tab.AdjustOpen(pcszFileName) -> ITabFile

与 `Tab.Open` 类似，但会优先尝试调整后的路径。

失败时不返回任何值。
