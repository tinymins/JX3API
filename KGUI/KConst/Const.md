English | [中文](./Const.zh-CN.md)

# Const

This module provides read-only constant tables.

## Tables

* <h4 id="LUA_CONST_LIST">LUA_CONST_LIST</h4>
> LUA_CONST_LIST

A global array-like table listing the names of all exported constant tables.

Notes:

- Each element is a string (the constant table name).
- The list is appended when constant tables are registered.

* <h4 id="WND_BASIC_STATUS">WND_BASIC_STATUS</h4>
> WND_BASIC_STATUS

Window basic status constants.

* <h4 id="ITEM_BASIC_STATUS">ITEM_BASIC_STATUS</h4>
> ITEM_BASIC_STATUS

Item basic status constants.

* <h4 id="WNDSIDE">WNDSIDE</h4>
> WNDSIDE

Window side constants.

* <h4 id="ALW">ALW</h4>
> ALW

Alignment/anchor-related constants.

* <h4 id="ALIGNMENT">ALIGNMENT</h4>
> ALIGNMENT

General alignment constants.

* <h4 id="ITEM_POSITION">ITEM_POSITION</h4>
> ITEM_POSITION

Item position constants.

* <h4 id="CURSOR">CURSOR</h4>
> CURSOR

Cursor state constants.

* <h4 id="MOVIE">MOVIE</h4>
> MOVIE

Movie-related constants.

* <h4 id="SOUND">SOUND</h4>
> SOUND

Sound-related constants.

* <h4 id="LOAD_LOGIN_REASON">LOAD_LOGIN_REASON</h4>
> LOAD_LOGIN_REASON

Login/loading reason constants.

* <h4 id="IMAGE">IMAGE</h4>
> IMAGE

Image type constants.

* <h4 id="FILE_OPEN_MODE">FILE_OPEN_MODE</h4>
> FILE_OPEN_MODE

File open mode constants.

* <h4 id="ANIMATE">ANIMATE</h4>
> ANIMATE

Animation type constants.

* <h4 id="D3DPT">D3DPT</h4>
> D3DPT

Primitive type constants.

* <h4 id="GEOMETRY_TYPE">GEOMETRY_TYPE</h4>
> GEOMETRY_TYPE

Geometry type constants.

* <h4 id="ANI_ACTION">ANI_ACTION</h4>
> ANI_ACTION

Animation action constants.

* <h4 id="ADDON_STATUS">ADDON_STATUS</h4>
> ADDON_STATUS

Addon status constants.

* <h4 id="BOX_STATE">BOX_STATE</h4>
> BOX_STATE

Box/widget state constants.

* <h4 id="ITEM_EVENT">ITEM_EVENT</h4>
> ITEM_EVENT

Item event constants.

* <h4 id="SQLITE3">SQLITE3</h4>
> SQLITE3

SQLite3-related constants.

* <h4 id="UNQLITE">UNQLITE</h4>
> UNQLITE

UnQLite-related constants.

* <h4 id="BUTTON_STATUS">BUTTON_STATUS</h4>
> BUTTON_STATUS

Button status constants.

* <h4 id="BUTTON_RUN_STATUS">BUTTON_RUN_STATUS</h4>
> BUTTON_RUN_STATUS

Button runtime status constants.

* <h4 id="CHECKBOX_STATUS">CHECKBOX_STATUS</h4>
> CHECKBOX_STATUS

Checkbox status constants.

* <h4 id="CHECKBOX_RUN_STATUS">CHECKBOX_RUN_STATUS</h4>
> CHECKBOX_RUN_STATUS

Checkbox runtime status constants.

* <h4 id="CODE_PAGE">CODE_PAGE</h4>
> CODE_PAGE

Code page constants.

* <h4 id="WNDEVENT_FIRETYPE">WNDEVENT_FIRETYPE</h4>
> WNDEVENT_FIRETYPE

Window event firing-type constants.

* <h4 id="YG_DIRECTION">YG_DIRECTION</h4>
> YG_DIRECTION

Yoga layout direction constants.

* <h4 id="YG_FLEX_DIRECTION">YG_FLEX_DIRECTION</h4>
> YG_FLEX_DIRECTION

Yoga flex direction constants.

* <h4 id="YG_FLEX_WRAP">YG_FLEX_WRAP</h4>
> YG_FLEX_WRAP

Yoga flex wrap constants.

* <h4 id="YG_JUSTIFY">YG_JUSTIFY</h4>
> YG_JUSTIFY

Yoga justify constants.

* <h4 id="YG_ALIGN">YG_ALIGN</h4>
> YG_ALIGN

Yoga align constants.

* <h4 id="GESTURE_STATE">GESTURE_STATE</h4>
> GESTURE_STATE

Gesture state constants.

## Game Constants

The following constants are exported from the game API for addon use:

* <h4 id="CAMP">CAMP</h4>
> CAMP

Camp type constants.

* <h4 id="GLOBAL">GLOBAL</h4>
> GLOBAL

Global game constants.

* <h4 id="FORCE_TYPE">FORCE_TYPE</h4>
> FORCE_TYPE

Force (faction) type constants.

* <h4 id="KUNGFU_TYPE">KUNGFU_TYPE</h4>
> KUNGFU_TYPE

Kungfu (martial arts style) type constants.

* <h4 id="ITEM_TABLE_TYPE">ITEM_TABLE_TYPE</h4>
> ITEM_TABLE_TYPE

Item table type constants.

* <h4 id="EQUIPMENT_REPRESENT">EQUIPMENT_REPRESENT</h4>
> EQUIPMENT_REPRESENT

Equipment representation constants.

* <h4 id="INVENTORY_INDEX">INVENTORY_INDEX</h4>
> INVENTORY_INDEX

Inventory index constants (equipment slots, bags, etc.).

* <h4 id="TARGET">TARGET</h4>
> TARGET

Target type constants.

* <h4 id="ITEM_GENRE">ITEM_GENRE</h4>
> ITEM_GENRE

Item genre constants.

* <h4 id="ITEM_BIND">ITEM_BIND</h4>
> ITEM_BIND

Item bind type constants.

* <h4 id="PLAYER_TALK_CHANNEL">PLAYER_TALK_CHANNEL</h4>
> PLAYER_TALK_CHANNEL

Player chat channel constants.

* <h4 id="TONG_OPERATION">TONG_OPERATION</h4>
> TONG_OPERATION

Guild operation type constants.

* <h4 id="MOVETYPE">MOVETYPE</h4>
> MOVETYPE

Character move type constants.

* <h4 id="ROLE_TYPE">ROLE_TYPE</h4>
> ROLE_TYPE

Role type constants (player, NPC, doodad).

* <h4 id="CHARACTER_TYPE">CHARACTER_TYPE</h4>
> CHARACTER_TYPE

Character type constants.

* <h4 id="NPC_KIND">NPC_KIND</h4>
> NPC_KIND

NPC kind constants.

* <h4 id="DOODAD_KIND">DOODAD_KIND</h4>
> DOODAD_KIND

Doodad kind constants.

## Behavior

All constant tables are read-only:

- Reading values uses normal indexing, e.g. `CODE_PAGE.UTF8`.
- Writing will be rejected and logged.
- The metatable is protected.
