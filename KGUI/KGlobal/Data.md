English | [中文](./Data.zh-CN.md)

# Data Functions

Functions for custom data storage operations.

## Functions

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

Saves custom data to disk (account-level).

 > (`void`) SaveCustomData(`string` szFile)

* <h4 id="LoadCustomData">LoadCustomData</h4>

Loads custom data from disk (account-level).

 > (`void`) LoadCustomData(`string` szFile)

* <h4 id="GetCustomData">GetCustomData</h4>

Gets custom data by key (account-level).

 > (`any` value) GetCustomData(`string` szKey)

* <h4 id="SetCustomData">SetCustomData</h4>

Sets custom data by key (account-level).

 > (`void`) SetCustomData(`string` szKey, `any` value)

* <h4 id="RemoveCustomData">RemoveCustomData</h4>

Removes custom data by key (account-level).

 > (`void`) RemoveCustomData(`string` szKey)

* <h4 id="SaveRoleCustomData">SaveRoleCustomData</h4>

Saves role-specific custom data to disk.

 > (`void`) SaveRoleCustomData(`string` szFile)

* <h4 id="LoadRoleCustomData">LoadRoleCustomData</h4>

Loads role-specific custom data from disk.

 > (`void`) LoadRoleCustomData(`string` szFile)

* <h4 id="GetRoleCustomData">GetRoleCustomData</h4>

Gets role-specific custom data by key.

 > (`any` value) GetRoleCustomData(`string` szKey)

* <h4 id="SetRoleCustomData">SetRoleCustomData</h4>

Sets role-specific custom data by key.

 > (`void`) SetRoleCustomData(`string` szKey, `any` value)

* <h4 id="RemoveRoleCustomData">RemoveRoleCustomData</h4>

Removes role-specific custom data by key.

 > (`void`) RemoveRoleCustomData(`string` szKey)
