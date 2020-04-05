# GameEntity

GameEntities指的是游戏中的实体，比如说角色、建筑、树、马等等。游戏中的所有道具都属于实体。


GameEntities 本身包含有网格、骨骼、物理模块、以及挂载的脚本等等其它事物。


你可以通过编辑[Scene](../../_xmldocs/scene.md)的 `scene.xscene` 文件，或者使用GameEntity类中的静态方法直接生成 \(创造\)  来向场景中添加 GameEntity。

```csharp
GameEntity.Instantiate(Scene scene, string prefabName, MatrixFrame frame)
```

示例用法 \(在[Agent]的main中生成 (../mountandblade/agent.md)\) ：

```csharp
GameEntity.Instantiate(Mission.Current.Scene, "ship_a", Agent.Main.Frame)
```

## 联机游戏的GameEntities

有的GameEntities并不会在客户端之间同步，除非它添加了SynchedMissionObject ScriptComponent。

