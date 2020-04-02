# 基本 C\# Mod

## 介绍

本文档旨在一步一步教你如何创建一个简单的 C\# Mod。这个Mod将会在单人模式的标题页面增加一个叫做 `消息` 的按钮。当点击按钮的时候，将会在聊天界面输出 `Hello World`。

## 准备

### 创建 C\# 项目

创建 C\# 项目之前，要明白的是，如果只是修改/增加物品，人物或场景的话，可以不需要创建项目。

1. 启动 Microsoft Visual Studio 并且选择 `创建新项目`。
2. 选择 `经典库 (.NET Framework)`。
3. 给项目起名字并且选择框架 `.NET Framework 4.7.2`。如果不能选这个选项，可以从[这里](https://dotnet.microsoft.com/download/dotnet-framework/net472)下载。下载\(开发者包\)
4. 现在你的项目已经创建好，设置你的[构建路径](https://docs.microsoft.com/en-us/visualstudio/ide/how-to-change-the-build-output-directory?view=vs-2019)到你的游戏目录下的`Modules/MyModule/bin/Win64_Shipping_Client`。
5. [引用](https://docs.microsoft.com/en-us/visualstudio/ide/how-to-add-or-remove-references-by-using-the-reference-manager?view=vs-2019) 所有`bin\Win64_Shipping_Client`目录下的 `TaleWorlds.*` DLLs 文件到你的游戏文件夹（不是Mod目录）。并且引用 `TaleWorlds.*` DLLs 到每一个官方模组的 `Modules\ModuleName\bin\Win64_Shipping_Client` 里。

### Debugging 项目

1. 打开 项目属性 到 `Debug` 选项卡。
2. 选择 `启动外部程序` 选项，同时浏览到你游戏目录下（不是Mod目录）的`bin\Win64_Shipping_Client`文件夹里面的 `Bannerlord.exe`。
3. 设置工作目录到游戏目录（不是Mod目录）下的 `bin\Win64_Shipping_Client`。
4. 添加如下的命令行参数(要确定替代 `MyModule` 的名字) 
   * `/singleplayer _MODULES_*Native*SandBox*SandBoxCore*StoryMode*CustomBattle*MyModule*_MODULES_`

#### 在本教程中，我们的项目名字叫做 `ExampleMod`。

### 设置你的Module \(SubModule.xml\)

1. 选定游戏目录下的`Modules`文件夹。
2. 创建一个新的文件夹并且起名字，进入文件夹。
3. 创建文件夹名字为 `bin`。
4. 在 Visual Studio 中设置 构建输出的DLL到这个 `bin` 文件夹下面。
5. 在 VS Project 下创建一个新的类 `MySubModule`。
6. 创建文件 `SubModule.xml` 然后复制如下到文件中：

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


### Setting up your Module \(SubModule.xml\)

1. Go to your game files and locate the `Modules` directory.
2. Create a new folder and name it `ExampleMod` (Must be the same as the Id you use for Step #6).
3. Create a new folder named `bin` and inside this directory, create a new folder called `Win64_Shipping_Client`.
4. Set the build output for your DLL \(in Visual Studio\) to the previously created `bin` folder.
5. Create a new class in your VS Project and name it `MySubModule` \(_can be anything_\).
6. Create a new `SubModule.xml` file inside the folder you created in Step #2 and then paste the following into it:

   ```markup
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
   
7. 如果你用了不同的名字，记得修改对应的值
8. 开始启动，确保你的 Mod 出现 `Singleplayer` &gt; `Mods`。

对于Mod文件结构的信息，请参考[这里](../_intro/folder-structure.md)

## 编程

1. 打开 `MySubModule` 类。
2. 添加如下的引用。

   ```csharp
    using TaleWorlds.Core;
    using TaleWorlds.Localization;
    using TaleWorlds.MountAndBlade;
   ```
3. 继承类 `MBSubModuleBase` 类
4. 重载 `OnSubModuleLoad()` 函数
5. 添加如下代码到这个函数：

   ```csharp
    Module.CurrentModule.AddInitialStateOption(new InitialStateOption("Message",
        new TextObject("消息", null),
        9990,
        () => { InformationManager.DisplayMessage(new InformationMessage("Hello World!")); },
        false));
   ```

6. 编译你的项目并且确认输出到 `Modules\ExampleMod\bin\Win64_Shipping_Client` 下
7. 打开 骑砍Bannerlord 启动器并且选择 `Singleplayer` &gt; `Mods` 然后选择你的 Mod， 然后启动游戏。
8. 在标题页面，你应该能看到一个按钮叫做 `消息` ，点击你应该能看到 `Hello World` 出现在屏幕左下角。
9. 现在你已经成功创建了第一个骑砍2领主的Mod！
