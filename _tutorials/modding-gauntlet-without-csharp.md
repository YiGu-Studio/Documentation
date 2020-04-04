<<<<<<< HEAD
# Modding Gauntlet UIs Without C\#

## Important

### You Can **NOT** Use Depended Modules For This Tutorial. It Shouldn't Cause Any Issues Though.
=======
# 不需要C#的UI系统Mod入门 #

## 重要提示
### 本教程中，你 **不能** 使用任何依赖性的模组。尽管这方面应该不会有什么问题。
>>>>>>> translated modding-gauntlet-without-csharp.md


<<<<<<< HEAD
The following guide will walk you through step-by-step on how to create a mod that can overwrite any Gauntlet UI without using any C\#. For this example, we will be overriding the Quests UI with some custom title text.
=======
## 说明
>>>>>>> translated modding-gauntlet-without-csharp.md

接下来的指南将在不使用任何C#的情况下，一步一步地教你创建可以重写任何Gauntlet UI的Mod。在这个例子中，我们将使用一些自定义的文本重写任务UI。

## 准备

#### 在本教程中, 我们将要做的Mod命名为 `ExampleUIMod`.

### 设置好你的模组 \(SubModule.xml\)

1. 到游戏目录下，找到 `Modules` 文件夹。
2. 创建新文件夹，命名为 `ExampleUIMod` (必须和你在步骤#5中使用同样的 Id)

3. 创建新文件夹，命名为 `GUI` 并打开。

4. 在GUI文件夹中，创建文件夹并命名为`Prefabs`。我们等会儿会用到它。

5. 回到步骤#2中你所创建的模组文件夹（即ExampleUIMod，译者注），并且创建文件`SubModule.xml`，然后把如下代码粘贴到文件里：

   ```markup
    <Module>
        <Name value="Example UI Mod"/>
        <Id value="ExampleUIMod"/>
        <Version value="v1.0.0"/>
        <SingleplayerModule value="true"/>
        <MultiplayerModule value="false"/>
        <DependedModules/>
        <SubModules/>
        <Xmls/>
    </Module>
   ```

6. 运行启动器，保证你的Mod能够在`Singleplayer` &gt; `Mods`下出现。

要获取更多模组文件结构的信息, [点击这里](../_intro/folder-structure.md)

## 重写一个Gauntlet UI

注意: 你可以重写任何 Gauntlet UI. 然而，在本教程中, 我们只重写任务UI。

1. 到目录`Modules\SandBox\GUI\Prefabs\QuestsScreen` 并且复制 `QuestsScreen.xml` 文件到剪贴板。

2. 到“设置好你的模组”步骤#4中，你所创建的`Prefabs`文件夹下，粘贴`QuestsScreen.xml` 文件。

3. 在文本编辑器中打开粘贴的文件。
4. 搜索定位 (Ctrl+F) `Text="@QuestTitleText"`。
5. 替换 `@QuestTitleText` (包括 @ symbol) 为你想要的标题。
6. 保存文件。
7. 打开霸主启动器并且切换至 `Singleplayer` &gt; `Mods` 界面，确保你的Mod打了勾，然后启动游戏，随便选个存档开始游戏。

8. 打开任务UI，你应该能够在屏幕的中上方看到你添加的的文本。
9. 你已经成功创建了你第一个霸主Gauntlet Mod！

## 如何启用&使用动态UI编辑

<<<<<<< HEAD
1. Go to `Modules\SandBox\GUI\Prefabs\QuestsScreen` and copy the `QuestsScreen.xml` file to your clipboard
2. Go to the `Prefabs` folder you created in Step 4 of `Setting up your Module` and paste the `QuestsScreen.xml` from your clipboard.
3. Open the pasted file in a text editor.
4. Search \(Ctrl+F\) for a `Text="@QuestTitleText"` and go to this section of the file.
5. Replace `@QuestTitleText` \(including @ symbol\) with the text you want the title to be.
6. Save the file.
7. Open the Bannerlord launcher and navigate to `Singleplayer` &gt; `Mods` then make sure that your mod is ticked and start the game and load any save.
8. Open the Quests UI and you should see the text you added in the top middle of the screen.
9. You have now successfully created your first Bannerlord Gauntlet mod!
=======
>>>>>>> translated modding-gauntlet-without-csharp.md


动态UI编辑，是使你生活**大大**轻松的游戏特性。不幸的是，它不是你在基础版本的游戏内部就能启用的。

要启用它, 你必须 [下载 DeveloperConsole Mod](https://www.nexusmods.com/mountandblade2bannerlord/mods/4).

只要你下载 & 安装好了 Developer Console Mod, 按以下步骤操作，就能在游戏中启用动态编辑。

<<<<<<< HEAD
1. Open the game launcher and then make sure `Developer Console` is ticked in `Singleplayer` &gt; `Mods` along with your Gauntlet UI mod.
2. The Developer Console mod uses the shortcut `CTRL` + `~` \(tilde\) to enable the console. If this shortcut doesn't work for you, try pressing CTRL and then the key on your keyboard above Tab and below Esc.
3. Now that you can see the console, you will want to type the command `ui.toggle_debug_mode` to enable the live UI editing feature.
4. Any changes you make to your UIs should now update automatically in-game.

=======
1. 打开游戏启动器，确保 `Singleplayer` &gt; `Mods`界面的 `Developer Console`和你的Gauntlet UI Mod打上勾。
2. Developer Console Mod 使用 `CTRL` + `~`(波浪符) 快捷键开启控制台。如果你发现快捷键不起作用, 尝试按下CTRL，然后按下 你键盘上Tab和Esc之间的那个键。
3. 现在你已经看见了控制台，你会想键入`ui.toggle_debug_mode`命令来启用动态UI编辑特性。
4. 任何你对UI的改动，都应该会自动更新到游戏中。
>>>>>>> translated modding-gauntlet-without-csharp.md
