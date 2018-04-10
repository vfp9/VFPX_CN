Visual FoxPro "Sedna"
=====================
Sedna 是一个用于 Visual FoxPRO 9.0 SP2 的类库、示例和插件的集合。

在安装 Sedna 前请先卸载它的 CTP 或 Beta 版。Sedna 默认情况下安装到 "Microsoft Visual FoxPro 9\Sedna" 目录。

这个安装包包括六个组成部分：VistaDialogs4COM、 Upsizing Wizard、Data Explorer、 NET4COM 和 MY for VFP 以及 DDEX for VFP 。下面的内容描述
了这些组件并提供如何使用它们的方法。

VistaDialogs4COM
================
VistaDialogs4COM 是一个可视的 COM 类集合，它封装了 Microsoft VistaBridgeLibrary 提供的函数。VistaDialogs4COM 为 Visual FoxPro 开发者提供
了访问 Windows Vista 任务对话框(TaskDialog) 和公共对话框的能力。

安装程序将安装 VistaDialogs4COM 集合、VistaBridgeLibrary 和其他需要的 DLL 文件，以及 VistaDialogs4COM 的源代码。一个 VFP 项目的示例也包含在
其中，用以展示 VistaDialogs4COM 的不同特性。

VistaDialogs4COM 文件夹下包含以下内容：
VistaDialogs4COM.dll -- 用于 COM 组件的 DLL ，它封装了 VistaBridgeLibrary.
VistaDialogs4COM -- 包含 VistaDialogs4COM 的 VB.NET 源代码
VFP Sample  -- 包含一个 VFP 示例项目，用以说明如何使用 VistaDialogs4COM

VistaDialogs4COM 的一些附加注意事项：
VistaLibrary4COM 需要 Windows Vista 。API 不能用于早期的 Windows 版本。VFP 示例文件夹下包含一些图片，来展示不同的对话框以及它们与早期版本对应
的对话框的区别。

SQL Server Upsizing Wizard
==========================
这是 Visual FoxPro 9.0 SP2 升迁向导的更新。Sedna 升迁向导将安装在 "Microsoft Visual FoxPro 9\Sedna\UpsizingWizard" 目录。从这个位置，你可
以运行 "UpsiziingWizard.app" 来执行新的向导。

这个更新包括：
*  更简洁的界面和效果
*  更简单的步骤
*  支持 bulk 插入来提高性能。
*  允许你指定连接为一个 DBC、DSN、一个已存在的连接，或者是一个新的连接字符串。
*  限制字段名使用 SQL 的保留关键字。
*  当调用生成器时，如果设置 lQuiet 设置为 .T.，将不显示界面。在升迁过程中，它使用 RAISEEVENT() ，所以用户可以看到进度显示。
*  升迁到 Microsoft SQL Server 2005 的性能改良。
*  在更新到 Varchar 时，使用 Trims 处理所有的字符串。
*  BlankDateValue 属性可用。它指定空的日期将作为 .NULL. 来更新。(原有的行为是设置它们为 01/01/1900)。
*  支持一个扩展的对象。这允许开发者针对更新过程的每个步骤设置钩子并改变其行为。另一个方式就是子类化引擎。
*  支持带空格的表名。
*  如果目标数据库已被创建，UpsizingWizard.APP 可以使用源文件名、路径、目标DB和一个布尔值作为参数来启动。

Database Explorer
=================
这是 Visual FoxPro 9.0 SP2 的数据浏览器的更新。它将被安装到 "Microsoft Visual FoxPro 9\Sedna\DataExplorer" 目录下。可以从这个位置运行新的 
'DataExplorer.app' 。

这个更新包括：
*  修复从数据浏览器拖动 VFP 表到表单的错误。
*  修复问题："从数据浏览器拖动 VFP 表/视图 到表单时不能设置 RecordSource 。"
*  修复当展开节点时，自由表无法显示它们的字段。
*  拖放操作现在遵从从 SQL Server 数据到 VFP 的字段映射。
*  允许排序应用到特定的对象，而不是所有对象。
*  针对本地视图显示 SQL ShowPlan 。
*  在查询结果中针对 VFP 的表/视图查询显示 ShowPlan 信息。
*  在选项对话框增加 Showplan 参数设置，应用于 showplan 特性。
*  Context menu item to launch the new UpsizingWizard.

NET4COM
=======
NET4COM 库是 .NET Framework 2.0 的子集的封装，它是一个 COM 类集合。.NET Framework 是命名空间和 API 的集合，它提供了一个全面的功能设置，使开发
者可以用其建立运行在 .NET 平台的应用程序。VFP 并没有一个 API 库，有些特性在 VFP 中并不存在或者很难在 Framework 中使用。NET4COM 提供了一个简单的
.NET Framework 子集，收集在 VFP 中不存在的，而又是常用的 API 来供 VFP 使用。

安装程序将安装 NET4COM 和示例文件到磁盘。安装程序也会注册 NET4COM.DLL 这个 COM 组件。NET4COM 文件夹包含以下内容：
*NET4COM.dll -- 针对 COM 组件的 DLL ，它是 .NET Framework 2.0 子集的封装。
*Source      -- 包含 NET4COM 的项目文件和源代码
*VFPSamples  -- 包含在 VFP 中使用 NET4COM 的示例
*VB6Samples  -- 包含在 VB6 中使用 NET4COM 的示例
*FFC         -- NET4COM 的 FFC 封状
示例程序展示了在 Visual FoxPro 和 Visual Basic 6.0 中 NET4COM 的使用。

MY for VFP
==========
MY 类库和 NET4COM 很相似。MY 是一个 Visual FoxPro 工具，它像 NET4COM 一样在更高的层次提供了常用的功能，以便很容易的来显示和浏览。
安装程序将安装 MY 类库到所选择的安装路径下的 "MY" 文件夹。要在 Visual FoxPro 中安装 MY ：
*  浏览 MY 文件夹
*  运行 MY.APP

MY 文件夹包含一个帮助文件：MY.CHM ，它包括 MY 的描述、安装和使用，以及包含针对不同的 API 的 API 引用。

DDEX for VFP
=============
它是 Visual Studio 2005 扩展(数据设计器扩展)，以便使用 Visual FoxPro 数据文件。安装 VFP DDEX ，同时也安装了 ADO .NET 数据驱动，它封装了 
VFPOLEDB 。

DDEX 允许 Visual Studio 使用 Visual FoxPro 数据源更好的工作。它将 VFP metadata 导入到 Visual Studio 的数据设计器中，然后可以执行常规的设计
任务，像从 Server Explorer 拖动表到 Visual Studio 设计器。

安装程序将拷贝 DDEX Provider、一个注册工具，以及源代码到 "Microsoft Visual FoxPro 9.0\DDEXProvider"目录。

在开始使用前，DDEXProvider 必须被安全。注意，DDEX 需要 Visual Studio 2005 。

注意：RegDDEX 必须以管理员身份运行。以管理员身份执行下面的命令。
要注册 DDEXProvider...

    更改目录到 Sedna 下的 'DDEXProvider'
    运行 RegDDEX

要撤消 DDEXProvider 注册...

    更改目录到 Sedna 下的 'DDEXProvider'
    运行 RegDDEX /u

一旦注册成功，在 Visual Studio 中可以在连接对话框中选择 Visual FoxPro 这样一个新的数据源类型。
