# LiveFakeName

直播也要大大方方开！

适配 DalamudCN API Level 15、`.NET 10` 的小队姓名本地伪装插件。

## 在线安装

在 DalamudCN 设置的“自定义插件仓库”中添加：

```text
https://raw.githubusercontent.com/Alittlerecallinglittlebrother/FAKE-Name-A/main/repo.json
```

保存后在插件安装器中搜索 `LiveFakeName` 并安装，无需下载本地 DLL。

## 功能

- `/aklname` 打开或关闭设置窗口
- 按小队列表实际显示顺序配置 1–8 号成员别名
- 同时改写本机小队列表与八名小队成员的头顶姓名
- 仅按小队成员实体 ID 匹配，不改写其他玩家、NPC、服务器或其他玩家客户端的数据
- 功能关闭或插件卸载时恢复本插件改写的姓名
- 持久化保存启用状态和八个别名

## 构建

在 PowerShell 中进入本目录并执行：

```powershell
.\build.ps1
```

构建输出位于：

```text
DalamudCNStarter\bin\x64\Debug\
```

## 在游戏内加载

1. 启动带 DalamudCN 的游戏。
2. 输入 `/xlsettings`，打开“测试版”或“实验性功能”页面。
3. 将构建输出中的 `DalamudCNStarter.dll` 完整路径加入开发插件位置。
4. 输入 `/xlplugins`，在开发插件页面启用 `LiveFakeName`。
5. 输入 `/aklname` 验证窗口与配置。

游戏内加载测试需要 FF14 客户端正在运行；命令行构建不需要启动游戏。
