# AdvancedConnect 插件的使用方法
AdvancedConnect 是 [KeePass](http://keepass.info) 密码管理器的插件，它可以直接连接应用程序。


## 要求

- Microsoft Windows 的 .NET/[Mono](http://www.mono-project.com/download/) 2.0 或更高版本。
- Unix/Linux 的 [Mono](http://www.mono-project.com/download/) 2.0 或更高版本。
- [KeePass](http://keepass.info) version 2.28 或更高版本。


## 安装

- 下载 [最新](https://github.com/aalbng/AdvancedConnectPlugin/releases/latest) 版本。
- 将 AdvancedConnectPlugin.plgx 复制到 KeePass/Plugins 目录中并重新启动应用程序。

## 用法

- 该插件在**工具**菜单下添加了一个名为 **AdvancedConnect** 的新菜单项。
- 使用**选项**对话框中的**主选项卡**来配置插件获取连接方法和连接选项字段的自定义字段（覆盖默认选项）。 <br /><br />
在 windows 操作系统上，本地远程桌面客户端没有选择通过命令行提供用户名和密码的选项。内置的 rdp 支持是提供这种功能的一个小小的解决方案。您必须配置 KeaPASS 连接字段（包含IP或主机名）、连接方法（例如rdp），并且可以设置附加参数（例如/w:1440 /h:900）。<br />
- 使用**选项**对话框中的**Applications****（应用程序）**选项卡配置连接应用程序。 <br />
The **Path** and **Commandline Options** column is also supporting keepass placeholders and OS environment variables.
- To use a **portable configuration** you have to create an emtpy file named **AdvancedConnect.xml** next to **KeePass.exe**. <br />
(If a portable\admin configuration file is available, the default configuration *%appdata%\Keepass\AdvancedConnect.xml* will be ignored)


## Example
- Configure main options
<p align="center"><img src="https://github.com/aalbng/AdvancedConnectPlugin/blob/master/Doc/AdvancedConnect_Options-Main.png"/></p>
- Add your applications
<p align="center"><img src="https://github.com/aalbng/AdvancedConnectPlugin/blob/master/Doc/AdvancedConnect_Options-Applications.png"/></p>
- Set custom fields in keepass entries
<p align="center"><img src="https://github.com/aalbng/AdvancedConnectPlugin/blob/master/Doc/Keepass_CustomFields.png"/></p>
- Start your applications directly from keepass
<p align="center"><img src="https://github.com/aalbng/AdvancedConnectPlugin/blob/master/Doc/Keepass_ContexMenu.png"/></p>

## Security

Please take note that launching applications via command-line can expose your password arguments in the taskmanager.

## Repository

The main repository is hosted on [GitHub](https://github.com/aalbng/AdvancedConnectPlugin).

## Changelog

See [CHANGELOG](https://github.com/aalbng/AdvancedConnectPlugin/blob/master/AdvancedConnectPlugin/CHANGELOG.txt) file for details.

## Download

You can get all binaries from [here](https://github.com/aalbng/AdvancedConnectPlugin/releases).

## License

The source code in this repository is released under the Apache License, Version 2.0 license. <br />
See the [LICENSE](https://github.com/aalbng/AdvancedConnectPlugin/blob/master/AdvancedConnectPlugin/LICENSE.txt) file for details.


____
The AdvancedConnect plugin is inspired by [QuickConnect](https://github.com/cristianst85/QuickConnectPlugin) 
