[English](./Const.md) | 中文

# Const

该模块提供一组只读的常量表。

## 表

* <h4 id="LUA_CONST_LIST">LUA_CONST_LIST</h4>
> LUA_CONST_LIST

全局的类数组 table，列出所有导出的常量表名称。

说明：

- 每个元素都是 string（常量表名）。
- 注册常量表时会把名称追加到该列表。

* <h4 id="WND_BASIC_STATUS">WND_BASIC_STATUS</h4>
> WND_BASIC_STATUS

窗口基础状态常量。

* <h4 id="ITEM_BASIC_STATUS">ITEM_BASIC_STATUS</h4>
> ITEM_BASIC_STATUS

控件/物件基础状态常量。

* <h4 id="WNDSIDE">WNDSIDE</h4>
> WNDSIDE

窗口边/方向相关常量。

* <h4 id="ALW">ALW</h4>
> ALW

对齐/锚点相关常量。

* <h4 id="ALIGNMENT">ALIGNMENT</h4>
> ALIGNMENT

通用对齐常量。

* <h4 id="ITEM_POSITION">ITEM_POSITION</h4>
> ITEM_POSITION

控件/物件位置常量。

* <h4 id="CURSOR">CURSOR</h4>
> CURSOR

鼠标指针状态常量。

* <h4 id="MOVIE">MOVIE</h4>
> MOVIE

Movie 相关常量。

* <h4 id="SOUND">SOUND</h4>
> SOUND

声音相关常量。

* <h4 id="LOAD_LOGIN_REASON">LOAD_LOGIN_REASON</h4>
> LOAD_LOGIN_REASON

登录/加载原因常量。

* <h4 id="IMAGE">IMAGE</h4>
> IMAGE

图片类型常量。

* <h4 id="FILE_OPEN_MODE">FILE_OPEN_MODE</h4>
> FILE_OPEN_MODE

文件打开模式常量。

* <h4 id="ANIMATE">ANIMATE</h4>
> ANIMATE

动画类型常量。

* <h4 id="D3DPT">D3DPT</h4>
> D3DPT

图元类型常量。

* <h4 id="GEOMETRY_TYPE">GEOMETRY_TYPE</h4>
> GEOMETRY_TYPE

几何类型常量。

* <h4 id="ANI_ACTION">ANI_ACTION</h4>
> ANI_ACTION

动画动作常量。

* <h4 id="ADDON_STATUS">ADDON_STATUS</h4>
> ADDON_STATUS

Addon 状态常量。

* <h4 id="BOX_STATE">BOX_STATE</h4>
> BOX_STATE

Box/容器状态常量。

* <h4 id="ITEM_EVENT">ITEM_EVENT</h4>
> ITEM_EVENT

控件/物件事件常量。

* <h4 id="SQLITE3">SQLITE3</h4>
> SQLITE3

SQLite3 相关常量。

* <h4 id="UNQLITE">UNQLITE</h4>
> UNQLITE

UnQLite 相关常量。

* <h4 id="BUTTON_STATUS">BUTTON_STATUS</h4>
> BUTTON_STATUS

按钮状态常量。

* <h4 id="BUTTON_RUN_STATUS">BUTTON_RUN_STATUS</h4>
> BUTTON_RUN_STATUS

按钮运行时状态常量。

* <h4 id="CHECKBOX_STATUS">CHECKBOX_STATUS</h4>
> CHECKBOX_STATUS

复选框状态常量。

* <h4 id="CHECKBOX_RUN_STATUS">CHECKBOX_RUN_STATUS</h4>
> CHECKBOX_RUN_STATUS

复选框运行时状态常量。

* <h4 id="CODE_PAGE">CODE_PAGE</h4>
> CODE_PAGE

代码页常量。

* <h4 id="WNDEVENT_FIRETYPE">WNDEVENT_FIRETYPE</h4>
> WNDEVENT_FIRETYPE

窗口事件触发方式常量。

* <h4 id="YG_DIRECTION">YG_DIRECTION</h4>
> YG_DIRECTION

Yoga 布局方向常量。

* <h4 id="YG_FLEX_DIRECTION">YG_FLEX_DIRECTION</h4>
> YG_FLEX_DIRECTION

Yoga flex direction 常量。

* <h4 id="YG_FLEX_WRAP">YG_FLEX_WRAP</h4>
> YG_FLEX_WRAP

Yoga flex wrap 常量。

* <h4 id="YG_JUSTIFY">YG_JUSTIFY</h4>
> YG_JUSTIFY

Yoga justify 常量。

* <h4 id="YG_ALIGN">YG_ALIGN</h4>
> YG_ALIGN

Yoga align 常量。

* <h4 id="GESTURE_STATE">GESTURE_STATE</h4>
> GESTURE_STATE

手势状态常量。

## 游戏常量

以下常量从游戏 API 导出供插件使用：

* <h4 id="CAMP">CAMP</h4>
> CAMP

阵营类型常量。

* <h4 id="GLOBAL">GLOBAL</h4>
> GLOBAL

全局游戏常量。

* <h4 id="FORCE_TYPE">FORCE_TYPE</h4>
> FORCE_TYPE

门派类型常量。

* <h4 id="KUNGFU_TYPE">KUNGFU_TYPE</h4>
> KUNGFU_TYPE

心法类型常量。

* <h4 id="ITEM_TABLE_TYPE">ITEM_TABLE_TYPE</h4>
> ITEM_TABLE_TYPE

物品表类型常量。

* <h4 id="EQUIPMENT_REPRESENT">EQUIPMENT_REPRESENT</h4>
> EQUIPMENT_REPRESENT

装备展示常量。

* <h4 id="INVENTORY_INDEX">INVENTORY_INDEX</h4>
> INVENTORY_INDEX

背包索引常量（装备栏位、背包等）。

* <h4 id="TARGET">TARGET</h4>
> TARGET

目标类型常量。

* <h4 id="ITEM_GENRE">ITEM_GENRE</h4>
> ITEM_GENRE

物品类别常量。

* <h4 id="ITEM_BIND">ITEM_BIND</h4>
> ITEM_BIND

物品绑定类型常量。

* <h4 id="PLAYER_TALK_CHANNEL">PLAYER_TALK_CHANNEL</h4>
> PLAYER_TALK_CHANNEL

玩家聊天频道常量。

* <h4 id="TONG_OPERATION">TONG_OPERATION</h4>
> TONG_OPERATION

帮会操作类型常量。

* <h4 id="MOVETYPE">MOVETYPE</h4>
> MOVETYPE

角色移动类型常量。

* <h4 id="ROLE_TYPE">ROLE_TYPE</h4>
> ROLE_TYPE

角色类型常量（玩家、NPC、Doodad）。

* <h4 id="CHARACTER_TYPE">CHARACTER_TYPE</h4>
> CHARACTER_TYPE

角色类型常量。

* <h4 id="NPC_KIND">NPC_KIND</h4>
> NPC_KIND

NPC 种类常量。

* <h4 id="DOODAD_KIND">DOODAD_KIND</h4>
> DOODAD_KIND

Doodad 种类常量。

## 行为

所有常量表都是只读的：

- 正常通过索引读取，例如 `CODE_PAGE.UTF8`。
- 试图写入会被拒绝并记录日志。
- 元表被保护，脚本侧不能修改。
