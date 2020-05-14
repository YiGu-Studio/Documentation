# CampaignBehaviorBase 类

这是一个抽象类[TaleWorlds.CampaignSystem](./README.md),它可以为战役中的独特行为的代码所继承.

## 抽象方法:
### ```public abstract void RegisterEvents()```
定义此方法时,可以用`CampaignEvents.On...`来确定事件的结果.简易范例:
```csharp
public override void RegisterEvents()
{   
    CampaignEvents.OnClanDestroyedEvent.AddNonSerializedListener(this, new Action<Clan>(
    clan => {
        String clanName = clan.Name.ToString();
        InformationManager.DisplayMessage(new InformationMessage("The " + clanName + " was destroyed!"));
    }));
}
```
上面的范例注册为一个事件,譬如某个家族灭亡时在消息框会宣布此消息. `AddNonSerializedListener`方法调用的第二个变量是一个动作,对于此动作描述[点击这里](https://docs.microsoft.com/en-us/dotnet/api/system.action-1?view=netframework-4.8).

###```public abstract void SyncData(IDataStore dataStore)```
(译者注:原作者说未完工)

**注意**:这个方法至今我们仍费解,但我们强烈建议直接放上空方法如下:
```csharp
public override void SyncData(IDataStore dataStore)
{
}
```

## 注册战役行为:
在你的[MBSubModuleBase](../mountandblade/mbsubmodulebase.md)类中,你可以用`OnGameStart`方法来为战役添加行为.以下为示例:
```csharp
protected override void OnGameStart(Game game, IGameStarter gameStarter) 
{
    if(game.GameType is Campaign) 
    {
        //The current game is a campaign
        CampaignGameStarter campaignStarter = (CampaignGameStarter) gameStarter;
        campaignStarter.AddBehavior(new ExampleBehavior());
        //ExampleBehavoir is our custom class which extends CampaignBehaviorBase
    }
}
```
