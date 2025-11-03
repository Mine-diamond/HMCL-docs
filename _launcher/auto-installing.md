---
title: 自动安装与模组下载简介
date: 2025-11-02 09:06:30 +0800
author: asdqp233
contributors:
  - Mine-diamond
---

要在 Minecraft 中安装模组，首先需要安装“模组加载器”（如 NeoForge 或 Fabric），然后再添加你想要的模组。HMCL 对这两个步骤都提供了完善且便捷的支持。

在安装前最重要的是确保兼容性，请牢记以下关键原则：

- 通常情况下，一个游戏实例只能安装一种模组加载器。
- 你下载的模组必须同时兼容对应的游戏版本（例如 1.20.4）和模组加载器（例如 Fabric）。

简单来说安装模组可分为三个步骤，本指南将带你依次完成：

1. 启用版本隔离：为模组创建一个独立、干净的游戏环境
2. 安装模组加载器（如 Forge 或 Fabric）
3. 安装模组

## 启用版本隔离

在安装模组之前，必须先启用版本隔离以避免不同实例之间的模组相互干扰，详细说明请参见[全局版本隔离][~/launcher/isolation]。

## 安装模组加载器

### 模组加载器简介

在安装模组之前，先了解几种常见的模组加载器。

`Forge`, `NeoForge`, `Fabric`, `Quilt`, `Cleanroom`, `LiteLoader` 是目前常见的六种模组加载器。

`Fabric API` 与 `QSL/QFAPI` 分别是 `Fabric` 与 `Quilt` 的官方 API（本质上也是模组），它们为其它模组提供运行所需的基础功能。

| 模组加载器 | 简介 | 游戏版本 |
| :--------: | ---- | :------: |
| ![Forge icon][~/assets/auto-installing/forge]<br>Forge | 历史悠久且功能完善的模组加载器，拥有最庞大的模组生态。推荐在 1.21 之前的版本使用。 | 1.5.2+ |
| ![NeoForge icon][~/assets/auto-installing/neoforge]<br>NeoForge | Forge 的社区分支在 1.20.1 后独立发展，性能与兼容性更佳，推荐在 1.21 及以后的版本使用。 | 1.20.1+ |
| ![Fabric icon][~/assets/auto-installing/fabric]<br>Fabric | 轻量级模组加载器，适合安装性能优化类或生存增强类模组。 | 1.16.3+ |
| ![Quilt icon][~/assets/auto-installing/quilt]<br>Quilt | Fabric 的社区分支，兼顾轻量的同时还提供更多实验性特性。 | 1.16.3+ |
| ![Fabric api icon][~/assets/auto-installing/fabric]<br>Fabric API<br>![QSL/QFAPI icon][~/assets/auto-installing/quilt]<br>QSL/QFAPI | Fabric 与 Quilt 的功能扩展 API，提供基础接口支持，是大多数此类模组的依赖前置。 | Fabric API<br>1.16.3+<br>QSL/QFAPI<br>1.18.2 - 1.21 |
| ![Cleanroom icon][~/assets/auto-installing/cleanroom]<br>Cleanroom | 专为 1.12.2 版本设计的 Forge 改进版。 | 1.12.2 |
| ![LiteLoader icon][~/assets/auto-installing/chicken]<br>LiteLoader | 轻量级模组加载器，曾作为 Forge 的简化替代方案，现已停止维护。 | 1.5.2 - 1.12.2 |

**兼容性说明：**

- LiteLoader 与 Forge 可以相互兼容，但在部分版本中（例如较新的 Forge 与较旧的 LiteLoader）可能存在兼容性问题，无法同时正常使用。
- 其余模组加载器之间基本互不兼容，无法同时使用。

**补充说明：**  

有大量的 Fabric 与 Quilt 模组依赖 Fabric API 或 QSL / QFAPI 因此在安装 Fabric 或 Quilt 加载器时，若无特殊原因强烈建议同时安装相应的 API 模组。

### 安装新实例时安装模组加载器

当你在安装新的游戏客户端时候, 会看到其中有该版本支持的模组加载器安装选项：

![AutoInstaller_ModLoader][~/assets/auto-installing/AutoInstaller_ModLoader]

- 点击你想要的加载器（如 Fabric）。
- 在弹出的版本选择页面，若无特殊需求，**选择最新稳定版**（通常是第一个）。
- 如果你选择 `Fabric` 或 `Quilt`，最好同时安装`Fabric API` 或 `QSL/QFAPI`。
- 点击「安装」即可。

### 为已有实例安装或更换模组加载器

如果你想为已安装好的纯净版游戏添加加载器，或者更换、更新加载器版本：

1.  在 HMCL 主界面，点击「实例管理」，然后选择你想要修改的游戏实例。
2.  在左侧菜单中，点击「自动安装」。

![Auto_Install_Page][~/assets/auto-installing/Auto_Install_Page]

- **安装**：点击你想要的加载器图标（如 Forge），选择版本（推荐最新版），然后点击安装。
- **更新**：点击已安装的加载器，选择一个更新的版本，然后点击安装。
- **删除**：点击加载器右侧的「X」按钮即可删除。
- **更换**：先删除旧的加载器，再安装新的。

> **注意**：此处的自动安装页面不支持安装 `Fabric API` 或 `QSL/QFAPI`。请将它们当作普通模组进行安装。


## 安装模组

安装好加载器后，就可以开始添加模组了。你可以在下列网站获取模组信息，并在 HMCL 内下载和安装：
- [MC 百科](https://www.mcmod.cn/) - 中文社区，资料详尽。
- [CurseForge](https://www.curseforge.com/minecraft/search?class=mc-mods) - 最大的模组发布站之一。
- [Modrinth](https://modrinth.com/mods) - 新兴的现代化模组发布站。

在安装任何模组前，请先确认三件事：
1.  **游戏版本**：模组是否支持你当前的游戏版本？(例如, 1.20.4)
2.  **加载器类型**：模组是给 Forge、Fabric 还是其它模组加载器用的？
3.  **前置模组**：模组是否需要其他模组作为前置？（模组页面通常会说明）

### 自动安装 (推荐)

HMCL 内置了 CurseForge 和 Modrinth 的搜索和下载功能，非常方便。

1.  在 HMCL 主界面，点击「下载」->「模组」。
2.  在搜索框输入模组名（支持中英文），然后点击搜索。如果搜不到，可以尝试切换右上角的下载源。
3.  点击你想要的模组，进入版本列表页面。
4.  根据**游戏版本**和**加载器**，找到你需要的版本，点击并选择「安装到当前实例」。
5.  如果该模组有前置，HMCL 会自动提示，请先安装所有前置模组（但是请不要重复安装前置模组）。

注：点击模组下载页面 上方的蓝色的链接可以到对应的网站查看模组的信息，这会告诉你模组的功能和有可能会提示你一些注意事项

**注意: 请查看你要下载的模组是否正常你要安装的游戏版本以及模组加载器，否则模组无法被正常加载!**

![AddingModAutomatically][~/assets/auto-installing/AutoInstaller_ModAutoAdding]

### 手动安装

当你在网站或其它位置手动下载了模组文件，你可以参照以下步骤完成安装：

一般的 Mod 文件后缀为 `jar` 或者 `litemod`，请确认后缀是正确的。其中`jar`为大多数模组加载器支持的格式，`litemod`仅`LiteLoader`支持。  

#### 通过模组管理页面

1.  进入「实例管理」-> 选择你的游戏实例 ->「模组管理」。
2.  点击「添加模组」并选择你的模组文件，或直接将文件拖拽到窗口内即可。  

#### 通过模组文件夹安装

1.  进入「实例管理」-> 选择你的游戏实例 ->「浏览」->「模组文件夹」。
2.  这会打开该实例的 `mods` 文件夹。
3.  将你下载的 `.jar` 模组文件复制或移动到这个文件夹里。
    （如果 `mods` 文件夹不存在，请自行创建一个。）

![AddingModManually][~/assets/auto-installing/AutoInstaller_ModManualAdding]

### 安装OptiFine 或其它光影模组

光影的安装方式略有不同，请参考专门的指南 [光影安装][~/launcher/shader]

## 安装 Mod 后游戏报错/无法启动

造成游戏报错的原因有很多, 比如 Mod 之间不兼容, Fabric API 的版本过高, 缺少前置 Mod 等等。

**第一步：基础检查（最常见问题）**
- **查看 HMCL 错误报告**：新版 HMCL 会直接提示大部分常见错误，这是你的首选信息来源。
- **检查兼容性**：确认模组版本、游戏版本、模组加载器三者是否匹配。
- **检查前置模组**：是否忘记安装必要的API（如 Fabric API）或其他前置模组？

**第二步：自己排查**
- **使用“二分法”**：在“模组管理”页面，先禁用一半的模组，看游戏能否启动或出错。如果可以，说明问题出在被禁用的那一半里。不断重复此过程，直到找到引发问题的具体模组。
- **查看日志文件**：如果你有能力，可以自行查看游戏日志来定位问题。

**第三步：有效求助**
如果无法自行解决，你需要向社区求助。但请记住，一个有效的求助包含**完整的日志文件**。

**如何正确求助**：
1. 在游戏崩溃后，点击 HMCL 弹出的错误窗口上的「**导出游戏日志**」按钮，它会生成一个 `minecraft-exported-crash-info-时间戳.zip` 文件。
2. 带着**这个文件**去社区、论坛或群里提问，并具体描述你遇到的问题。

> **重要**：对于向他人求助，千万不要只截图，不要只说“游戏出错怎么办”这种及其笼统的话语。**没有日志，谁也帮不了你。**

![CrashReportPage][~/assets/auto-installing/Crash_Report_Page]

<!--{% comment %}-->
[~/launcher/shader]: /_launcher/shader.md
[~/launcher/isolation]: /_launcher/isolation.md
[~/assets/auto-installing/forge]: /assets/img/docs/auto-installing/forge.png
[~/assets/auto-installing/neoforge]: /assets/img/docs/auto-installing/neoforge.png
[~/assets/auto-installing/fabric]: /assets/img/docs/auto-installing/fabric.png
[~/assets/auto-installing/quilt]: /assets/img/docs/auto-installing/quilt.png
[~/assets/auto-installing/cleanroom]: /assets/img/docs/auto-installing/cleanroom.png
[~/assets/auto-installing/chicken]: /assets/img/docs/auto-installing/chicken.png
[~/assets/auto-installing/Auto_Install_Page]: /assets/img/docs/auto-installing/Auto_Install_Page.png
[~/assets/auto-installing/Crash_Report_Page]: /assets/img/docs/auto-installing/Crash_Report_Page.png
[~/assets/auto-installing/AutoInstaller_ModLoader]: /assets/img/docs/auto-installing/AutoInstaller_ModLoader.png
[~/assets/auto-installing/AutoInstaller_ModAutoAdding]: /assets/img/docs/auto-installing/AutoInstaller_ModAutoAdding.png
[~/assets/auto-installing/AutoInstaller_ModManualAdding]: /assets/img/docs/auto-installing/AutoInstaller_ModManualAdding.png
<!--{% endcomment %}--{{'>'}}
[~/launcher/shader]: {% link _launcher/shader.md %}
[~/launcher/isolation]: {% link _launcher/isolation.md %}
[~/assets/auto-installing/forge]: {% link /assets/img/docs/auto-installing/forge.png %}
[~/assets/auto-installing/neoforge]: {% link /assets/img/docs/auto-installing/neoforge.png %}
[~/assets/auto-installing/fabric]: {% link /assets/img/docs/auto-installing/fabric.png %}
[~/assets/auto-installing/quilt]: {% link /assets/img/docs/auto-installing/quilt.png %}
[~/assets/auto-installing/cleanroom]: {% link /assets/img/docs/auto-installing/cleanroom.png %}
[~/assets/auto-installing/chicken]: {% link /assets/img/docs/auto-installing/chicken.png %}
[~/assets/auto-installing/Auto_Install_Page]: {% link /assets/img/docs/auto-installing/Auto_Install_Page.png %}
[~/assets/auto-installing/Crash_Report_Page]: {% link /assets/img/docs/auto-installing/Crash_Report_Page.png %}
[~/assets/auto-installing/AutoInstaller_ModLoader]: {% link /assets/img/docs/auto-installing/AutoInstaller_ModLoader.png %}
[~/assets/auto-installing/AutoInstaller_ModAutoAdding]: {% link /assets/img/docs/auto-installing/AutoInstaller_ModAutoAdding.png %}
[~/assets/auto-installing/AutoInstaller_ModManualAdding]: {% link /assets/img/docs/auto-installing/AutoInstaller_ModManualAdding.png %}
<!---->
