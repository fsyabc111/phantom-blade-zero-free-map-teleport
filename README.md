# 影之刃零：地图自由传送

[English](README.en.md) · [下载 v1.0.1](https://github.com/fsyabc111/phantom-blade-zero-free-map-teleport/releases/tag/v1.0.1)

在安全野外打开普通地图，选择已经激活的铃铛即可直接传送。**无需持有穿行符、不弹出道具消耗确认、不消耗穿行符。**

本 Mod 保留游戏的战斗、空中、异常状态、剧情关键段、禁传区域、异空间和目的地区域限制，不会解锁未激活的铃铛。普通地图在铃铛附近也可以使用。

## 版本与兼容性

| 项目 | 已验证版本 |
| --- | --- |
| Mod | 1.0.1 |
| 游戏平台 | Steam，Windows |
| Steam App ID | 4115450 |
| 游戏 Build ID | **26266538** |

游戏更新后需要重新验证兼容性。与替换同一个 `JavaScript/UI/Widget/Map.js` 的地图 Mod 可能冲突。

## 安装

1. 完整退出游戏，并备份存档。
2. 在 Steam 中右键《影之刃零》→ **管理 → 浏览本地文件**，打开游戏根目录。
3. 从 [Releases](https://github.com/fsyabc111/phantom-blade-zero-free-map-teleport/releases/latest) 下载 `FreeMapTeleport-1.0.1-Steam-Build26266538.zip`。请下载该安装包，而不是 GitHub 自动生成的 Source code 压缩包。
4. 将压缩包中的 **`ProjectPBZ` 文件夹**解压到游戏根目录。
5. 确认以下三个文件都位于 `ProjectPBZ/Content/Paks/`，然后重新启动游戏。

```text
游戏根目录/
└─ ProjectPBZ/
   └─ Content/
      └─ Paks/
         ├─ ProjectPBZ-FreeMapTeleport_999_P.pak
         ├─ ProjectPBZ-FreeMapTeleport_999_P.utoc
         └─ ProjectPBZ-FreeMapTeleport_999_P.ucas
```

**三个文件必须一起保留，并放在 `Paks` 根目录。** 此版本游戏需要配套的 IoStore 容器；只有 `.pak` 文件时无法正常挂载。

进入安全野外，打开普通地图，选择一个已经激活的铃铛，执行游戏原有的传送操作即可。

## 卸载

退出游戏，仅删除以上三个名称包含 `FreeMapTeleport` 的文件，再重新启动游戏。保留游戏原版资源包。

## 验证情况

- 2026-10-30：确认重启后的游戏已加载修改后的地图脚本，玩家实测普通地图直接传送成功。
- 17 项脚本行为检查通过，覆盖零穿行符、保留状态/剧情/区域限制、连续点击和失败重试。
- 脚本语法、包内脚本回读、IoStore 容器标识及内容哈希检查通过。
- **跨区域传送与传送后读档尚未分别确认。**

## 下载校验与反馈

[downloads/SHA256SUMS.txt](downloads/SHA256SUMS.txt) 包含安装包和三个 Mod 文件的 SHA-256 校验值。仓库中也保留了一份 [安装包](downloads/FreeMapTeleport-1.0.1-Steam-Build26266538.zip)。

如遇问题，请在 [Issues](https://github.com/fsyabc111/phantom-blade-zero-free-map-teleport/issues) 中注明游戏 Build ID、Mod 版本、提示内容，以及是否安装了其他地图 Mod。

## 开发资料

- [修改差异](patches/Map.patch)
- [技术说明](docs/TECHNICAL.md)
- [更新记录](CHANGELOG.md)

这是非官方 Mod。仓库提供安装包、修改差异与说明；安装不需要 Python、Node.js 或额外 Mod 加载器。
