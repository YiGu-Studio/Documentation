# CampaignGameStarter 类

这个类用于给战役来描述行为,对话,菜单和模型,并运行`IGameStarter`接口.这在`OnGameStart`方法中很有用,这里有实例[MBSubModuleBase](mbsubmodulebase.md).

**注意**:*本页还未完工,如果你发现了这方面更多的内容,请提交pull request来完善该文档.*

##已知方法:
####`public void ClearEmptyObjects()`
(有待完善)
#### `public void AddBehavior(CampaignBehaviorBase campaignBehavior)`
添加[Campaign Behavior](campaignbehaviorbase.md)到当前战役.
#### `public void AddModel(GameModel model)`
添加[Game Model](../core/gamemodel.md)到当前战役.
#### `public void LoadGameTexts(string xmlPath)`
(有待完善)在输入路径中加载更多文本描述的XML文件.这些文本都有着*comment_strings.xml*这样的格式,然而当前还不知它们的作用.
#### `public void LoadGameMenus(Type typeOfGameMenusCallbacks, string xmlPath)`
(有待完善)在输入路径中加载更多菜单描述的XML文件.
#### `public void AddGameMenu(string menuId, string menuText, OnInitDelegate initDelegate, GameOverlays.MenuOverlayType overlay = GameOverlays.MenuOverlayType.None, GameMenu.MenuFlags menuFlags = GameMenu.MenuFlags.none, object relatedObject = null)`
用法参见[GameMenu](gamemenu.md).
#### `public void AddWaitGameMenu(string idString, string text, OnInitDelegate initDelegate, OnConditionDelegate condition, OnConsequenceDelegate consequence, OnTickDelegate tick, GameMenu.MenuAndOptionType type, GameOverlays.MenuOverlayType overlay = GameOverlays.MenuOverlayType.None, float targetWaitHours = 0f, GameMenu.MenuFlags flags = GameMenu.MenuFlags.none, object relatedObject = null)`
(有待完善)
#### `public void AddGameMenuOption(string menuId, string optionId, string optionText, GameMenuOption.OnConditionDelegate condition, GameMenuOption.OnConsequenceDelegate consequence, bool isLeave = false, int index = -1, bool isRepeatable = false)`
用法参见[GameMenu](gamemenu.md).

##已知属性
**注意**:*所有这些属性只有读取功能*
#### `public readonly bool IsTutorial`
战役开局是否开启教学.
#### `public ICollection<CampaignBehaviourBase> CampaignBehaviors`
所有已注册的战役行为收录[Campaign Behaviours](campaignbehaviorbase.md).
#### `public IEnumerable<GameModel> Models`
枚举所有已注册的游戏模型[Game Models](../core/gamemodel.md).

##示例应用
在[MBSubModuleBase]( mbsubmodulebase.md) 类中使用:
```csharp
protected override void OnGameStart(Game game, IGameStarter gameStarter) 
{
