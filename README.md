# AdvancedConnect 插件的使用方法
- AdvancedConnect是[KeePass](http://keepass.info)密码管理器的插件，它可以打开应用程序。
- 只有WinSCP能自动登录，其他不能自动登录，无须此插件可在网址处输入程序路径即可打开。

## 要求
- Microsoft Windows的.NET/[Mono](http://www.mono-project.com/download/) 2.0或更高版本。
- Unix/Linux 的 [Mono](http://www.mono-project.com/download/) 2.0或更高版本。
- [KeePass](http://keepass.info) version 2.28或更高版本。

## 安装
- 下载[最新](https://github.com/aalbng/AdvancedConnectPlugin/releases/latest)版本。
- 将AdvancedConnectPlugin.plgx复制到KeePass/Plugins目录中并重新启动应用程序。

## 用法
- 该插件在**工具**菜单下添加了一个名为**Advanced Connect**的新菜单项。
- 使用**Options**对话框中的**Main**（主选项卡）来配置插件获取连接方法和连接选项字段的自定义字段（覆盖默认选项）。<br />
在windows操作系统上，本地远程桌面客户端没有选择通过命令行提供用户名和密码的选项。内置的rdp支持是提供这种功能的一个小小的解决方案。您必须配置KeaPASS连接字段（包含IP或主机名）、连接方法（例如rdp），并且可以设置附加参数（例如/w:1440 /h:900）。
- 使用**Options**对话框中的**Applications**（应用程序）选项卡配置连接应用程序。
在**路径**和**Commandline Options**（命令行选项）还支持KeePass的占位符和操作系统环境变量。
- 要使用**便携式配置**需要在**KeePass.exe**主程序文件夹下创建一个名为**AdvancedConnect.xml**的空文件。<br />
（如果有这个便携的\管理配置文件可用，则忽略默认配置%appdata%\Keepass\AdvancedConnect.xml）

## 范例
- **工具-Advanced Connect(高级连接)-Options(选项)**
- **Main(配置主选项)**
- **Settings（设置）**<br />
Connection method field(连接方法字段)：输入连接方法（可自定义输入，但必须和条目中字串字段的字段名相同）<br />
Connection options field(连接选项字段)：输入连接选项（可自定义输入，但必须和条目中字串字段的字段名相同）<br />
**Enable built in RDP suppot(启用内置的RDP支持)：（远程桌面协议，默认勾选）**<br />
Connection address field(连接地址字段)：输入连接地址（可自定义输入，但必须和条目中字串字段的字段名相同）<br />
Connection Method(连接方法)：输入rdp<br />
Additional RDP Parameter(额外的RDP参数)：输入/w:1440 /h:900<br />
<p align="center"><img src="https://github.com/1688aa/AdvancedConnectPlugin/blob/master/Doc/1%E9%85%8D%E7%BD%AE%E4%B8%BB%E9%80%89%E9%A1%B9.PNG"/></p>

- **Applications(添加应用程序)**<br />
Application Name(应用名称)：可自定义输入<br />
Method/Protocol(方法/协议)：输入打开程序，可自定义输入，但必须和条目中字串字段的字段名连接方法下的字段值相同<br />
Path(路径)：输入程序路径<br />
Commandline Options(命令行选项)
<p align="center"><img src="https://github.com/1688aa/AdvancedConnectPlugin/blob/master/Doc/2%E6%B7%BB%E5%8A%A0%E5%BA%94%E7%94%A8%E7%A8%8B%E5%BA%8F.PNG"/></p>
<p align="center"><img src="https://github.com/1688aa/AdvancedConnectPlugin/blob/master/Doc/2%E6%B7%BB%E5%8A%A0%E5%BA%94%E7%94%A8%E7%A8%8B%E5%BA%8F%EF%BC%88%E8%8B%B1%E6%96%87%EF%BC%89.png"/></p>

- **在字串字段添加自定义字段：**<br />
字段名输入连接方法字段值输入打开程序<br />
字段名输入连接选项字段值留空<br />
字段名输入连接地址字段值输入主机地址和端口或网址
<p align="center"><img src="https://github.com/1688aa/AdvancedConnectPlugin/blob/master/Doc/3%E5%9C%A8keepass%E6%9D%A1%E7%9B%AE%E4%B8%AD%E8%AE%BE%E7%BD%AE%E8%87%AA%E5%AE%9A%E4%B9%89%E5%AD%97%E6%AE%B5.PNG"/></p>

- **选择条目右键点击相应的程序就可以打开程序了**
- **只有WinSCP能自动登录，其他不能自动登录**
<p align="center"><img src="https://github.com/1688aa/AdvancedConnectPlugin/blob/master/Doc/4%E7%9B%B4%E6%8E%A5%E4%BB%8EKeePass%E5%90%AF%E5%8A%A8%E5%BA%94%E7%94%A8%E7%A8%8B%E5%BA%8F%EF%BC%88%E8%8B%B1%E6%96%87%EF%BC%89.png"/></p>

- **打开程序设置方法**<br />
**在Connection method field输入连接方法：** Application Name输入程序名称，Method/Protocol输入程序名称（多个条目共用一个值，右键会出现全部相同值的程序。一个条目也可建立多个程序），Path输入程序路径，在字串字段字段名输入连接方法值输入程序名称（多个条目共用一个值，右键会出现全部相同值的程序。一个条目也可建立多个程序）
- **打开WinSCP自动登录设置方法**<br />
**在Connection method field输入连接方法：** Connection address field输入连接地址，Application Name输入程序名称，Method/Protocol输入程序名称，Path输入程序路径，Commandline Options输入{USERNAME}:{PASSWORD}@{S:连接地址}，在字串字段字段名输入连接方法值输入程序名称，字段名输入连接地址值输入主机名和端口<br />
打开浏览器特定网址：Commandline Options输入{S:连接地址}

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
___
AdvancedConnect插件受QuickConnect启发
