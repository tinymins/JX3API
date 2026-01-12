English | [中文](./CPath.zh-CN.md)

# CPath

## Functions

* <h4 id="LuaCPath_MakeDir">MakeDir</h4>
> CPath.MakeDir(pszDir) -> bOk

Creates a directory.

* <h4 id="LuaCPath_GetFolderList">GetFolderList</h4>
> CPath.GetFolderList(pszPath) -> tList

Returns an array-like table of folder names under `pszPath`.

* <h4 id="LuaCPath_GetFileList">GetFileList</h4>
> CPath.GetFileList(pszPath) -> tList

Returns an array-like table of file names under `pszPath`.

* <h4 id="LuaCPath_Move">Move</h4>
> CPath.Move(pszPath, pszNewPath) -> bOk

Moves/renames a file or directory.

* <h4 id="LuaCPath_DelDir">DelDir</h4>
> CPath.DelDir(pszDir) -> bOk

Deletes a directory recursively.

* <h4 id="LuaCPath_RemovePathSpec">RemoveSpec</h4>
> CPath.RemoveSpec(pszPath) -> pszPath

Removes the last path component.

* <h4 id="LuaCPath_DelFile">DelFile</h4>
> CPath.DelFile(pszPath) -> bOk

Deletes a file.

* <h4 id="LuaCPath_GetFileName">GetFileName</h4>
> CPath.GetFileName(pszPath) -> szFileName

Extracts file name from a path.
