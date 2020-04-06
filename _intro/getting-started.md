# Getting Started

## 注意

在开始前，你需要对[SubModule.xml](../_xmldocs/submodule.md)文件有较深刻的了解，这一文件控制着MOD启用时，游戏加载的内容。

## 工具

### C\# IDE

* [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/) \(不用到C#的MOD就不必须\)

### 文本编辑器

任意文本编辑器均可，以下是推荐的三个。

* [Visual Studio Code](https://code.visualstudio.com/download)
* [Sublime Text](https://www.sublimetext.com/)  
* [Notepad++](https://notepad-plus-plus.org/downloads/)

## 制作无关 C\# 的MOD

你可以不通过C\#修改游戏的某些部分，包括场景(Scenes)，物品(Items)，文化(Cultures), 角色(Characters)，Gauntlet UIs等等。

## 制作用到 C\# 的MOD

本作的模块化MOD系统使得制作MOD比以前更加简单，并且使得制作更加复杂的MOD成为可能。

## 创建一个Module

本作中一个独立的MOD被称作Module，其必须的组成部分只有一个独立的文件夹以及`SubModule.xml`文件用于保存MOD的信息。

1. 在`Modules`文件夹中创建一个以MOD名字命名的文件夹。
2. 在这个MOD文件夹中创建`SubModule.xml`文件。[例子](../_xmldocs/submodule.md)，[详细文档](../_xmldocs/submodule.md)。

## 接下来

- 参考[目录结构](folder-structure.md)——了解你需要为你的MOD创建哪些目录。
- 参考[基础 C\# MOD](../_tutorials/basic-csharp-mod.md)——了解如何配置、构建并运行代码。
- 参考[Gauntlet UIs MOD](../_tutorials/modding-gauntlet-without-csharp.md)——了解如何修改Gauntlet UIs。\(不涉及C#\)

