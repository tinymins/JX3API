[English](./CPath.md) | 中文

# CPath

## 函数

* <h4 id="LuaCPath_MakeDir">MakeDir</h4>
> CPath.MakeDir(pszDir) -> bOk

创建目录。

* <h4 id="LuaCPath_GetFolderList">GetFolderList</h4>
> CPath.GetFolderList(pszPath) -> tList

返回 `pszPath` 下的文件夹名列表（类数组 table）。

* <h4 id="LuaCPath_GetFileList">GetFileList</h4>
> CPath.GetFileList(pszPath) -> tList

返回 `pszPath` 下的文件名列表（类数组 table）。

* <h4 id="LuaCPath_Move">Move</h4>
> CPath.Move(pszPath, pszNewPath) -> bOk

移动/重命名文件或目录。

* <h4 id="LuaCPath_DelDir">DelDir</h4>
> CPath.DelDir(pszDir) -> bOk

递归删除目录。

* <h4 id="LuaCPath_RemovePathSpec">RemoveSpec</h4>
> CPath.RemoveSpec(pszPath) -> pszPath

移除路径最后一级（文件名/目录名）。

* <h4 id="LuaCPath_DelFile">DelFile</h4>
> CPath.DelFile(pszPath) -> bOk

删除文件。

* <h4 id="LuaCPath_GetFileName">GetFileName</h4>
> CPath.GetFileName(pszPath) -> szFileName

从路径中提取文件名。
