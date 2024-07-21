# ForgeHax
![](logo.png)

[![](https://img.shields.io/github/downloads/fr1kin/ForgeHax/total)](https://github.com/fr1kin/ForgeHax/releases)
[![](https://img.shields.io/matrix/forgehax:nerdsin.space.svg?label=%23forgehax%3Anerdsin.space&logo=matrix)](https://matrix.to/#/#forgehax:nerdsin.space)

[![buiawpkgew1/ForgeHax](https://gitee.com/awnioow/ForgeHax/widgets/widget_card.svg?colors=4183c4,ffffff,ffffff,e3e9ed,666666,9b9b9b)](https://gitee.com/awnioow/ForgeHax)
![构建状态](https://github.com/fr1kin/ForgeHax/actions/workflows/continuous_integration.yml/badge.svg?branch=1.19.4)

一个作为Forge模组运行在Minecraft上的作弊工具。

## 安装

1. 下载适用于相应ForgeHax Minecraft版本的最新版本的[Minecraft Forge](https://files.minecraftforge.net/)（如果你希望运行旧版本的ForgeHax，这是重要的）。
2. 通过访问[发布页面](https://github.com/fr1kin/ForgeHax/releases)下载最新的ForgeHax构建版本。
   不要安装包含`sources`的jar文件。那个jar文件包含源代码，并且没有编译。
3. 将ForgeHax jar文件放入`.minecraft/mods/`目录中。如果你希望按Minecraft版本组织文件，可以将它放在`.minecraft/mods/{mc.version}`目录下，其中`mc.version`是正在运行的Minecraft版本（例如：`.minecraft/mods/1.12.2`）。注意：这不会对1.13+版本有效！你只能将模组jar文件放在`/mods`文件夹中！
4. 使用Forge配置文件启动Minecraft。ForgeHax现在应该已经加载了。

## Wiki

如果你需要任何帮助，请在提交问题之前查看[ForgeHax Wiki](https://github.com/fr1kin/ForgeHax/wiki)。

## 构建
ForgeHax使用[Lombok](https://projectlombok.org/)来帮助消除样板代码并提供一些有用的功能，如扩展方法。如果你将ForgeHax导入到你的IDE中，请确保为你的IDE安装[Lombok插件](https://plugins.jetbrains.com/plugin/6317-lombok)。
否则，很多代码可能会被标记为错误，但实际上是正确的。

要构建ForgeHax，你只需要运行`./gradlew build`。确保使用JDK8运行gradle。JDK的新版本可能尚未支持javac插件。

#### 常见的构建问题

##### 当IntelliJ IDEA正在运行时，gradle构建失败/缺少符号错误

有时，当IntelliJ IDEA打开时，新的构建可能会失败。这是因为IDE对javac插件jar有一个文件句柄打开，并且由于某种原因，Lombok无法同时读取jar文件。结果就是Lombok会禁用自己，导致整个构建失败，出现“缺少符号”错误。

修复：关闭IntelliJ IDEA，并在终端中运行`./gradlew build`。问题可能是IntelliJ正在索引新添加的jar。所以一旦索引完成，你就可以使用IntelliJ构建，而没有任何问题。

## 常见问题解答

阅读[wiki](https://github.com/fr1kin/ForgeHax/wiki/FAQ)上的常见问题解答。

###### 感谢Rain#4705为Logo设计
