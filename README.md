# AdvancedConnect 插件的使用方法
AdvancedConnect是[KeePass](http://keepass.info)密码管理器的插件，它可以直接连接应用程序。


## 要求

- Microsoft Windows的.NET/[Mono](http://www.mono-project.com/download/) 2.0或更高版本。
- Unix/Linux 的 [Mono](http://www.mono-project.com/download/) 2.0或更高版本。
- [KeePass](http://keepass.info) version 2.28或更高版本。


## 安装

- 下载[最新](https://github.com/aalbng/AdvancedConnectPlugin/releases/latest)版本。
- 将AdvancedConnectPlugin.plgx复制到KeePass/Plugins目录中并重新启动应用程序。

## 用法

- 该插件在**工具**菜单下添加了一个名为**AdvancedConnect**的新菜单项。
- 使用**选项**对话框中的**Main**（主选项卡）来配置插件获取连接方法和连接选项字段的自定义字段（覆盖默认选项）。<br /><br />
在windows操作系统上，本地远程桌面客户端没有选择通过命令行提供用户名和密码的选项。内置的rdp支持是提供这种功能的一个小小的解决方案。您必须配置KeaPASS连接字段（包含IP或主机名）、连接方法（例如rdp），并且可以设置附加参数（例如/w:1440 /h:900）。<br />
- 使用**选项**对话框中的**Applications**（应用程序）选项卡配置连接应用程序。<br />
在**路径**和**Commandline Options**（命令行选项）还支持KeePass的占位符和操作系统环境变量。
- 要使用**便携式配置**需要在**KeePass.exe**旁边创建一个名为**AdvancedConnect.xml**的emtpy文件。<br />
（如果有一个便携的\管理配置文件可用，则忽略默认配置%appdata%\Keepass\AdvancedConnect.xml）


## 范例
- **配置主选项**<br />
**Settings（设置）**<br />
Connection method field（连接方法字段）：输入连接方法（可自定义输入，但必须和条目中字串字段的字段名相同）<br />
Connection options field（连接选项字段）：输入连接选项（可自定义输入，但必须和条目中字串字段的字段名相同）<br />
**Enable built in RDP suppot（启用内置的RDP支持）**<br />
Connection address field（连接地址字段）：输入连接地址（可自定义输入，但必须和条目中字串字段的字段名相同）<br />
Connection Method（连接方法）输入：rdp<br />
Additional RDP Parameter（额外的RDP参数）：输入/w:1440 /h:900<br />
<p align="center"><img src="https://github.com/1688pc/AdvancedConnectPlugin/blob/master/Doc/1%E9%85%8D%E7%BD%AE%E4%B8%BB%E9%80%89%E9%A1%B9.PNG"/></p>
- 添加应用程序
Application Name（应用名称）（可自定义输入）

<p align="center"><img src="https://github.com/aalbng/AdvancedConnectPlugin/blob/master/Doc/AdvancedConnect_Options-Applications.png"/></p>
- 在keepass条目中设置自定义字段
<p align="center"><img src="https://github.com/aalbng/AdvancedConnectPlugin/blob/master/Doc/Keepass_CustomFields.png"/></p>
- 直接从KeePass启动应用程序
<p align="center"><img src="https://github.com/aalbng/AdvancedConnectPlugin/blob/master/Doc/Keepass_ContexMenu.png"/></p>

## 安全

请注意，通过命令行启动应用程序可以在任务管理器中显示您的密码参数。

## 存储库

主存储库在[GitHub](https://github.com/aalbng/AdvancedConnectPlugin)上托管。

## 更新日志

有关详细信息，请参阅[日志](https://github.com/aalbng/AdvancedConnectPlugin/blob/master/AdvancedConnectPlugin/CHANGELOG.txt)文件。

## 下载

你可以从[这里](https://github.com/aalbng/AdvancedConnectPlugin/releases)获得所有的二进制文件

## 许可

这个存储库中的源代码是在Apache许可版本2.0许可下发布的。 <br />
有关详细信息，请参阅[许可](https://github.com/aalbng/AdvancedConnectPlugin/blob/master/AdvancedConnectPlugin/LICENSE.txt)文件。


____
AdvancedConnect插件受QuickConnect启发
