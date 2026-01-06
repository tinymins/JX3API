# WndPage

`WndPage`'s metatable is registered as: `KScriptLoader::RegisterMetaTable(L, "WndPage", s_aWndWindowMetaTable, s_aWndWindowMetaTable, ...)`.

That means it only has the base `WndWindow` APIs (no additional extended APIs).

Please refer to:

- [KGUI/KWnd/WndWindow.md](./WndWindow.md)
