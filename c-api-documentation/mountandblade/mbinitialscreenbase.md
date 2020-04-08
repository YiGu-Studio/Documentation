# MBInitialScreenBase

你可以通过继承MBInitialScreenBase类，然后将GameStateScreen特性赋予该类，从而创建一个属于你的自定义标题屏幕。

这里是一个让你知道如何正确操作的具体框架：

```csharp
[GameStateScreen(typeof(InitialState))]
public class MyInitialScreen : MBInitialScreenBase
{
    private GauntletLayer _gauntletLayer;
    private InitialMenuVM _dataSource;

    public MBInitialScreen(InitialState initialState) : base(initialState) { }

    protected override void OnInitialize()
    {
        base.OnInitialize();
        this._dataSource = new InitialMenuVM();
        this._gauntletLayer = new GauntletLayer(1, "GauntletLayer");
        this._gauntletLayer.LoadMovie("InitialScreen", this._dataSource);
        this._gauntletLayer.InputRestrictions.SetInputRestrictions(true, InputUsageMask.Mouse);
        base.AddLayer(this._gauntletLayer);
        GameNotificationManager.Current?.LoadMovie(false);
        ChatLog.Current?.LoadMovie(false);
        InformationManager.ClearAllMessages();
    }
}
```

将字符串`InitialScreen` 替换成你想要的[Movie](../../_gauntlet/movie.md)的XML文件名。

