# MBInitialScreenBase

You can create a custom title screen by inheriting from MBInitialScreenBase and then applying the GameStateScreen attribute to your class.

Here is a skeleton of what your inherited class should look like:

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

Replace the string `InitialScreen` with the name of your [Movie](../../_gauntlet/movie.md)'s XML file.

