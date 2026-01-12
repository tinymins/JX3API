[English](./Data.md) | 中文

# 数据函数

自定义数据存储操作相关函数。

## 函数

[`SaveCustomData`](#SaveCustomData)
[`LoadCustomData`](#LoadCustomData)
[`GetCustomData`](#GetCustomData)
[`SetCustomData`](#SetCustomData)
[`RemoveCustomData`](#RemoveCustomData)
[`SaveRoleCustomData`](#SaveRoleCustomData)
[`LoadRoleCustomData`](#LoadRoleCustomData)
[`GetRoleCustomData`](#GetRoleCustomData)
[`SetRoleCustomData`](#SetRoleCustomData)
[`RemoveRoleCustomData`](#RemoveRoleCustomData)

---

* <h4 id="SaveCustomData">SaveCustomData</h4>

将自定义数据保存到磁盘（账号级别）。

 > (`void`) SaveCustomData(`string` szFile)

* <h4 id="LoadCustomData">LoadCustomData</h4>

从磁盘加载自定义数据（账号级别）。

 > (`void`) LoadCustomData(`string` szFile)

* <h4 id="GetCustomData">GetCustomData</h4>

根据键获取自定义数据（账号级别）。

 > (`any` value) GetCustomData(`string` szKey)

* <h4 id="SetCustomData">SetCustomData</h4>

根据键设置自定义数据（账号级别）。

 > (`void`) SetCustomData(`string` szKey, `any` value)

* <h4 id="RemoveCustomData">RemoveCustomData</h4>

根据键移除自定义数据（账号级别）。

 > (`void`) RemoveCustomData(`string` szKey)

* <h4 id="SaveRoleCustomData">SaveRoleCustomData</h4>

将角色专属自定义数据保存到磁盘。

 > (`void`) SaveRoleCustomData(`string` szFile)

* <h4 id="LoadRoleCustomData">LoadRoleCustomData</h4>

从磁盘加载角色专属自定义数据。

 > (`void`) LoadRoleCustomData(`string` szFile)

* <h4 id="GetRoleCustomData">GetRoleCustomData</h4>

根据键获取角色专属自定义数据。

 > (`any` value) GetRoleCustomData(`string` szKey)

* <h4 id="SetRoleCustomData">SetRoleCustomData</h4>

根据键设置角色专属自定义数据。

 > (`void`) SetRoleCustomData(`string` szKey, `any` value)

* <h4 id="RemoveRoleCustomData">RemoveRoleCustomData</h4>

根据键移除角色专属自定义数据。

 > (`void`) RemoveRoleCustomData(`string` szKey)
