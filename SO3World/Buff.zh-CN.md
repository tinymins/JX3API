[English](./Buff.md) | 中文

# Buff 函数

Buff/Debuff 操作相关函数。

## 函数

[`GetBuffName`](#GetBuffName)
[`GetBuffInfo`](#GetBuffInfo)
[`GetBuffDesc`](#GetBuffDesc)
[`GetBuffTip`](#GetBuffTip)
[`GetBuffAttrib`](#GetBuffAttrib)

---

* <h4 id="GetBuffName">GetBuffName</h4>

获取 Buff 名称。

 > (`string` szName) GetBuffName(`number` dwBuffID, `number` nLevel)

* <h4 id="GetBuffInfo">GetBuffInfo</h4>

获取 Buff 信息。

 > (`table` tBuffInfo) GetBuffInfo(`number` dwBuffID, `number` nLevel)

* <h4 id="GetBuffDesc">GetBuffDesc</h4>

获取 Buff 描述。

 > (`string` szDesc) GetBuffDesc(`number` dwBuffID, `number` nLevel)

* <h4 id="GetBuffTip">GetBuffTip</h4>

获取 Buff 提示文本。

 > (`string` szTip) GetBuffTip(`number` dwBuffID, `number` nLevel, `table` tExtraInfo)

* <h4 id="GetBuffAttrib">GetBuffAttrib</h4>

获取 Buff 属性。

 > (`table` tAttrib) GetBuffAttrib(`number` dwBuffID, `number` nLevel)
