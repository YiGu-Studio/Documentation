# Basic C\# Mod

## 简介

本教程会手把手教你如何制作一个基础的用到C#的MOD。这个MOD会在单机模式的标题画面增加一个叫`Message`的按钮。当你按下它，会在聊天框输出`Hello World`。

## 准备工作

#### 本教程中的模组名为`ExampleMod`.

### 配置你的模组\(SubModule.xml\)

1. 进入游戏根目录下的`Modules`目录。
2. 创建一个叫`ExampleMod`的新目录 (必须与第四步中的ID一致).
3. 创建一个叫`bin`的新目录，并在其中再创建一个叫`Win64_Shipping_Client`的目录(Modules\ExampleMod\bin\Win64_Shipping_Client)。
4. 创建`SubModule.xml`文件(Modules\ExampleMod\SubModule.xml)并将一下内容贴到文件中。

   ```xml
    <Module>
        <Name value="Example Mod"/>
        <Id value="ExampleMod"/>
        <Version value="v1.0.0"/>
        <SingleplayerModule value="true"/>
        <MultiplayerModule value="false"/>
        <DependedModules>
            <DependedModule Id="Native"/>
            <DependedModule Id="SandBoxCore"/>
            <DependedModule Id="Sandbox"/>
            <DependedModule Id="CustomBattle"/>
            <DependedModule Id="StoryMode" />
        </DependedModules>
        <SubModules>
            <SubModule>
                <Name value="ExampleMod"/>
                <DLLName value="ExampleMod.dll"/>
                <SubModuleClassType value="ExampleMod.MySubModule"/>
                <Tags>
                    <Tag key="DedicatedServerType" value="none" />
                    <Tag key="IsNoRenderModeElement" value="false" />
                </Tags>
            </SubModule>
        </SubModules>
        <Xmls/>
    </Module>
   ```

    **注意**: `MySubModule`将是[码代码 Programming](#programming)部分中我们要用到的类名。

5. 如果你用的是不同的名字，把上面的相关值改掉，以匹配Module/SubModule文件夹。
6. 打开启动器，此时你的MOD应该显示在`Singleplayer` &gt; `Mods`类中.

[点击](../_intro/folder-structure.md)了解Module目录结构

### 配置项目

首先，对于基础MOD来说\(比如修改或添加物品、场景等\)， **这一步不是必须的**。

1. 打开 Microsoft Visual Studio 并创建一个新项目。
2. 选择`.NET Framework`类库。
3. 给项目取名叫`ExampleMod` (如果你取别的名字，注意命名空间和 assembly name(不知道是啥) 别错了)，框架选`.NET Framework 4.7.2`。如果不能选这个框架, [点击下载](https://dotnet.microsoft.com/download/dotnet-framework/net472)\(开发者包\).
4. 现在你的项目配置好了, [设置你的构建路径](https://docs.microsoft.com/en-us/visualstudio/ide/how-to-change-the-build-output-directory?view=vs-2019)为`Modules/ExampleMod/bin/Win64_Shipping_Client`。
5. [引用](https://docs.microsoft.com/en-us/visualstudio/ide/how-to-add-or-remove-references-by-using-the-reference-manager?view=vs-2019)`游戏\bin\Win64_Shipping_Client`目录下名为`TaleWorlds.*`的所有DLL文件。同时引用各个官方MOD中所有名为`TaleWorlds.*`的DLL文件\(`Modules\ModuleName\bin\Win64_Shipping_Client`\)。

### 为你的项目DEBUG (可选)

1. 打开project properties，选择 `Debug` 标签.
2. 选择`启动外部程序 Start external program`选项并选中位于`bin\Win64_Shipping_Client`目录下的`Bannerlord.exe`。
3. 把工作目录设置为`bin\Win64_Shipping_Client`。
4. 添加如下运行参数\(把ExampleMod替换为你MOD的名字\):
   * `/singleplayer _MODULES_*Native*SandBox*SandBoxCore*StoryMode*CustomBattle*ExampleMod*_MODULES_`

## 编写代码

1. 在你的 VS 项目中创建一个新的类，命名为`MySubModule`并打开它。
2. 为你的类添加如下引用:

   ```csharp
    using TaleWorlds.Core;
    using TaleWorlds.Localization;
    using TaleWorlds.MountAndBlade;
   ```

3. 继承`MBSubModuleBase`类。
4. 重写继承自上述类的`OnSubModuleLoad()`方法。
5. 将以下代码加如你重写的方法:

   ```csharp
    Module.CurrentModule.AddInitialStateOption(new InitialStateOption("Message",
        new TextObject("Message", null),
        9990,
        () => { InformationManager.DisplayMessage(new InformationMessage("Hello World!")); },
        false));
   ```

6. 编辑你的项目并取人它被输出到`Modules\ExampleMod\bin\Win64_Shipping_Client`目录。
7. 打开游戏启动器并在`Singleplayer` &gt; `Mods`中找到你的MOD，启用它并启动游戏。
8. 在标题画面，你应该能看到`Message`按钮。当你点击它后，你应该能在屏幕左下角看到`Hello World`字样\(在对话框里\)。
9. 恭喜你完成了你的第一个骑砍2MOD！

